# hpips_dag_pool_scripts

功能：此存储库包含作为池用户运行的脚本。池用户运行dag_pool守护进程本身、cron调度和nginx PHP FPM池。

计划功能：
这个自述文件不能深入到每个必要的步骤，您应该对linux/unix管理以及计算机编程的基础知识有很好的了解，并且还应该对dag_pool般如何工作以及它们的设置很熟悉。这个自述文件假设您的IP已经在主网络上被白名单化了。

完整设置:

开发环境Ubuntu 16.04，全程指令采用ROOT用户执行

1.将系统时区设置为UTC，执行sudo dpkg-figurationtzdata 并选择UTC

2.安装所有PHP7.0需求，在Ubuntu 16.04执行

sudo apt-get install php7.0-bcmath php7.0-cli php7.0-common php7.0-fpm php7.0-json php7.0-mbstring php7.0-mcrypt php7.0-mysql php7.0-opcache php7.0-readline php7.0-sqlite3 php7.0-xml php7.0-zip autoconf libtool nasm supervisor

下一步设置php.ini。设置memory_limit 至少 512M，expose_php 设置 Off ，设置 error_reporting 到 E_ALL.


