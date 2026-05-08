# 识字卡

一款帮助儿童或汉语学习者学习汉字的工具应用。

## 在线访问

**访问地址：** https://lyh18926105383-cpu.github.io/Flash-Card-Chinese-character/

可在任何设备的浏览器中打开，数据自动同步。

## 使用方法

### 添加卡片
1. 点击右上角的 **+** 按钮
2. 输入汉字（一次只能输入一个）
3. 系统自动从 Wikimedia Commons 获取相关配图（支持换一批、上传自定义图片）
4. 输入组词（用空格分隔，最多3个）
5. 点击 **确认添加**

### 学习模式
- **翻转卡片**：点击卡片区域，查看背面（音频+图片+组词）
- **播放发音**：点击卡片背面的音频图标
- **切换卡片**：点击底部圆点或左右滑动（手机端支持触摸滑动）

### 编辑与删除
- 点击底部 **编辑** 按钮修改组词和图片
- 点击底部 **删除** 按钮移除卡片

## 功能特点

- 苹果简约风格界面
- 卡片 3D 翻转动画
- TTS 中文发音（点击音频图标播放）
- 自动获取配图（Wikimedia Commons）
- 支持自定义图片上传
- **云端同步**：数据保存在 Firebase Realtime Database，不同浏览器和设备自动同步
- LocalStorage 本地备份
- 手机端触摸滑动切换卡片
- 支持键盘快捷键（← → 切换卡片，空格/Enter 翻转）

## 文件结构

```
识字卡/
├── index.html      # 主程序（单文件，可直接打开）
├── README.md       # 使用说明
└── 需求文档.md      # 产品需求文档
```

## 技术说明

- 纯 HTML + CSS + JavaScript，无任何依赖
- 发音使用浏览器 Web Speech API
- 图片来源：Wikimedia Commons API（支持 CORS）
- **数据存储**：Firebase Realtime Database（云端）+ LocalStorage（离线备份）
- Firebase 配置已内置，无需额外设置

## 注意事项

- 音频功能需要浏览器支持 Web Speech API（Chrome、Safari、Edge 均支持）
- 图片加载需要网络连接，离线时显示占位图
- 首次加载需要网络连接以访问 Firebase
- localStorage 满时会自动清理旧数据，优先使用云端存储
