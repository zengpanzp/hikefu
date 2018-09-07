# 小程序里面的客服按钮各种样例
小程序客服接入按钮各种说明

1.普通客服按钮
```
<button type='default' open-type='contact'> 联系客服 </button>
```

2.把用户的头像和昵称传递给客服系统
```
<button type='default' session-from='{"nickName":"{{userInfo.nickName}}","avatarUrl":"{{userInfo.avatarUrl}}"}' open-type="contact" >联系客服(传递信息)</button>

```

3.直接提示用户是否发送小程序卡片
 ![image](https://github.com/agilab/hikefu/raw/master/send-message-demo.png)
```
<button send-message-title="分享标题" send-message-img="分享的单个图片链接"
show-message-card="true" send-message-path="../index/index?id={{id}}"
class='details_button' open-type='contact' plain>
  </button>
 ```


 主要用到以下几个属性
 send-message-title 分享的标题
 send-message-path 分享的路径
 send-message-img 就是上图所看到的图片
 show-message-card 显示会话内消息卡片（必须为true，不然没法分享）
 这里写图片描述


 ![image](https://github.com/agilab/hikefu/raw/master/send-message.png)

 小程序的客服消息会被发送到 [这里](https://mpkf.weixin.qq.com/)
这是一个微信官方提供的客服消息回复工具

当然您也可以选择第三方开发的系统,下面这个是我们的一个客服系统,微信小程序即可回复,有需要的可以用用看

 ![image](https://github.com/agilab/hikefu/raw/master/hi.jpg)

