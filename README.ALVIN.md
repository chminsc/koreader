
# build
退出之后，要：
export PATH="$(brew --prefix)/opt/findutils/libexec/gnubin:$(brew --prefix)/opt/gnu-getopt/bin:$(brew --prefix)/opt/make/libexec/gnubin:$(brew --prefix)/opt/util-linux/bin:${PATH}"

export MACOSX_DEPLOYMENT_TARGET=15.2 

之后再build,run