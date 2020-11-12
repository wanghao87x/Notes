### 远程Linux传输文件命令scp

在本地环境向Linux服务器传输文件时使用

`scp -r localfile.txt username@192.168.0.1:/home/username/`
其中，
１）scp是命令，-r是参数
２）localfile.txt 是文件的路径和文件名
３）username是服务器账号
４）192.168.0.1是要上传的服务器ip地址
５）/home/username/是要拷入的文件夹路径



从远程服务器下载目录下载kali-linux-2017.1-amd.iso 到本地机器的当前目录。

```shell
scp test@192.168.1.103:/home/test/下载/kali-linux-2017.1-amd.iso ./
```