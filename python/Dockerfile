# Copyright 2015 tsuru authors. All rights reserved.
# Use of this source code is governed by a BSD-style
# license that can be found in the LICENSE file.

FROM	tsuru/base-platform
ADD	. /var/lib/tsuru/python
RUN	cp /var/lib/tsuru/python/deploy /var/lib/tsuru
RUN     echo "Acquire::http::Proxy 'http://dextra2:12345678@10.52.132.3:8080/'" > /etc/apt/apt.conf.d/01Proxy
RUN	/var/lib/tsuru/python/install
