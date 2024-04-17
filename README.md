# Crosstool-NG Learning

一个仅用于学习的在线 `Crosstool-NG` 构建仓库，由 `Github Actions` 支持。

> [!WARNING]
> 本仓库的所有内容、功能及产物均为学习和研究目的而创建，请勿滥用。我们鼓励并期望这些资源能够在合法和道德的范围内被使用。
> 
> 用户在使用本仓库内容时，应自行承担相应的风险和责任。本仓库所有者及贡献者不对任何因滥用这些内容而导致的直接或间接后果承担责任。
> 此外，本仓库内容的准确性、可靠性或适用性不作任何明示或暗示的保证。

# 使用方法
1. fork 本仓库
2. clone 仓库, 编辑 crosstool-ng 配置文件. 例如使用 `ct-ng menuconfig`
3. push 到 fork 后的个人仓库
4. 前往 Actions 选项卡, 选择 `制作交叉工具链`
5. 点击 `Run Workflow` 并填写相关信息, 开始制作
6. 等待预计 40 分钟
7. 回到 Actions 选项卡, 找到刚刚运行的 Workflow Summary, 下载构建后的 artifact