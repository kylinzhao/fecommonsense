###常见问题

* 图片请求没有正确发出
	* image加onload事件
	* image加随机数
* 遮盖层的宽高
 
 ````javascript

	function getDE(){
		return (document.compatMode && document.compatMode.toLowerCase() == "css1compat") ? document.documentElement : document.body;
    }
    function getWH(){
        var de = getDE();
        return { width : Math.max( de.clientWidth , de.scrollWidth ) , 
        	height : Math.max( de.clientHeight , de.scrollHeight )
        };
    }
````