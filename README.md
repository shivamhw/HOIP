#!/bin/bash
USER="ftp_user"
PASS="jFvt52jM"
#USER="demo"
#PASS="password"
#URL="test.rebex.net"
URL="10.84.129.1"
FILE="IVM01412.dat"


echo $USER $PASS
cd ~
rm IVM01412.dat


ftp -n $URL << EOF
quote USER $USER
quote PASS $PASS
cd DailyDeliveredDateReport_PROD
get $FILE
quit
EOF
