### 注意
**目前纯真ip免费数据库已经不再通过微信推文发布下载链接，本Repository已失效，详情见[纯真官网](https://www.cz88.com/geo-public)**

# qqwry.dat [![build](https://github.com/nmgliangwei/qqwry/actions/workflows/qqwry.yml/badge.svg)](https://github.com/nmgliangwei/qqwry/actions/workflows/qqwry.yml)
**纯真IP数据库文件，dat数据非exe安装包，使用 Github Action 定时获得最新版本的IP库文件，每天会扫描5次（10:10 12:10 17:10 20:10 23:10），当发现更新时也可以选择手动运行来获得文件。**

**特别感谢 [FW27623](https://github.com/FW27623)/[qqwry](https://github.com/FW27623/qqwry) 由于fork出现一些问题导致异常所以单独建了项目。**

**基于本仓库的dat库文件，我还制作了兼容ipip.net的IPDB格式的库文件，请关注[nmgliangwei](https://github.com/nmgliangwei)/[qqwry.ipdb](https://github.com/nmgliangwei/qqwry.ipdb)。**

**本仓库如果有帮助到您的话可以点点 [Star⭐](https://github.com/nmgliangwei/qqwry)支持下。**

# 目录说明
 1、[`qqwry.dat` ](https://raw.gitmirror.com/nmgliangwei/qqwry/main/qqwry.dat) 为最新数据直链（https://raw.gitmirror.com/nmgliangwei/qqwry/main/qqwry.dat 国内加速链，接即下即用），每次更新会覆盖之前的内容，如果想要某个时间段的历史数据可在 [` Release ` ](https://github.com/nmgliangwei/qqwry/releases) 里进行查看。

 2、`qqwry.py` 文件用于获取“纯真IP实验室”最新微信公众号推文内发布的免费IP库的下载链接  

# 感谢
-  借鉴 [HMBSbige](https://github.com/HMBSbige)/[qqwry](https://github.com/HMBSbige/qqwry) 的 `workflow` 写法
-  使用 [dscharrer](https://github.com/dscharrer)/[innoextract](https://github.com/dscharrer/innoextract) 对获取到的 exe 文件进行解包操作
-  特别感谢 [FW27623](https://github.com/FW27623)/[qqwry](https://github.com/FW27623/qqwry) 由于fork出现一些问题导致异常所以单独建了项目

# 更新点

- 在` Github Action ` 中增加定时运行和手动运行操作
- 使用 ` Python ` 来获取微信公众号推文发布的IP库更新链接
- 在` Github Action ` 中增加对已有同名 [` Release` ](https://github.com/nmgliangwei/qqwry/releases) 以及[` Tags `](https://github.com/nmgliangwei/qqwry/tags)的处理
- 在` Github Action ` 中解包 `qqwy.dat` 文件，默认上传至根目录和 Release 页面中，此外将增加哈希值校验防止重复提交
- 处理获取公众号的 dat 链接时异常问题

# 如何使用

- 首先 Fork 本仓库，然后在 [Personal access tokens (classic)](https://github.com/settings/tokens) 里创建一个 Token ，给予 `Repo` 和 `Workflow` 权限。

  <p align=center><img src="https://pic.1016.site/file/77bfb30076803ef0487a4.png" style="zoom:50%;" /></p>

  <p align=center><img src="https://pic.1016.site/file/47e907c05535b078d36c6.png" style="zoom:50%;" /></p>

- 然后打开 Fork 的仓库，点击 `Settings` ，找到`Secrets and variables` ，点击 `Actions` ，增加一个名为 `qqwry` 的`Secrets` ，将刚刚生成的 `Token` 复制进去。

  <p align=center><img src="https://pic.1016.site/file/950cf56dd4cf8fe773721.png" style="zoom:50%;" /></p>

- 然后再新建两个变量 `GIT_USERNAME` 和 `GIT_EMAIL`  ，这两个填你自己的就好了，然后保存，运行 Action ，不出意外的话你应该很快就能看到最新的IP库了。

  <p align=center><img src="https://pic.1016.site/file/e4011db8b992a5da6a28b.png" style="zoom:50%;" /></p>
