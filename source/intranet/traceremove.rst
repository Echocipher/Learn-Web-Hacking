痕迹清理
========================================

Windows
----------------------------------------
+ 操作日志：3389登录列表、文件访问日志、浏览器日志、系统事件
+ 登录日志：系统安全日志

Linux
----------------------------------------
+ 清除历史
    + ``unset HISTORY HISTFILE HISTSAVE HISTZONE HISTORY HISTLOG; export HISTFILE=/dev/null;``
    + ``kill -9 $$`` kill history
    + ``history -c``
+ 删除 ``~/.ssh/known_hosts`` 中记录
+ 修改文件时间戳
    + ``touch –r``
+ 删除tmp目录临时文件

难点
----------------------------------------
+ 攻击和入侵很难完全删除痕迹，没有日志记录也是一种特征
+ 即使删除本地日志，在网络设备、安全设备、集中化日志系统中仍有记录
+ 留存的后门包含攻击者的信息
+ 使用的代理或跳板可能会被反向入侵

注意
----------------------------------------
+ 在操作前检查是否有用户在线
+ 删除文件使用磁盘覆写的功能删除
+ 尽量和攻击前状态保持一致
