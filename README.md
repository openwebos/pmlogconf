PmLogConf
=========

Notice
-------
- This comoponent is no longer needed when using PmLogLib, PmLogCtl and PmLogDaemon 3.0.0.
- The component will be removed from this repository.
- Components need not edit PmLog.conf and PmLogContext.conf to add their context information. Instead, they need to install their configration file in @WEBOS_INSTALL_SYSCONFDIR@/pmlog.d/".
<code>
<pre>
{
	"contexts" : [
		{
			"name" : "mycontext",
			"level" : "info",
			"logProcessIds" : false,
			"logThreadIds" : false,
			"logToConsole" : false,
			"rules" : [
				{ "filter" : "*.* , "output" : "stdlog" }
				{ "filter" : "kern.!info", "output" : "-stdlog" }
			]
		}
	],

	"outputs" : [
		{
			"name" : "stdlog",
			"file" : "@WEBOS_INSTALL_LOGDIR@/messages",
			"maxSize" : 2000,
			"rotations" : 5
		}
	],

	"KeyValueValidation" : true
}
</pre>
</code>

Summary
-------
Configuration files used by PmLogLib, PmLogDaemon and PmLogCtl


## Copyright and License Information

All content, including all source code files and documentation files in this repository are:

 Copyright (c) 2010-2012 Hewlett-Packard Development Company, L.P.
 Copyright (c) Copyright 2013 LG Electronics

All content, including all source code files and documentation files in this repository are:
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this content except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

