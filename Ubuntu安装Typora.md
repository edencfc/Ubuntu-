# Ubuntu安装Typora

在Windows上使用Typora的体验较好，因此将其作为Ubutun中Markdown编辑器的首选

## [Typora官网](https://www.typora.io/#linux)下载教程

```bash
# or run:
# sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE
wget -qO - https://typora.io/linux/public-key.asc | sudo apt-key add -
# add Typora's repository
sudo add-apt-repository 'deb https://typora.io/linux ./'
sudo apt-get update
# install typora
sudo apt-get install typora
```

> 注意：不要从Ubuntu商店下载，GUI简陋且不能支持中文输入法

