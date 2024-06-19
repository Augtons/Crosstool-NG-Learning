# Crosstool-NG Learning

一个仅用于学习的在线 `Crosstool-NG` 构建仓库，由 `Github Actions` 支持。

> [!WARNING]
> 本仓库的所有内容、功能及产物均为学习和研究目的而创建，请勿滥用。我们鼓励并期望这些资源能够在合法和道德的范围内被使用。
> 
> 用户在使用本仓库内容时，应自行承担相应的风险和责任。本仓库所有者及贡献者不对任何因滥用这些内容而导致的直接或间接后果承担责任。
> 此外，本仓库内容的准确性、可靠性或适用性不作任何明示或暗示的保证。

# 一、使用方法
## 1. 获取仓库

Fork 本仓库，并 Clone 到本地

> [!NOTE]
> **必须** Fork 本仓库到你的 Github 账户，否则你：
> - 既不能轻易 Push 代码以更改你的配置
> - 又不能直接在网页上触发 Workflow 的执行

## 2. 制作交叉工具链
### (1) 编辑配置文件

Clone 你 Fork 的仓库后, 编辑 `Crosstool-NG` 的配置文件. 例如：

```shell
cd ./crosstool_ng_config
ct-ng menuconfig
```

> [!NOTE]
> 注意，这一步要求你的本地电脑需要有一份 `Crosstool-NG` 命令 `ct-ng`，请自行编译安装

### (2) 推送更改

将你所做的更改 Push 到你刚刚 Fork 后的个人仓库

### (3) 运行 Workflow 以制作交叉工具链

前往 Actions 选项卡, 选择 `002. 制作 Crosstool-NG 交叉工具链`

点击 `Run Workflow` 并填写相关信息, 开始制作

> [!IMPORTANT]
> - `工具链打包名` 不影响实际工具链的特性，仅用作名称。工具链的具体特性由前文的配置决定
> - `Crosstool-NG 版本` 注意与你在本地机器更改配置所用的 Crosstool-NG **保持版本一致**
> - `指定平台` 是指最终得到的工具链所运行的平台系统，并不是交叉工具链产物所运行的系统。即该配置对应 Host 而非 Target

<img alt="Run WorkFlow" src="/docs/1_RunWorkflow.png" height=300>

### (4) 等待完成构建

该过程等待预计 40 分钟

### (5) 查看并下载
回到 Actions 选项卡, 找到刚刚运行的 Workflow Summary, 下载构建后的 artifact 即为所得工具链
