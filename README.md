### PS1
    PS1='\033[1;32m\u@\h\033[1;37m:\033[1;34m\w\033[1;37m$ '

### Logout users
    pkill -KILL -u {username}
  
### MySQL login fix
    UPDATE mysql.user SET plugin = 'mysql_native_password' WHERE user = 'root' AND plugin = 'unix_socket';
