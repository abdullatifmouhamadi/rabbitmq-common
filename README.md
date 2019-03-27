# rabbitmq-common
Commons to use rabbitmq 


# Config
https://stackoverflow.com/questions/24610367/unable-to-start-rabbitmq-server-on-ubuntu-10-04

```
chown rabbitmq:rabbitmq /var/lib/rabbitmq/.erlang.cookie
chmod 600 /var/lib/rabbitmq/.erlang.cookie
```

## Envconf
```
nano /etc/rabbitmq/rabbitmq-env.conf


```


# Start
```
sudo systemctl start rabbitmq
sudo rabbitmqctl start_app

rabbitmqctl stop_app
```

# Engling HTTP admin
```
sudo rabbitmq-plugins enable rabbitmq_management
```

# TUTORIAL

## Create user
```
http://localhost:15672/
rabbitmqctl add_user snow snowpass
rabbitmqctl set_user_tags snow administrator
rabbitmqctl set_permissions -p / snow ".*" ".*" ".*"
```



## Create cluster
```
rabbitmqctl cluster_status
```
