# 使用：
顶部设置 第二项，Hightlights, Highlight lookup words by default

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
