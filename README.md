## 功能

本工具可以监听微信视频号直播间的弹幕、礼物信息，并转发到指定的http地址。

- 工具只在Win64系统上发布并测试过。其他系统未测试。
- 同一个用户在不同的直播场次中，用户ID会变化。
- 可以获取到用户的点赞行为，以及直播间的点赞总数，但是无法获取单个用户精确的点赞次数。

## 使用方式

![gif2sc.gif](gif2sc.gif)

1. 点击“开始监听”按钮。
2. 浏览器会打开的视频号管理后台，用微信扫码登录。
3. 本工具上会展示出直播间的状态以及弹幕、礼物信息。
4. 设置http转发地址，将弹幕、礼物信息转发到指定地址。

## 返回数据

### 入场
```
{
	'host_info': {
		'wechat_uin': '5995',
		'finder_username': 'v2_06000023577473@finder'
	},
	'live_info': {
		'wechat_uin': '5995',
		'live_id': '204260942950',
		'online_count': 1,
		'start_time': 1703168483,
		'like_count': 0,
		'reward_total_amount_in_wecoin': '0'
	},
	'events': [{
		'msg_time': 1703169678279,
		'msg_sub_type': 10005,
		'decoded_type': 'enter',
		'msg_id': 'finderlive_sysmsg_joinlive_20426031GFSXo',
		'sec_openid': 'v8_06000fc50@flstranger',
		'content': 'bot来了',
		'nickname': 'bot',
		'seq': '12'
	}]
}
```

### 弹幕
```
{
	'host_info': {
		'wechat_uin': '5995',
		'finder_username': 'v2_060000231003b203@finder'
	},
	'live_info': {
		'wechat_uin': '5995',
		'live_id': '2042602950',
		'online_count': 1,
		'start_time': 1703168483,
		'like_count': 0,
		'reward_total_amount_in_wecoin': '0'
	},
	'events': [{
		'msg_time': 1703169491593,
		'msg_sub_type': 1,
		'decoded_type': 'comment',
		'msg_id': 'finderlive_usermsg_comment_9V1pD-9rrIJr1GFSXo',
		'sec_openid': 'v8_060000e2fc50@flstranger',
		'content': '弹幕',
		'nickname': 'bot',
		'seq': '11'
	}]
}
```

## 开发说明

### Install

Clone the repo and install dependencies:

```bash
npm install
```

### Starting Development

Start the app in the `dev` environment:

```bash
npm start
```

### Packaging for Production

To package apps for the local platform:

```bash
npm run package
```

## Donations

<img src="https://github.com/fire4nt/wxlivespy/blob/main/coffee.jpg" width="300" />


## License

MIT
