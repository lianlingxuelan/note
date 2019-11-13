### Axja封装
```javascript
function ajxa(){
    var xhr = null
    //浏览器兼容
    var params = formasParams(options.data)
    if(window.XMLHttpRequest()){
        xhr = new XMLHttpRequest()
    }else{
        xhr = new ActiveXObject('Microsoft.XMLHttpRequest')
    }
    //type请求连接
    if(options.type == 'GET'){//注意类型为大写
        xhr.open(options.type,options.url + "?" + params,options.async)
        xhr.send(null)
    }else if(options.type == 'POST'){
        xhr.open(options.type,options.url,options.async);
        xhr.setRequestHeader("Content-Type","application/x-www-form-urlencoded");
        xhr.send(params);
    }
    xhr.onreadystatechange = function(){
        if(xhr.readystatechange == 4 && xhr.status == 200){
            options.success(xhr.responseText);
        }
    }
    function formsParms(data){
        var arr = []
        for(var prop in data){
            arr.push(prop + '=' + data[prop]);
        }
        return arr.join('&')
    }
}
axja({
    url: 'http:www.amistyz.com:5555/login',
    type: 'post',
    async: true,
    data: {
        username: '123421',
        password: 'sadasd'
    },
    success: function(data){
        console.log(data)
    }
})
```
