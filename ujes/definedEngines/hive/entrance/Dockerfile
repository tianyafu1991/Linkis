#
#  Copyright 2019 WeBank
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

FROM wedatasphere/linkis:emr-base-spark2.4.4
MAINTAINER wedatasphere@webank.com

RUN yum install -y unzip
WORKDIR /opt/linkis

COPY target/linkis-ujes-hive-entrance.zip /opt/linkis
RUN unzip linkis-ujes-hive-entrance.zip

WORKDIR /opt/linkis/linkis-ujes-hive-entrance/bin
ENTRYPOINT ["/opt/linkis/linkis-ujes-hive-entrance/bin/startup.sh"]
