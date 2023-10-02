# Tutorial

## 下载

点击 [Releases](https://github.com/moesnow/March7thAssistant/releases/latest) 打开下载页面，滚动到底部。

找到名称类似 `March7thAssistant_v1.x.x_full.zip` 的文件，点击下载。

> 如果中国大陆下载缓慢可以尝试右键上述文件，选择 "复制链接"。
>
> 然后打开其中一个加速站 https://ghproxy.com/ https://github.moeyy.cn/ ，粘贴后点击下载。

## 解压（安装）

找到下载完毕的名称类似 `March7thAssistant_v1.x.x_full.zip` 的文件，右键选择 "全部解压缩"。

## 运行

找到名称类似 `March7thAssistant_v1.x.x` 的文件夹并双击打开，里面应当至少包含以下文件（夹）：

- `March7th Launcher.exe`
- `March7th Assistant.exe`
- `Update.exe`
- `assets`
- `libraries`

双击 `March7th Launcher.exe` 打开图形界面，同意《免责声明》。

> 此程序为免费开源项目，如果你付了钱请立刻退款！！！
>
> 本项目已经因倒卖行为受到严重威胁，请帮助我们！！！
>
> 咸鱼倒狗4000+！你付给倒狗的每一分钱都会让开源自动化更艰难，请退款并举报商家！！！

## 任务

### 完整运行

按照 `日常`→`清体力`→`锄大地`→`模拟宇宙`→`忘却之庭`→`领取奖励` 的顺序依次执行

已经判断为完成的任务不会重复运行，其中日常和锄大地的重置时间为每天凌晨4点，

模拟宇宙和忘却之庭的重置时间为每周一凌晨4点。

> 模拟宇宙运行34次后才会停止，因耗时过长，执行前会额外领取奖励和清体力，执行后也会额外清体力。

### 锄大地

调用的 [Fhoe-Rail](https://github.com/linruowuyin/Fhoe-Rail) 项目，直接运行，不会判断本日是否完成过。

### 模拟宇宙

调用的 [Auto_Simulated_Universe](https://github.com/CHNZYX/Auto_Simulated_Universe) 项目，直接运行，不会判断本周是否完成过。

### 忘却之庭

直接运行，不会判断本周是否完成过。会自动识别星数，满星就会跳过执行。

## 配置

点击左下角的`设置`进入小助手设置界面。

### 程序

#### 日志等级
一般保持默认 `INFO` 即可，显示日志信息比较简洁，如果遇到异常请切换为 `DEBUG` 方便排查问题。

#### 游戏截图

可以用于自行判断程序获取的图像是否正确，也支持框选后调用OCR识别文字，可用于复制副本名称中的一些生僻字。

#### 任务完成后

任务完成后会执行的一些操作，其中`退出`指退出游戏，

`循环`指根据开拓力7×24小时无人值守循环运行程序（仅限完整运行生效），

`关机
- 休眠
- 睡眠`前会提示并等待1分钟再执行。

#### 循环运行再次启动所需开拓力

当`任务完成后`选项设置为`循环`后，该选项才会生效。

开拓力恢复到预设值后就会再次运行，凌晨4点优先级高于开拓力。

#### 优先使用 Windows 终端

使用 Windows Terminal 替换 conhost.exe （控制台主机）

### 游戏

#### 游戏路径

启动游戏后再运行小助手会自动配置该选项。

如果手动配置一定要注意不要错选成启动器 `Star Rail\launcher.exe` ，

`Star Rail\Game\StarRail.exe` 才是游戏本体。

### 体力

#### 副本类型

清体力时刷的副本类型，会自动识别开拓力计算次数，

其中"拟造花萼"默认60体力一次，可以在`config.yaml`中修改`power_needs`变更

#### 副本名称

副本名称除了用于清体力外，当每日实训中出现`完成1次「XXXX」`的任务时，

就会打这里设置的副本来完成任务，如果即使有任务也不想完成，请修改为`无`

#### 启用使用支援角色

通常只有每日实训中出现`使用支援角色并获得战斗胜利1次`任务后才会使用支援角色一次，

开启此选项后，每次打副本都会使用支援角色

#### 启用历战余响

支持自动判断历战余响剩余次数，优先级高于清体力，重置时间为每周一凌晨4点

### 锄大地

调用的 [Fhoe-Rail](https://github.com/linruowuyin/Fhoe-Rail) 项目

需要从中断的地图继续运行可以点击`原版运行`，会打开锄大地自身的界面，然后选择调试模式即可

`更新锄大地`按钮可以一键更新到最新版

### 模拟宇宙

调用的 [Auto_Simulated_Universe](https://github.com/CHNZYX/Auto_Simulated_Universe) 项目

快速上手，请访问：[项目文档](https://asu.stysqy.top/) 

遇到问题，请在提问前查看：[Q&A](https://asu.stysqy.top/guide/qa.html)

小助手使用的是 `命令行使用方法`，请确保 Python 环境变量配置正确

需要修改命途和难度等可以点击`原版运行`，会打开模拟宇宙自身的图形界面

`更新模拟宇宙`按钮可以一键更新到最新版

### 忘却之庭

修改队伍必须要按照格式，单引号不能删除。

数字代表秘技使用次数，其中`-1`代表最后一个放秘技和普攻的角色（也就是开怪角色）

角色对应的英文名字可以在 `March7thAssistant\assets\images\character` 中查看

> 目前不支持卡芙卡等同时开2个BOSS的角色

### 推送

图形界面内只支持启用`Windows原生通知`，需要其他通知请在 `config.yaml` 中添加。

目前支持：

- bark
- gocqhttp
- dingtalk
- discord
- pushplus
- pushdeer
- qmsg
- serverchan
- serverchanturbo
- smtp
- telegram
- wechatworkapp
- wechatworkbot
- lark

> 其中 Telegram 支持发送截图，欢迎 PR 适配其他推送方式

### 按键

按键设置只会在小助手内置的功能中生效，例如忘却之庭。

如果你需要修改模拟宇宙和锄大地，请查看相关项目的教程。