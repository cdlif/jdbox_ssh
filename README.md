## 京东云无线宝开启ssh 

#### 1.登录路由器

#### 2.按 F12 进入控制台

#### 3.输入以下命令启动 dropbear
```
$.ajax({
    url: 'http://' + $.cookie("HostAddrIP") + '/jdcapi',
    async: false,
    data: JSON.stringify({
        jsonrpc: "2.0",
        id: 1,
        method: "call",
        params: [
            $.cookie("sessionid"),
            "service",
            "set",
            {
                "name": "dropbear",
                "instances": {"instance1": {"command": ["/usr/sbin/dropbear"]}}
            }
        ]
    }),
    dataType: 'json',
    type: 'POST'
})
```
