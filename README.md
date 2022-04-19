# Redis <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30px">
All Abound Redis

#### LIST
- [Install 👻](#install-)
- [Error 👻](#error-)
- [Redis Server 👻](#redis-server-)
- [Redis CLI 👻](#redis-cli-)

#### INSTALL 👻
### Redis Server
    sudo apt update
    sudo apt install redis-server
    
### Restart Service
    sudo systemctl restart redis.service
    sudo systemctl status redis.service

#### ERROR 👻
### Error 203/EXEC
    Example:
    Process: 6030 ExecStart=/usr/local/bin/redis-server /etc/redis/redis.conf (code=exited, status=203/EXEC)
    
    This error because your directory is notfound
    
    Please check ExecStart directory, copy directory in terminal example:
    /usr/local/bin/redis-server
    -bash: /usr/local/bin/redis-server: No such file or directory

    you must know directory installation redis-server, in default my linux in: /usr/bin/redis-server
    
    Change service in file:  
    /etc/systemd/system/redis.service
    like this:
    ExecStart=/usr/bin/redis-server /etc/redis/redis.conf
    
    
#### REDIS SERVER 👻
#### REDIS CLI 👻
