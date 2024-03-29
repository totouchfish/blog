# linux 命令

### 操作类

- 当前文件夹下复制文件

  `cp [需要复制的文件名称] [复制后的名称]`

- 当前文件夹下的文件重命名

  `mv [需要重命名的文件名称] [重命名后的名称]`

- mv 即可重命名又可以移动文件或者文件夹

  ```bash
  mv 旧文件/目录 新文件名/目录
  
  # 将目录A重命名为B
  mv A B
  
  #将/a目录移动到/b下，并重命名为c
  mv /a /b/c
  
  ```

  

- 当前文件夹下删除文件

  ```bash
  rm -rf 文件名/文件夹 
  ```

  

### 查看类

- 查看服务对应端口

  ```bash
  netstat -nlp
  ```

- type xx  意思是显示可执行文件xx的路径

  ~~~bash
  type nginx
  // nginx 是 /usr/sbin/nginx
  ~~~

- ls -l xx  查看xx是不是一个可执行文件

  ```bash
  ls -l /usr/sbin/nginx
  // -rwxr-xr-x. 1 root root 1373656 5月  25 2021 /usr/sbin/nginx
  ```

- find / -name xx  查找从根目录开始的所有关于xx的文件

  ```
  find / -name nginx
  /**
   	/etc/rc.d/init.d/nginx
  	/etc/logrotate.d/nginx
  	/etc/nginx
  	/var/log/nginx
  	/var/cache/nginx
  	/usr/sbin/nginx
  	/usr/lib64/nginx
  	/usr/share/nginx
  	/usr/libexec/initscripts/legacy-actions/nginx
  */
  
  ```

  

