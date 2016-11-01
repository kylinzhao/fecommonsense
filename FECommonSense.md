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
* 用===不用==
* parseInt必须传第二个参数
* HTML5跨域办法
	* 修改response头：Access-Control-Allow-Origin
	* xhr.withCredentials = true
	* 参考 http://www.html5rocks.com/en/tutorials/cors/
* fekit组件内需要install其他组建时要保证根目录有fekit_modules目录才可以安装
* HttpServletRequest.getScheme获取https结果获得了http [stackoverflow](http://stackoverflow.com/questions/19598690/how-to-get-host-name-with-port-from-a-http-or-https-request)
* windows抓包代理软件fiddler
* mac抓包代理软件charles
* 图片在浏览器上的内存消耗 长*宽*4bytes
* 渲染图片的内存消耗跟显示大小无关，跟图片本身尺寸有关
* 微信调试工具 http://blog.qqbrowser.cc/
* 页面中使用的图片大小超过80kb时需要注意是否可以压缩
* 接口、API等命名绝对不能叫newXXX，oldXXX之类的
* 不要让依赖第三方的接口把整个页面搞挂，需要让这部分内容异步加载
* CSS，DOM命名最好不要带AD，极有可能被adblock之类的广告插件给拦掉
* React Component 首字母必须为大写，[参考原因](http://stackoverflow.com/questions/30373343/reactjs-component-names-must-begin-with-capital-letters)
