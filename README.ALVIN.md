# 使用：
顶部设置 第二项，Hightlights, Highlight lookup words by default

# 为什么总是打开QuickStart：
在reader.lua中，QuickStart:isShown() 返回 false 时，程序会无视你的“start with: last file”设置，强制打开 quickstart.html。
要手动跳过 quickstart 指南，只需让 QuickStart:isShown() 返回 true。
这通常通过设置 quickstart_shown_version 为大于等于 quickstart_force_show_version 实现。
要把 settings.reader.lua中的 ["quickstart_shown_version"]改得比quickstart.lua中的local QuickStart = {
quickstart_force_show_version = 2021070000,
}的值大就可以了。

# build
退出之后，要：
export PATH="$(brew --prefix)/opt/findutils/libexec/gnubin:$(brew --prefix)/opt/gnu-getopt/bin:$(brew --prefix)/opt/make/libexec/gnubin:$(brew --prefix)/opt/util-linux/bin:${PATH}"

export MACOSX_DEPLOYMENT_TARGET=15.2 

之后再:
./kodev build
./kodev run

# sign

使用 uber-apk-signer（开源 GUI + CLI）

如果你想要 更简单的方式（无需命令行），可以使用 uber-apk-signer，它是一个 支持 GUI 的自动签名工具。

🛠 安装 uber-apk-signer
wget https://github.com/patrickfav/uber-apk-signer/releases/download/v1.2.1/uber-apk-signer-1.2.1.jar

然后使用 Java 运行：
java -jar uber-apk-signer-1.2.1.jar --apks your_app.apk

注：
在我的docker lxd ubuntu中，这个jar位于/home/ubuntu下
