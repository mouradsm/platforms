# Copyright 2015 tsuru authors. All rights reserved.
# Use of this source code is governed by a BSD-style
# license that can be found in the LICENSE file.

FROM    tsuru/base-platform

ENV     http_proxy="http://dextra2:12345678@10.52.132.3:8080/"
ENV     https_proxy="http://dextra2:12345678@10.52.132.3:8080/"
ENV     no_proxy="10.52.139.152, 10.52.138.95, 10.52.139.8, 10.52.137.90, 10.52.137.62, 10.52.139.51, 10.52.138.43"
RUN     echo 'Acquire::http::Proxy "http://dextra2:12345678@10.52.132.3:8080/";' >/etc/apt/apt.conf.d/01Proxy

RUN     echo 'deb http://archive.ubuntu.com/ubuntu/ vivid main restricted universe multiverse' >> /etc/apt/sources.list
RUN     echo 'deb http://archive.ubuntu.com/ubuntu/ vivid-security main restricted universe multiverse' >> /etc/apt/sources.list
RUN     echo 'APT::Default-Release "trusty";' >> /etc/apt/apt.conf.d/01ubuntu
ADD	. /var/lib/tsuru/php
RUN	cp /var/lib/tsuru/php/deploy /var/lib/tsuru
RUN	cp /var/lib/tsuru/php/interpretor/fpm5/php5_apt_preferences /etc/apt/preferences.d/php5
RUN	/var/lib/tsuru/php/install
