---
layout: doc_page
---
<!--
    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.
-->
# Downloads

## [Signing Keys](https://downloads.apache.org/datasketches/KEYS)
It is essential that you verify the integrity of release downloads. See [instructions here.](https://www.apache.org/dyn/closer.cgi#verify)

## Latest Source Zip Files

{% include downloadsInclude.txt %}

## Download Java Jar Files
From [Maven Central](https://search.maven.org/search?q=g:%20org.apache.datasketches).

## Enabling Python
* First download the C++ core above, then read the [Python Installation Instructions](https://github.com/apache/datasketches-cpp/tree/master/python)

## Download Earlier Versions

* **[ZIP Files](http://archive.apache.org/dist/datasketches/java/)**  OR **[ZIP Files](http://archive.apache.org/dist/incubator/datasketches/java/)**
* **[Java Jar Files](https://search.maven.org/search?q=g:%20org.apache.datasketches)**

## Version Numbers
Apache DataSketches uses [semantic versioning](https://semver.org/). Version numbers use the form major.minor.incremental and are updated as follows:

* __major version__ for major new functionality and/or major API changes.  For major API changes users should expect that there may be some API-incompatible changes.  This will be made clear in the release comments. 
* __minor version__ for new functionality and scheduled bug fixes. These should be API compatible with prior versions.
* __incremental version__ for unscheduled bug fixes only.

Note: we maintain *forward binary compatiblity* of a specific sketch type.  For example, a Java Theta Sketch stored as a binary image using version 0.1.0 (Aug, 2015) can be merged into a C++ Theta Union version 1.2.0 (Jan, 2020).  The languages can be swapped in this scenario, but the versions cannot be. 

The zip files downloaded from [datasketches-xxx](https://www.apache.org/dyn/closer.cgi?path=/datasketches)
include a version number in the name, as in _apache-datasketches-java-1.1.0-src.zip_. 
This same number is also in the top section of the pom.xml file.

If you are developing using Maven and want to use, for example, datasketches-java, add the following dependencies to your pom.xml file:

```
<dependency>
  <groupId>org.apache.datasketches</groupId>
  <artifactId>datasketches-java</artifactId>
  <version>1.2.0</version>
</dependency>
```


### Release Philosophy

These are fully tested, production quality releases, and hopefully as bug-free as humanly possible. 
However, the code is continuously evolving and improvements in performance, documentation, additions 
to the API, and bug fixes do occur.  When enough of these build up, especially for bug fixes or 
performance improvements, a new release will be issued and the <b>minor</b> 
digit will be incremented.  The <b>incremental</b> digit will only be used for bug fixes as stated above.

As stated above, the <b>major</b> digit is being reserved for major refactorings of the library where backward API 
compatibility may not be guaranteed. 

For the repositories that depend on java core, such as <i>datasketches-hive</i>, 
the version number may be incremented just to be in sync with the java core repository, 
and may not reflect any actual code changes other than a change in the pom.xml to reflect the new 
dependency. 


### Version History
Please use GitHub revisions history on the respective component repositories


 
