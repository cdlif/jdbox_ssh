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
                "instances":{"instance1":{"command":["/usr/sbin/dropbear"]}}
            }
        ]
    }),
    dataType: 'json',
    type: 'POST'
})
