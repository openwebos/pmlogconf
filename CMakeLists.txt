# @@@LICENSE
#
#      Copyright (c) 2010-2012 Hewlett-Packard Development Company, L.P.
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
#
# LICENSE@@@

#
# PmLogConf/CMakeLists.txt
#

cmake_minimum_required(VERSION 2.8.7)

project(PmLogConf NONE)

include(webOS/webOS)
webos_modules_init(1 0 0 QUALIFIER RC3)
webos_component(2 0 0)

if(WEBOS_CONFIG_LOGGING_TERSE)
	webos_build_configured_file(etc/PmLog.conf.terse SYSCONFDIR PmLog)
	webos_build_configured_file(etc/PmLogContexts.conf.terse SYSCONFDIR PmLog)

elseif(WEBOS_CONFIG_LOGGING_SDK)
	webos_build_configured_file(etc/PmLog.conf.sdk SYSCONFDIR PmLog)
	webos_build_configured_file(etc/PmLogContexts.conf.sdk SYSCONFDIR PmLog)

else()
	webos_build_configured_file(etc/PmLog.conf SYSCONFDIR PmLog)
	webos_build_configured_file(etc/PmLogContexts.conf SYSCONFDIR PmLog)
endif()
