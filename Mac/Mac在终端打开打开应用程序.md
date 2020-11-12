### Mac在终端快速打开应用



Linux终端打开应用直接输入相应应用名字即可比如打开Chrome就输入

```shell
% google-chrome
```



而Mac不一样，要打开应用程序需要执行open命令，打开typora：

```shell
% open -a typora
```

若要打开一个 App，请使用打开命令：

```
% open -a MyProg.app
```

打开文本编辑器非常便捷，直接使用参数-e，其他默认编辑器用-t



open命令参数选项：

```shell
Options:
      -a                Opens with the specified application.
      -b                Opens with the specified application bundle identifier.
      -e                Opens with TextEdit.
      -t                Opens with default text editor.
      -f                Reads input from standard input and opens with TextEdit.
      -F  --fresh       Launches the app fresh, that is, without restoring windows. Saved persistent state is lost, excluding Untitled documents.
      -R, --reveal      Selects in the Finder instead of opening.
      -W, --wait-apps   Blocks until the used applications are closed (even if they were already running).
          --args        All remaining arguments are passed in argv to the application's main() function instead of opened.
      -n, --new         Open a new instance of the application even if one is already running.
      -j, --hide        Launches the app hidden.
      -g, --background  Does not bring the application to the foreground.
      -h, --header      Searches header file locations for headers matching the given filenames, and opens them.
      -s                For -h, the SDK to use; if supplied, only SDKs whose names contain the argument value are searched.
                        Otherwise the highest versioned SDK in each platform is used.
```

