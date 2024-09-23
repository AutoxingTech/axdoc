# Android entrance MainActivity

##  1. github
[https://github.com/AutoxingTech/android_webview_demo](https://github.com/AutoxingTech/android_webview_demo)

##  2. File address
Android entrance file:
file:///android_webview_demo\app\src\main\java\com\autoxing\delivery\MainActivity.java  
js entrance file:
file:///android_asset/dist/index.html

## 3. Android loading webview code and instructions

### example

???+ example

    === "java Android"
        ```java 
        ##### "java Initialize the loading configuration of the activity webview"
        /**
        *The main methods for initializing activities
        *This method sets the main layout, checks and requests external storage permissions, configures WebView, and initializes view components
        *The instance state saved by @ paramsavedInstanceState is used when the activity is recreated
        */
        protected void onCreate(Bundle savedInstanceState) {
                super.onCreate(savedInstanceState);
                setContentView(R.layout.activity_main);
                
                // Check and request external storage permissions
                if (Build.VERSION.SDK_INT>=23&&checkSelfPermission(Manifest.permission.WRITE_EXTERNAL_STORAGE)!= PackageManager.PERMISSION_GRANTED){
                    requestPermissions(new String[]{Manifest.permission.WRITE_EXTERNAL_STORAGE},1);
                }
        
                // This line must be retained to create an external file directory
                getExternalFilesDir("").getAbsolutePath();
        
                // Initialize the startup view and set the click listener
                launcherView = findViewById(R.id.launch_view);
                // Set the click listener for the launcher view
                launcherView.setOnClickListener(new View.OnClickListener() {
                    @Override
                    public void onClick(View view) {
                        // When a click event occurs, call the loading WebView method of the main activity
                        MainActivity.this.loadWebView();
                    }
                });
        
        
                // Configure WebView settings
                webView = findViewById(R.id.web_view);
                // Enabling JavaScript support is necessary for the interactive functionality of modern web pages
                webView.getSettings().setJavaScriptEnabled(true);
                // Allow access to file resources so that WebView can load the content of local file protocols
                webView.getSettings().setAllowFileAccess(true);
                // Allow access to content resources, i.e. allow loading of HTTP/HTTPS protocol content
                webView.getSettings().setAllowContentAccess(true);
                // Enable DOM storage so that web pages can use local storage functionality
                webView.getSettings().setDomStorageEnabled(true);
                // Set up WebChrome Client to enhance the functionality of WebView
                webView.setWebChromeClient(new WebChromeClient());
        
                // Custom WebViewClient to handle page loading events
                webView.setWebViewClient(new WebViewClient(){
                    // Define a boolean variable to mark whether the page has finished loading
                    Boolean pageFinished = false;
                
                    /**
                     * Called when the page starts loading
                     * @param view    WebView control
                     * @param url     The URL being loaded
                     * @param favicon The website's icon
                     */
                    @Override
                    public void onPageStarted(WebView view, String url, Bitmap favicon) {
                        Log.i(TAG, "onPageStarted");
                        // Set the loading mark to false when the page starts loading
                        pageFinished = false;
                        super.onPageStarted(view, url, favicon);
                    }
                
                    /**
                     * Called when the page has finished loading
                     * @param view WebView control
                     * @param url  The URL that has finished loading
                     */
                    @Override
                    public void onPageFinished(WebView view, String url) {
                        Log.i(TAG, "onPageFinished" + view.getProgress());
                        // Check if the page has completely finished loading and has not yet been marked as finished
                        if (view.getProgress() == 100 && pageFinished == false) {
                            // Start a new thread
                            new Thread(new Runnable() {
                                @Override
                                public void run() {
                                    try {
                                        // Sleep the thread for 1 second
                                        Thread.sleep(1000 * 1);
                                    } catch (Exception e) {
                                        e.printStackTrace();
                                    }
                                    // Run code on the UI thread, typically used for updating the UI
                                    runOnUiThread(new Runnable() {
                                        @Override
                                        public void run() {
                                            // Hide launcherView, e.g., loading indicator
                                            launcherView.setVisibility(View.GONE);
                                        }
                                    });
                                }
                            }).start();
                            // Set the page loading completion mark to true
                            pageFinished = true;
                        }
                        super.onPageFinished(view, url);
                    }
                });
        
                // Register a JavaScript interface, allowing JavaScript to call Android methods
                webView.addJavascriptInterface(MainActivity.this, "app");
                
                // Initialize the WebView loading operation
                this.loadWebView();
                
                // Set an onClick listener for the button to call a JavaScript method in the WebView
                findViewById(R.id.btn).setOnClickListener(new View.OnClickListener() {
                @Override
                public void onClick(View view) {
                // Call the JavaScript function 'callJSHello' with a random number as an argument
                webView.loadUrl("javascript:callJSHello(" + Math.random() + ")");
                }
                });
                
                // Log when the Activity is created
                Log.i(TAG, "onCreate");

            }
        
        ```
            
            
        ```java 
            ##### "java This method is mainly responsible for displaying WebViews and loading specific URLs to showcase the functionality of the SDK"
            /**
             * In practical applications, one can experience and interact with the functions provided by the SDK by loading specific URLs
             */
           private void loadWebView() {
                // Set launcherView to visible, possibly to indicate the loading process of the WebView
                launcherView.setVisibility(View.VISIBLE);
                
                // The following is a comment on how to use the WebView
                // Run this project https://github.com/AutoxingTech/AX_SDK1.0_Example,
                // and then use webView.loadUrl("https://xxxxx/sdk/v1.0/example") to experience SDK functionality
                // file:///android_asset/dist/index.html is a demo of Android and JS interaction
            
                // Load a local HTML file to showcase SDK functionality and the interaction example between Android and JS
                webView.loadUrl("file:///android_asset/dist/index.html");
            }
        ```
        
        ```java 
            ##### "The main purpose of Java is to demonstrate how to call Android (Java) methods from JavaScript code for interaction"
            // The main purpose of this Java method is to demonstrate how to call Android (Java) methods from JavaScript code.
            /**
             * This method's main purpose is to demonstrate how to call Android (Java) methods from JavaScript code.
             * @param args The parameters passed from the JavaScript method, processed as input strings.
             * @return Returns a result string concatenated with the input parameters, a random number, and a fixed string.
             */
            @android.webkit.JavascriptInterface
            public String actionFromJsHello(String args) {
            return args + Math.random() + "android_return_result";
            }
            
            /**
            * This method's main purpose is to trigger a webpage refresh operation in JavaScript code.
            * It accomplishes this by executing the refresh operation on the Android main thread.
            */
            @android.webkit.JavascriptInterface
            public void actionFromJsWebRefresh() {
                Log.i(TAG, "Refreshing webpage");
                runOnUiThread(new Runnable() {
                    @Override
                    public void run() {
                        MainActivity.this.loadWebView();
                    }
                });
            }
        ```

    === "js Introducing SDK"

        ```html
        <!DOCTYPE html>
          <html lang="en">
          <head>
              // 引入js-sdk
              <script src=./autoxing-robot-js-sdk1.0.81.js></script>
              <script>
                  // appId You can apply to the relevant operational personnel to provide
                  const appId = "—————————————"
                  // appSecret  You can apply to the relevant operational personnel to provide
                  const appSecret = "——————————————————————————————"
                  // robot sn
                  const robotId = "xxxxxxxxxxx817"
                  // Initialization, parameters include application ID, application key, and application mode, set to wide area application mode here
                  * **AppMode** - [AppMode](../Define/Define-AppMode)
                  let axRobot = new AXRobot(appId, appSecret, AppMode.WAN_APP);
        
                  // init
                  function init() {
                      axRobot.init().then((isOk) => { //init
                          return axRobot.connectRobot({ //connectRobot
                              robotId: robotId
                          })
                      }).then((isOK) => {
                          return axRobot.getPoiList(); //get poiList
                      }).then((res) => {
                          console.log(res)
                      }).catch((res) => {
                          console.log(res.errText)
                      })
                  }
        
                  // Android calls JavaScript's Hello function @ param {string} text - string parameter passed from Android
                  function callJSHello(text) {
                      // sdk init
                      init()
        
                      // Get the element with ID 'androidContent', display the value passed in from Android, and add prompt text before it
                      document.getElementById("androidContent").innerHTML = "Android：" + text
                  }
        
                  // js Call the methods provided by Android
                  function clickAndroidHello() {
                      //app from： webView.addJavascriptInterface(MainActivity.this, "app");
                      let android_res = app.actionFromJsHello("你好")
                      // By calling the Android method, the return value is displayed in the element with ID "androidContent"
                      document.getElementById("androidContent").innerHTML = android_res
                  }
        
                  // JavaScript calls Android method to refresh WebView
                  function clickAndroidRefresh() {
                      //Call the Android native app.actionFromJsWebRefresh method to perform a WebView refresh operation
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

