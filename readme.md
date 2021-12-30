打包
执行以下命令，然后把import_libs下的全部内容复制到生成的dist文件加下
然后把静态资源icon文件夹复制到dist文件夹下
--windows-uac-admin 申请admin权限
```commandline
nuitka --standalone --windows-disable-console --mingw64 --show-memory --show-progress --plugin-enable=qt-plugins --include-qt-plugins=sensible,styles --plugin-enable=numpy --windows-uac-admin  --follow-import-to=lib --output-dir=out2 --windows-icon-from-ico=icon.ico TrayIcon.py
```
debug
```commandline
nuitka --standalone --mingw64 --nofollow-imports --show-memory --show-progress --plugin-enable=qt-plugins --include-qt-plugins=sensible,styles --plugin-enable=numpy  --follow-import-to=lib --output-dir=out --windows-icon-from-ico=icon.ico TrayIcon.py
```