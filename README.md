#!/bin/bash
USER="ftp_user"
PASS="jFvt52jM"
#USER="demo"
#PASS="password"
#URL="test.rebex.net"
URL="10.84.129.1"
echo $USER $PASS

cd ~
rm IVM014012.dat

ftp -n $URL << EOF
quote USER $USER
quote PASS $PASS
get IVM01412.dat
quit
EOF
