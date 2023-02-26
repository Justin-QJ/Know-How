# VLC

## 1. 保存播放列表时设置默认存储路径为当前播放文件所在路径

1.1 用文本编辑应用打开 `vlc-qt-interface.ini` 配置文件，路径通常为 `...\AppData\Roaming\vlc` ，确保 VLC 应用未启动或后台运行；

1.2 查找 `[General]` 项下的 `filedialog-path` 参数，将其值设置为 `file:playlist` ；

1.3 启动 VLC 应用，上述参数的值会被自动修改为 `@Variant(\0\0\0\x11\0\0\0\rfile:playlist)` ，以后保存播放列表时对话框会自动打开当前播放文件所在路径，默认名称为 playlist ，默认名称自动获取当前播放文件名的参数代码暂未摸索出来。