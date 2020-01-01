# 各个功能配置介绍

功能太多，按需配置

```

# 完整配置
# api_url: 接口请求地址（必填项）
# sidebar_title: 侧边栏名称
# sidebar_icon: 侧边栏图标
# show_mode: 显示模式（全屏显示: fullscreen）
# uid: 网易云音乐的用户ID
# tts_before_message: tts服务前置消息（可选）
# tts_after_message: tts服务后置消息（可选）
# mail_qq: QQ号码（可选）
# mail_code: QQ邮箱授权码（可选）
# base_url: 当前外网的地址[http://xxx.com:8123]（在使用消息提醒，功能操作时必填）
# ha_voice: 是否启用语音文字识别（默认启用）
# map_ak: 百度地图AK密钥（可选）

media_player:
  - platform: ha_cloud_music
    api_url: 'http://localhost:3000',
    sidebar_title: 云音乐
    sidebar_icon: mdi:music
    show_mode: fullscreen
    uid: 47445304
    tts_before_message: '主人：'
    tts_after_message: '。我是爱你的小喵'
    mail_qq: QQ号码（会自动加上@qq.com）
    mail_code: QQ邮箱授权码
    base_url: 外网地址（在邮件里点操作时与HA通信需要使用）
    ha_voice: true
    map_ak: 百度地图AK密钥（配置后启用百度地图）

```

## 节假日

```

binary_sensor:
  - platform: ha_cloud_music

```

## 文字转语音插件

```
# 文字转语音插件
# 注意：加在message之后加两个“。哦”可以解决vlc播放不完整的问题
# before_message: 添加在message之前的文字
# after_message: 添加在message之后的文字
tts:
  - platform: ha_cloud_music
    before_message: '主人：'
    after_message: '。我是爱你的小喵'
```