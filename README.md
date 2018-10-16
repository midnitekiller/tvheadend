# tvheadend
how to install tvheadend on ubuntu 14.04 lts 

apt-get install build-essential git pkg-config libssl-dev bzip2 wget libavahi-client-dev zlib1g-dev libavcodec-dev libavutil-dev libavformat-dev libswscale-dev libcurl4-gnutls-dev liburiparser-dev debhelper

git clone --branch release/4.2 https://github.com/tvheadend/tvheadend.git

AUTOBUILD_CONFIGURE_EXTRA=" --enable-hdhomerun_client --enable-avahi --enable-hdhomerun_static --enable-libffmpeg_static" ./Autobuild.sh -t precise-amd64

dpkg -i tvheadend_4.0.7-11~g398e4fe~precise_amd64.deb

service tvheadend start
