##使用说明
1.添加插件到项目 
cordova plugin add https://github.com/songchaoyuan/cordova-plugin-alipay --variable PARTNER_ID=[你的商户PID可以在账户中查询] 

2.定义全局变量
declare var AliPay: any;  

3.调用代码
let payInfo  = "xxx";  

AliPay.pay(payInfo,  
  function success(e){  
    alert('success!');  
},function error(e){  
	alert('error!');  
});  


#修改于http://blog.csdn.net/qq_15096707/article/details/53073547#

4.在info.plist里面添加
<key>LSApplicationQueriesSchemes</key>
<array>
	<string>alipay</string>
</array>
