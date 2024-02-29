# AoE4 World Overlay

> 简体中文翻译

### 为流媒体播放器提供的游戏信息展示工具

* 支持所有排名和快速比赛模式（1v1, 2v2等）
* 显示玩家姓名、排名、文明和胜率
* 包含所有新文明
* 可选支持自定义游戏
* 可直接在 OBS 和Streamlabs OBS中作为浏览器源使用

在[overlay.aoe4world.com](https://overlay.aoe4world.com/)获取你的叠加层。

<img width="1005" alt="CleanShot 2022-11-13 at 02 08 30@2x" src="https://user-images.githubusercontent.com/6642554/201501074-ea967231-59cb-44b4-b339-437bf741255c.png">


> **注意**
> 我们强烈建议您加入我们的[Discord](https://discord.gg/rVgtQ8n6QK)上的＃overlay频道，以获取有关新版本和更改的最新信息。这也是分享反馈或获取帮助的好地方。

---

## 设置

要获取AoE4 World Overlay，请按照[overlay.aoe4world.com](https://overlay.aoe4world.com/)上的步骤进行设置。

--- 

## 手动设置
叠加层实际上是一个可以作为浏览器源包含在流媒体软件中的个性化网页。首先，您需要创建正确的URL，然后可以将其添加为源。

#### 档案ID
叠加层的URL需要您的AoE4档案ID。您的档案ID是aoe4world.com上您的个人资料页面URL中的数字。例如，coRe的个人资料URL是https://aoe4world.com/players/7090781-coRe，因此他的档案ID是7090781。

### 默认URL
要在默认设置中使用叠加层，请将下面URL中的数字替换为您的档案ID。

```
https://overlay.aoe4world.com/profile/1234567/bar?theme=top&includeAlts=true
```

> **注意** 该URL在叠加层退出beta版后将更改。

#### 默认主题
默认行为旨在将叠加层显示在屏幕顶部，并居中显示。这样可以很好地与当前时代指示器重叠。

#### 漂浮主题
如果您想在流媒体中的任意位置显示叠加层，例如屏幕角落，可以使用漂浮主题。这将在所有四个方向上以固定宽度呈现带有圆角的叠加层。要使用漂浮主题，请将您的URL中的`theme=top`替换为`theme=floating`

##### 示例
```
https://overlay.aoe4world.com/profile/1234567/bar?theme=floating&includeAlts=true
```

<img width="932" alt="Floating Theme" src="https://user-images.githubusercontent.com/6642554/201501063-67a07b01-474b-4460-9efe-5c701b6b436a.png">


### 添加为浏览器源
一旦您有了URL，可以将其作为浏览器源添加到您的流媒体软件中，按照以下指南：

* [OBS](https://obsproject.com/wiki/Sources-Guide#browser-source)
* [Streamlabs OBS](https://blog.streamlabs.com/introducing-browser-source-interaction-for-streamlabs-obs-d8fc4dcbb1fb)

在这两种情况下，使用至少800px的宽度和400px的高度。

> **注意** 为了将叠加层正确对齐到屏幕中心，请右键单击源，然后单击“Transform -> Center Horizontally”。

### 自动隐藏行为
当您不在游戏中时，叠加层将自动隐藏。这是为了防止在大厅，主菜单或加载新游戏时显示过时的信息。

首次加载叠加层时，它将始终显示您当前/上一场比赛，以帮助您设置叠加层。

为防止在启动时显示叠加层，当切换到配置的场景时，请确保在浏览器源设置中取消选中“场景激活时刷新浏览器”选项。

---

## 关于
### Bugs & Support
Open an issue in this GitHub repo or connect with us on Discord in the [#overlay](https://discord.gg/rVgtQ8n6QK) channel.

### 贡献
We are open to contributions and feedback. If you want to contribute, please open an issue or a pull request on this GitHub repo. The stack is fairly straightforward:
- [SolidJS](https://www.solidjs.com/)
- [TailwindCSS](https://tailwindcss.com/)
- [Vite](https://vitejs.dev/)

### 其他项目
- [FluffyMaguro's AoE4 Overlay](https://github.com/FluffyMaguro/AoE4_Overlay) - 具有许多自定义选项，建造顺序和统计数据的功能丰富的本机应用程序。不仅仅是为了流媒体主！
- [Capture Age Spectator Tool](https://www.ageofempires.com/news/captureage-new-spectator-tool-ageiv/) - 用于观看/观察带有实时收入和单位统计的游戏的播放叠加层（与游戏捆绑在一起）

### 鸣谢
Build and maintained by the [AoE4 World team](https://aoe4world.com). A lot of inspiration was taken from the original 'AOEIV Overlay' by Hadmaerd.

> Age Of Empires 4 © Microsoft Corporation. AoE4 World Overlay was created under Microsoft's "Game Content Usage Rules" using assets from Age Of Empires 4, and it is not endorsed by or affiliated with Microsoft.
