
#!/bin/bash
if [ $# -ge 1 ] ; then
       systemctl status $1 > /dev/null
    if [ $? -eq 0 ] ; then
       echo "$1 服务没毛病"
 else
       systemctl start $1
 fi
else
       echo "sh $0 服务吗"
