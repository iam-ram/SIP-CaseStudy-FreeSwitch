# SIP-CaseStudy-FreeSwitch
Read Me
To study the performance of FreeSwitch in Cloud by benchmarking 

the maximum registration rate it can handle as a SIP proxy 

server.
##FreeSwitch#SIPperformance#SIPp#SoakTest

#Host Configuration

Server: Amazon AWS [t2.micro, t2.small, t2.medium, t2.large]

Operating system: Centos

#Install FreeSwitch in CentOS

rpm -ivh http://pkgs.repoforge.org/rpmforge-release/rpmforge-release-0.5.3-1.el6.rf.x86_64.rpm

yum install -y git gcc-c++ autoconf automake libtool wget python ncurses-devel zlib-devel libjpeg-devel openssl-devel e2fsprogs-devel sqlite-devel libcurl-devel pcre-devel speex-devel ldns-devel libedit-devel libxml2-devel libyuv-devel opus-devel libvpx-devel libvpx2* libdb4* libidn-devel unbound-devel libuuid-devel lua-devel libsndfile-devel yasm-devel rpm* libmudflap* libltd* build* nspr* ncurses-devel bison
git clone -b v1.6 https://freeswitch.org/stash/scm/fs/freeswitch.git

cd freeswitch

./bootstrap.sh

./configure –C 

make;make install

#Files
register.xml && invite.xml - Scenario files custom made to run from SIPp against the FreeSwitch Proxy Server

user.csv - CSV files used to inject along with the scenario files, includes the list of unregistered users 
