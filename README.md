🛵 绿源电动车 Scriptable 小组件使用说明

此小组件适用于 iOS 上 Scriptable 应用，可显示电动车信息（如电量、续航、定位、健康状态等），无需打开官方 App。
（我的车是绿源inno7，其他车型未测试）
![IMG_6627](https://github.com/user-attachments/assets/58e366e2-f515-4ae7-9cc3-752944f53f78)
⸻

✅ 第一步：准备配置文件（配置文件需要抓包获取，具体方法可以自己搜一下）

请创建一个名为 luyuan_config.json 的配置文件，内容如下：
{
  "code16": "你的 车辆编号",
  "headers": {
    "Host": "intelligence.luyuan.cn",
    "api-sign": "你的 api-sign",
    "mocktoken": "你的 mocktoken",
    "Accept": "*/*",
    "Cookie": "你的 Cookie",
    "Connection": "keep-alive",
    "api-key": "你的 api-key",
    "User-Agent": "LY_Intelligence/版本号 (设备信息)",
    "Accept-Language": "zh-Hans-CN;q=1, en-CN;q=0.9",
    "apptoken": "你的 apptoken",
    "Accept-Encoding": "gzip, deflate, br"
  },
  "fullRangeKm": 60
}
 ![IMG_6626](https://github.com/user-attachments/assets/12262fad-6a33-4509-ae63-05a631906b12)

❗请将以上内容中 你的 ... 替换为你通过抓包获取的实际值。fullRangeKm 填写你的电池满电理论续航，如 60、70、75 不需要写km。

⸻

📥 第二步：保存配置文件 
	1.	打开 Scriptable 应用；
	2.	点击左上角 + 创建一个脚本（命名随意）；
	3.	在脚本中粘贴你得到的完整代码；
	4.	第一次运行脚本时会自动提示你将此配置粘贴并保存；
	5.	你也可以使用以下方式手动保存：
	•	将配置保存为文件 luyuan_config.json
	•	存放路径为：/iCloud Drive/Scriptable/（Scriptable 的 iCloud 目录）

⸻

📱 第三步：添加到桌面小组件
	1.	返回 iPhone 主屏；
	2.	长按空白处 → 点击左上角 + → 选择 Scriptable；
	3.	添加一个小组件，长按它选择“编辑”；
	4.	在“脚本”中选择刚才创建的脚本；
	5.	设置为中尺寸（Medium）显示最佳。

⸻

🔔 小组件功能说明
	•	🚘 车辆型号、设防状态
	•	🔋 实时电量、温度、充电次数
	•	🔧 电池健康评估（基于续航衰减）
	•	📍 车辆定位（点开跳转地图）
	•	🛞 智能预估续航（含算法估算）
	•	🕒 最近更新时间显示

⸻

💡 注意事项
	•	所有数据直接从绿源接口获取；
	•	本地仅保存一个配置文件，无隐私泄露风险；
	•	配置文件错误或接口过期会提示“❌ 数据获取失败”。

⸻

如需更新配置（例如更换车辆、token 过期），请：
	1.	删除原有 luyuan_config.json 文件；
	2.	再次运行脚本，即可重新输入保存。
