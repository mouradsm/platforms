# Copyright 2015 tsuru authors. All rights reserved.
# Use of this source code is governed by a BSD-style
# license that can be found in the LICENSE file.

FROM	tsuru/python
ENV     http_proxy="http://dextra2:12345678@10.52.132.3:8080/"
ENV     no_proxy="10.52.139.152, 10.52.138.95, 10.52.139.8, 10.52.137.90, 10.52.137.62, 10.52.139.51"
RUN     echo 'Acquire::http::Proxy "http://dextra2:12345678@10.52.132.3:8080/";' >/etc/apt/apt.conf.d/01Proxy
