# 安卓端-入口 MainActivity

##  1. 项目地址
[https://github.com/AutoxingTech/android_webview_demo](https://github.com/AutoxingTech/android_webview_demo)

##  2. 文件地址
安卓入口文件:
file:///android_webview_demo\app\src\main\java\com\autoxing\delivery\MainActivity.java  
js入口文件:
file:///android_asset/dist/index.html

## 3. 安卓加载webview代码及说明

### 示例

???+ example

    === "java 安卓"
        ```java 
        ##### "java 初始化活动的加载配置webview"
        /**
        * 初始化活动的主要方法
        * 此方法设置主布局，检查并请求外部存储权限，配置WebView，并初始化视图组件
        * @param savedInstanceState 保存的实例状态，当活动重新创建时使用
        */
        protected void onCreate(Bundle savedInstanceState) {
                super.onCreate(savedInstanceState);
                setContentView(R.layout.activity_main);
        
                // 检查并请求外部存储权限
                if (Build.VERSION.SDK_INT>=23&&checkSelfPermission(Manifest.permission.WRITE_EXTERNAL_STORAGE)!= PackageManager.PERMISSION_GRANTED){
                    requestPermissions(new String[]{Manifest.permission.WRITE_EXTERNAL_STORAGE},1);
                }
        
                // 必须保留此行以创建外部文件目录
                getExternalFilesDir("").getAbsolutePath();
        
                // 初始化启动视图并设置点击监听器
                launcherView = findViewById(R.id.launch_view);
                // 设置启动器视图的点击监听器
                launcherView.setOnClickListener(new View.OnClickListener() {
                    @Override
                    public void onClick(View view) {
                        // 当点击事件发生时，调用主活动的加载WebView方法
                        MainActivity.this.loadWebView();
                    }
                });
        
        
                // 配置WebView的设置
                webView = findViewById(R.id.web_view);
                // 启用JavaScript支持，对于现代网页的交互功能是必需的
                webView.getSettings().setJavaScriptEnabled(true);
                // 允许访问文件资源，以便webView可以加载本地文件协议的内容
                webView.getSettings().setAllowFileAccess(true);
                // 允许访问内容资源，即允许加载http/https协议的内容
                webView.getSettings().setAllowContentAccess(true);
                // 启用DOM存储，以便网页可以使用本地存储功能
                webView.getSettings().setDomStorageEnabled(true);
                // 设置WebChromeClient以增强WebView的功能
                webView.setWebChromeClient(new WebChromeClient());
        
                // 自定义WebViewClient以处理页面加载事件
                webView.setWebViewClient(new WebViewClient(){
                    // 定义一个布尔变量用于标记页面是否加载完成
                    Boolean pageFinished = false;
        
                    /**
                     * 当页面开始加载时调用
                     * @param view    WebView控件
                     * @param url     正在加载的网址
                     * @param favicon 网站的图标
                     */
                    @Override
                    public void onPageStarted(WebView view, String url, Bitmap favicon) {
                        Log.i(TAG,"onPageStarted");
                        // 页面开始加载时，将加载的标记设置为false
                        pageFinished = false;
                        super.onPageStarted(view, url, favicon);
                    }
        
                    /**
                     * 当页面加载完成时调用
                     * @param view WebView控件
                     * @param url  已加载完成的网址
                     */
                    @Override
                    public void onPageFinished(WebView view, String url) {
                        Log.i(TAG,"onPageFinished"+view.getProgress());
                        // 检查页面是否完全加载完成且尚未被标记为完成
                        if(view.getProgress()==100&&pageFinished==false){
                            // 启动一个新的线程
                            new Thread(new Runnable() {
                                @Override
                                public void run() {
                                    try {
                                        // 让线程睡眠1秒
                                        Thread.sleep(1000*1);
                                    }catch (Exception e){
                                        e.printStackTrace();
                                    }
                                    // 在UI线程中运行代码，通常用于更新UI
                                    runOnUiThread(new Runnable() {
                                        @Override
                                        public void run() {
                                            // 隐藏launcherView，例如加载指示器
                                            launcherView.setVisibility(View.GONE);
                                        }
                                    });
                                }
                            }).start();
                            // 将页面加载完成的标记设置为true
                            pageFinished = true;
                        }
                        super.onPageFinished(view, url);
                    }
        
                });
        
                // 注册JavaScript接口，允许JavaScript调用Android方法
                webView.addJavascriptInterface(MainActivity.this, "app");
        
                // 初始化WebView加载操作
                this.loadWebView();
        
                // 设置按钮的点击监听器，用于调用WebView中的JavaScript方法
                findViewById(R.id.btn).setOnClickListener(new View.OnClickListener() {
                    @Override
                    public void onClick(View view) {
                        webView.loadUrl("javascript:callJSHello("+Math.random()+")");
                    }
                });
        
                // 当Activity被创建时，记录日志
                Log.i(TAG,"onCreate");
            }
        
        ```
            
            
        ```java 
            ##### "java 该方法主要负责显示WebView并加载特定的URL，用于展示SDK的功能"
            /**
             * 在实际应用中，可以通过加载特定的URL来体验和交互SDK提供的功能
             */
            private void loadWebView() {
                // 设置launcherView为可见状态，可能用于指示WebView的加载过程
                launcherView.setVisibility(View.VISIBLE);
        
                // 以下是关于如何使用WebView的说明注释
                // 运行此项目 https://github.com/AutoxingTech/AX_SDK1.0_Example,
                // 之后 webView.loadUrl("https://xxxxx/sdk/v1.0/example");
                // 即可体验sdk功能
                // file:///android_asset/dist/index.html 为android与js交互demo
        
                // 加载本地HTML文件，用于展示SDK功能和android与js的交互示例
                webView.loadUrl("file:///android_asset/dist/index.html");
            }
        ```
        
        ```java 
            ##### "java主要目的是演示如何从JavaScript代码调用Android（Java）方法进行交互"
            /**
             * 此方法的主要目的是演示如何从JavaScript代码调用Android（Java）方法。
             * @param args JavaScript方法传递的参数，将作为输入字符串进行处理。
             * @return 返回拼接了输入参数、随机数和固定字符串的结果字符串。
             */
            @android.webkit.JavascriptInterface
            public String actionFromJsHello(String args) {
                return args+Math.random()+"android_返回结果";
            }
        
        
            /**
             * 此方法的主要目的是在JavaScript代码中触发网页刷新操作。
             * 它通过在Android主线程中执行刷新操作来实现。
             */
            @android.webkit.JavascriptInterface
            public void actionFromJsWebRefresh() {
                Log.i(TAG,"刷新网页");
                runOnUiThread(new Runnable() {
                    @Override
                    public void run() {
                        MainActivity.this.loadWebView();
                    }
                });
            }
        ```

    === "js 引入sdk"

        ```html
        <!DOCTYPE html>
        <html lang="en">
        <head>
            // 引入js-sdk
            <script src=./autoxing-robot-js-sdk1.0.81.js></script>
            <script>
                // appId 可向相关运营人员申请提供
                const appId = "—————————————"
                // 密钥  可向相关运营人员申请提供
                const appSecret = "——————————————————————————————"
                // 定义机器人sn
                const robotId = "xxxxxxxxxxx817"
                // 初始化，参数包括应用ID、应用密钥和应用模式，这里设置为广域应用模式
                * **AppMode** - [AppMode](../Define/Define-AppMode)
                let axRobot = new AXRobot(appId, appSecret, AppMode.WAN_APP);
        
                // 初始化
                function init() {
                    axRobot.init().then((isOk) => { //初始化
                        return axRobot.connectRobot({ //连接机器人
                            robotId: robotId
                        })
                    }).then((isOK) => {
                        return axRobot.getPoiList(); //拉取站点信息
                    }).then((res) => {
                        console.log(res)
                    }).catch((res) => {
                        console.log(res.errText)
                    })
                }
        
                // 安卓调用JavaScript的Hello函数 @param {string} text - 从Android传入的字符串参数
                function callJSHello(text) {
                    // 调用sdk初始化
                    init()
        
                    // 获取ID为"androidContent"的元素，显示从Android传入的值，前面加上提示文本
                    document.getElementById("androidContent").innerHTML = "Android传入值：" + text
                }
        
                // js 调用 Android 提供的方法
                function clickAndroidHello() {
                    //app来自： webView.addJavascriptInterface(MainActivity.this, "app");
                    let android_res = app.actionFromJsHello("你好")
                    // 通过调取安卓方法返回值显示在ID为"androidContent"的元素
                    document.getElementById("androidContent").innerHTML = android_res
                }
        
                // js调用Android的方法刷新webView
                function clickAndroidRefresh() {
                    //调用Android原生的app.actionFromJsWebRefresh方法，进行WebView的刷新操作.
                    app.actionFromJsWebRefresh()
                }
            </script>
        </head>
        <body>
        <div style="margin-top:50px;font-weight:bold">111Android WebView 交互Demo</div>
        <div id="androidContent">
        </div>
        <button onclick="clickAndroidHello()">调用Android代码</button>
        <button onclick="clickAndroidRefresh()">调用Android刷新webView</button>
        </body>
        
        </html>
        ```

