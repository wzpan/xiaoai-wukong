# xiaoai-wukong

小爱音箱联动 wukong-robot 。

## demo

<https://www.bilibili.com/video/BV1eg4y1b75Y>

## 依赖安装

``` bash
pip3 install -r requirements.txt
```

## 配置

从 config.template.yml 复制一份保存为 config.yml 。然后按照注释完成配置：

``` yaml
HARDWARE: "LX05A"           # 你的小爱音箱设备型号（贴在小爱音箱底部）

MI_USER: "YOUR_ACCOUNT"  # 你的米家账号
MI_PASS: "YOUR_PASSWD"    # 你的米家密码

WUKONG_HOST: '192.168.1.7'  # wukong-robot 的服务地址
WUKONG_PORT: '5001'         # wukong-robot 的端口号
WUKONG_VALIDATE: "f4bde2a342c7c75aa276f78b26cfbd8a"  # 你的 wukong-robot validate

KEY_WORD: "问下悟空"         # 小爱联动wukong的触发词
```

其中 `HARDWARE` 是你的小爱音箱设备型号，可以在小爱音箱底部的标签里找到。

## 使用

``` bash
python3 miwukong.py
```

跑起来之后就可以问小爱同学问题了，`KEY_WORD` 开头（例如 “问下悟空”）的问题，小爱除了自己会回答之外，还会发送一份给 wukong-robot 进行解答。

> 默认用目前 ubus, 如果你的设备不支持 ubus 可以使用 --use_command 来使用 command 来 tts 。

## 致谢

项目灵感及部分代码参考了 [yihong0618/xiaogpt](https://github.com/yihong0618/xiaogpt) 。
