# SIP-CaseStudy-FreeSwitch
Read Me
To study the performance of FreeSwitch in Cloud by benchmarking 

the maximum registration rate it can handle as a SIP proxy 

server.
##FreeSwitch#SIPperformance#SIPp#SoakTest

#Host Configuration

Server: Amazon AWS T2.Micro Instance
Server: Amazon AWS T2.Small Instance
Server: Amazon AWS T2. Medium Instance
Server: Amazon AWS T2.
Operating system: Centos
Processor: Intel Xeon Processors 3.3 GHZ
Memory: 1GiB
Disk:8GB
Kernel Version:3.13.0-74-generic

#Install FreeSwitch in CentOS

rpm -ivh http://pkgs.repoforge.org/rpmforge-release/rpmforge-release-0.5.3-1.el6.rf.x86_64.rpm

yum install -y git gcc-c++ autoconf automake libtool wget python ncurses-devel zlib-devel libjpeg-devel openssl-devel e2fsprogs-devel sqlite-devel libcurl-devel pcre-devel speex-devel ldns-devel libedit-devel libxml2-devel libyuv-devel opus-devel libvpx-devel libvpx2* libdb4* libidn-devel unbound-devel libuuid-devel lua-devel libsndfile-devel yasm-devel rpm* libmudflap* libltd* build* nspr* ncurses-devel bison
git clone -b v1.6 https://freeswitch.org/stash/scm/fs/freeswitch.git

cd freeswitch

./bootstrap.sh

./configure –C 

make;make install

Files
