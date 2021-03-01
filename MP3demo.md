---
title: MP3的下载播放代码
categories: 技术
---


``` bash
<a href='http://img.a3008.xin/converter/9135/20190102/快快乐乐哈哈.mp3'>播放</a>
<a href='#' onclick='down()'>下载</a>
<script src="https://code.jquery.com/jquery-3.3.1.min.js"></script>
<script>
function down(){
	//使用方法  
	var fileUrl = 'http://img.a3008.xin/converter/9135/20190102/快快乐乐哈哈.mp3';  
	loadFile(fileUrl, function(URI) {  
		// 下载完毕回调，URI是blob的资源地址，可以直接调用

		var bURL = URI;

		var link = document.createElement('a');
		link.href = bURL;
		link.setAttribute('download', "快快乐乐哈哈.mp3");
		document.getElementsByTagName("body")[0].appendChild(link);
		// Firefox
		if (document.createEvent) {
			var event = document.createEvent("MouseEvents");
			event.initEvent("click", true, true);
			link.dispatchEvent(event);
		}
		// IE
		else if (link.click) {
			link.click();
		}
		link.parentNode.removeChild(link);
	});
}

function loadFile(uri, callback) {  
    if (typeof callback != 'function') {  
        callback = function(uri) {  
            console.log(uri);  
        }  
    }  
    var xhr = new XMLHttpRequest();  
    xhr.responseType = 'blob';  
    xhr.onload = function() {  
        callback(window.URL.createObjectURL(xhr.response));  
    }  
    xhr.open('GET', uri, true);  
    xhr.send();
}
   
</script>
```