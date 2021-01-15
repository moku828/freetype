FROM gcc:latest
RUN apt-get -y update \
 && apt-get install -y x11-apps x11-utils x11-xserver-utils dbus-x11 libxkbcommon-x11-0 bear \
 && wget -nv https://github.com/CoatiSoftware/Sourcetrail/releases/download/2020.4.35/Sourcetrail_2020_4_35_Linux_64bit.tar.gz \
 && tar zxf Sourcetrail_2020_4_35_Linux_64bit.tar.gz \
 && /Sourcetrail/install.sh \
 && rm -rf Sourcetrail_2020_4_35_Linux_64bit.tar.gz \
 && rm -rf /Sourcetrail \
 && apt-get -y clean \
 && rm -rf /var/lib/apt/lists/*
ENV DISPLAY=host.docker.internal:0.0
ENV LANG=C.UTF-8
