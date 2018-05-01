#
# Copyright 2018 Jimin Hsieh
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.


FROM azul/zulu-openjdk:8u162

ENV LANG C.UTF-8
ENV JAVA_OPTS '-XX:+UnlockExperimentalVMOptions -XX:+UseCGroupMemoryLimitForHeap'
# For regression, https://github.com/scala/scala/pull/5588
ENV JAVA_HOME /usr/lib/jvm/zulu-8-amd64

ENV SCALA_VERSION 2.11.12
ENV SBT_VERSION 0.13.17


RUN apt update && apt install -y curl && \
        export SCALA_TGZ=scala-${SCALA_VERSION}.tgz && \
        export SBT_TGZ=sbt-${SBT_VERSION}.tgz && \
        cd /opt && \
        curl -L -o ${SCALA_TGZ}  https://downloads.lightbend.com/scala/${SCALA_VERSION}/${SCALA_TGZ} && \
        tar -xf ${SCALA_TGZ}  && \
        rm ${SCALA_TGZ}  && \
        rm /opt/scala-${SCALA_VERSION}/bin/*.bat && \
        ln -s /opt/scala-${SCALA_VERSION}/bin/* /usr/local/bin && \
        curl -L -o ${SBT_TGZ}  https://github.com/sbt/sbt/releases/download/v${SBT_VERSION}/${SBT_TGZ} && \
        tar -xf ${SBT_TGZ} && \
        rm ${SBT_TGZ} && \
        rm /opt/sbt/bin/*.bat && \
        ln -s /opt/sbt/bin/sbt /usr/local/bin/sbt && \
        apt purge -y curl && apt -y autoremove && \
        sbt sbtVersion
