[![LGPLv3](https://img.shields.io/badge/license-LGPLv3-blue.svg)](https://www.gnu.org/licenses/lgpl.html) [![GPLv2+CE](https://img.shields.io/badge/license-GPLV2+CE-red.svg)](http://openjdk.java.net/legal/gplv2+ce.html) [![Gratipay Tips](https://img.shields.io/gratipay/NexusTools.svg)](https://gratipay.com/NexusTools/)

# JVM.JS
A Java to JavaScript compiler and runtime for the web, and soon NodeJS.

 - Access to JavaScript is provided either by the JSObjectRef bridge classes, or by implementing native methods with a .native.js counterpart that is loaded at runtime.
 - Java classes are compiled at runtime like a normal JVM, which would allow class modifications if someone wanted, and allows browser specific modifications by testing for features rather than guessing
 - Java bytecode is converted to a JSON format using the ASM library provided by INRIA
 - Code optimizations are performed at compile time, some only running once but some using a configurable loop
 - Many verbosity settings exist to dump everything from the stack while the code is running, to the compiled source code after compilation
 - You can supply your own JS and Java Runtimes if you wish, making this system very hackable

## [Compiler](https://github.com/NexusTools/JVM.JS-Compiler)
The Compiler module is licensed under the LGPLv3 and provides functionality via a GUI or as a library you can integrate with your own projects.

 - You can export/import your compiler configuration in json format, thanks to the gson project.
 - Loading of zipped classpaths is planned but not supported yet
 - Proguard integration is planned but not supported yet

## [JS Runtime](https://github.com/NexusTools/JVM.JS-JSRuntime)
This is where the magic happens, several low level classes such as Object, Error, Exception, Throwable and so on are implemented here, as well as the classpath and runtime compiler.

For speed and efficiency, as many low level classes and mechanisms as possible are implemented entirely in 100% JavaScript, and more may be migrated from the Java Runtime as time goes on.

## [Java Runtime](https://github.com/NexusTools/JVM.JS-JavaRuntime)
The actual Java Runtime is based on OpenJDK 6, as such this component is licensed under Oracle's revised GPLv2 with a classpath extension.

We also include in it a bridge for accessing and manipulating JavaScript objects as described above.


