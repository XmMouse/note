### oauth and saml openId的区别
（1）openId基于oauth实现本身完美兼容可以看成是一组
（2）oauth本身是一个授权协议，只是返回一个token支持第三方应用在不需要密码和账号的情况下使用服务-无法获取用户的具体信息
（3）openId在oauth的基础上增加返回用户其他信息的功能可以进行更加详细的验证-openid解决的是一个账号可以在多个应用中使用的问题
（4）saml协议具有上面所有功能
