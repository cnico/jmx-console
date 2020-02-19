Port of old JBoss AS 5 JMX Console to Wildfly and Jboss EAP
===========

# Introduction

In JBoss AS 5 we had a web-based JMX console installed by default. It was placed in /jmx-console context. In JBoss 7 
and above (for example Wildfly) this console has been removed. 

This project contains ported old JMX console which can be started in Wildfly and Jboss EAP.

It has been tested with Jboss EAP 7.1.

# Alternatives

There are a couple of alternative tools:
* JConsole
* JVisualVM
* [Hawt.io](http://hawt.io/)
* [JBoss RHQ](https://docs.jboss.org/author/display/RHQ/Home)

# Repository layout

This repository contains 1 project:
* jmx-console WAR modules
Previous integration-tests have not been backported.

# How to install

It's really easy - just copy war into JBoss AS7/Wildfly deployment directory and you're done. Note that security is 
turned on by default. It will use `ApplicationRealm` with `jmx-console` role. 
You will have to create a user with add-user.sh script and set the correct role `jmx-console`.




