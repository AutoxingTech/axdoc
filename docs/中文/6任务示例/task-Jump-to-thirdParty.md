# 多点任务跳转到第三方页面

## 跳转到第三方页面操作流程
1.配置：在设置界面中=>其他设置=>定制页面设置 打开配置开关，以及配置任务开始跳转到第三方页面地址http://xxx.com/xxx.html和任务到达跳转到第三方页面地址http://xxx.com/xxx.html

2.任务开始：在多点任务创建界面，点击任务点位，跳转到配置的任务开始页面，会传递当前点位名称,Id,第三方处理完业务后，向基线APP发送消息返回到基线APP， 然后开始任务

3.任务到达：在任务到达时会跳转到配置的任务到达页面，会传递当前点位名称,Id,以及订单号，第三方页面地址等，第三方处理完业务后，向基线APP发送消息返回到基线APP， 然后继续任务

## 第三方页面eg:
1.提供客户自己页面的地址 eg: http://10.10.20.125:8000/xxx.html

2.页面大小：1280*720

3.客户自己页面需要提供通信的方法
```javascript
// 监听来自基线app的消息
window.addEventListener('message', (event) => {
  if(event.data) {
    /**
     * @params  event.data
     * name: 当前点位名称
     * id: 当前点位id
     * orderId: 当前点位订单号, 来只客户页面生成的订单号
     * */
    const data = JSON.parse(event.data); // {name: ''}
    // poiName.innerText = 当前点位: ${data.name} + (data.orderId ? (订单号:${data.orderId}) : '');
  }
})


// 向基线APP 发送消息
    /**
     * @params  data
     * type: 0 取消 1 确定
     * orderId: 当前订单号 (唯一ID, 用于到达页面通知客户页面当前生成的订单号)
     * url: 不必填参数   用于指定到达页面跳转到客户页面的地址，如果不传默认跳转到机器人配置里设置的到达页面
     * */
    const data = {
        type: 0,
        orderId: 'PO1728544645390',
        url: 'http://www.xxx.com'
    }
    // 向基线APP 发送消息
    window.parent.postMessage(data, '*'); // '*' 可以替换为具体的源

```

4.客户自己页面参考例子
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<style>
    * {
        margin: 0;
        padding: 0;
    }

    body {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        width: 100%;
        height: 100%;
    }

    .header,
    .body-con,
    select,
    .footer {
        text-align: center;
        font-size: 24px;
    }

    .header {
        padding-top: 20px;
        height: 10%;
    }
    .input-item {
        border: 1px solid #cccccc;
        height: 40px;
        text-indent: 10px;
        width: 300px;
    }

    .body-con {
        width: 100%;
        height: 10%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .body-111 {
        width: 100%;
        height: 60%;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        font-size: 24px;
        flex-direction: column;
    }
    .body-111 p {
        text-align: center;
    }

    .footer {
        width: 100%;
        height: 10%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .btn {
        background: #646cff;
        padding: 10px 30px;
        border-radius: 10px;
        color: #f9f9f9;
        margin-right: 30px;
    }
    .cancel {
        background: #cccccc;
    }
</style>

<body>

<div class="header">
    <h3 id="poi-name">当前点位: </h3>
    <h5>扫描条形码</h5>
</div>
<div class="body-con">
    <div class="input-box">
        <input id="elInput" class="input-item" autofocus placeholder="请扫描条形码" @blur="blur" @input="changeCode">
    </div>
</div>

<div class="body-111" id="code-list">
</div>

<div class="footer">
    <span class="btn cancel" id="close">取消</span>
    <span class="btn" id="sure">确定</span>
</div>
</body>

<script>
    window.onload = function() {
        const elInput = document.getElementById('elInput');
        elInput.focus();
        const poiName = document.getElementById('poi-name');
        // 监听来自基线app的消息
        window.addEventListener('message', (event) => {
            console.log('Message from parent:', event.data);
            if(event.data) {
                /**
                 * @params  event.data
                 * name: 当前点位名称
                 * id: 当前点位id
                 * orderId: 当前点位订单号, 来只客户页面生成的订单号
                 * */
                const data = event.data;
                poiName.innerText = `当前点位: ${data.name}` + (data.orderId ? `(订单号:${data.orderId})` : '');
            }
        });

        // 获取按钮元素
        const button = document.getElementById('close');
        const sureBtn = document.getElementById('sure');
        const codeListDom = document.getElementById('code-list');
        const codeList = JSON.parse(localStorage.getItem('codeList') || '[]')
        inseterHtml()
        elInput.addEventListener('input', (event) => {
            console.log('输入内容:', event.target.value);
            pushCode(event.target.value)
        })

        var debounce = (fn,delay = 1000)=>{
            let t =null
            return (...args)=>{
                const context = this;
                if(t!=null){
                    clearTimeout(t)
                }
                t=setTimeout(()=>{
                    fn.apply(context, args)
                },delay)
            }
        }
        var pushCode = debounce((value) => {
            value = value.replace("\n", "")
            const index = codeList.findIndex((item)=>{
                return  item === value
            })
            if(index !== -1) {
                codeList.splice(index, 1)
                elInput.value = '';
            }else {
                codeList.push(value)
                elInput.value = '';
            }
            inseterHtml()

        }, 200)


        function inseterHtml() {
            const html = codeList.reduce((acc, curr) => {
                return acc + `<p>${curr}</p>`
            }, '')
            codeListDom.innerHTML = html
        }

        sureBtn.onclick = function () {
            localStorage.setItem('codeList', JSON.stringify(codeList))
            /**
             * @params  data
             * type: 0 取消 1 确定
             * orderId: 当前订单号 (唯一ID, 用于到达页面通知客户页面当前生成的订单号)
             * */
            const data = {
                type: 1,
                orderId: `PO${new Date().getTime()}`,
            }
            // 向父页面发送消息
            window.parent.postMessage(data, '*'); // '*' 可以替换为具体的源
        }

        // 添加点击事件监听器
        button.addEventListener('click', () => {
            const data = {
                type: 0,
            }
            // 向父页面发送消息
            window.parent.postMessage(data, '*'); // '*' 可以替换为具体的源
        });
    };
</script>
</html>


```







多点任务到达后跳转到第三方页面

```typescript 
const task5 = {
    "name": "多点任务",
    "runNum": 1,
    "runMode": 1,
    "taskType": 2,
    "runType": 21,
    "curPt": {},
    "pts": [
        {
            "x": 7.276271231262399,
            "y": -22.44962375343107,
            "yaw": 261.5,
            "areaId": "67e67399103fd836e52050db",
            "dockingRadius": "1",
            "ext": {
                "name": "点位一",
                "id": "67e6739c217da3b4832b32ff",
                "orderId": "PO1752474223883",  // 第三方页面反馈的订单id
                "url": "http://10.10.40.134:5173/index.html"   // 跳转到第三方页面的地址
            },
            "stepActs": [
                {
                    "type": 5,
                    "data": {
                        "mode": 1,
                        "audioId": "3111002",
                        "num": 1,
                        "volume": 0,
                        "interval": -1,
                        "duration": -1,
                        "forcePlay": true
                    }
                },
                {
                    "type": 40
                }
            ]
        }
    ],
    "backPt": {},
    "ignorePublicSite": true
}
const success = axRobot.startTask(task5)
```