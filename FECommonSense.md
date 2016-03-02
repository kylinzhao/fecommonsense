###常见问题

* 图片请求没有正确发出
	* image加onload事件
	* image加随机数
* 遮盖层的宽高

```javascript

	function getDE(){
		return (document.compatMode && document.compatMode.toLowerCase() == "css1compat") ?
				document.documentElement : document.body;
    }

    function getWH(){
        var de = getDE();
        return { width : Math.max( de.clientWidth , de.scrollWidth ) ,
        	height : Math.max( de.clientHeight , de.scrollHeight )
        };
    }
```

* 判断全局变量是否存在用window.xxx，直接判断变量会因为undefined报错导致程序无法继续
* 用==不用===
* parseInt必须传第二个参数
* HTML5跨域办法
	* 修改response头：Access-Control-Allow-Origin
	* xhr.withCredentials = true
	* 参考 http://www.html5rocks.com/en/tutorials/cors/
* fekit组件内需要install其他组建时要保证根目录有fekit_modules目录才可以安装
* HttpServletRequest.getScheme获取https结果获得了http [stackoverflow]('http://stackoverflow.com/questions/19598690/how-to-get-host-name-with-port-from-a-http-or-https-request')
