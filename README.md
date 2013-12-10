This fork has two goals:

1. Allow use on Google App Engine
2. Allow public applications via scribe oath library

The changes required were:

1. Relax visibility of some XeroClient fields for subclassing
2. Remove File I/O related PDF functions that are disallowed on GAE
3. Add protected methods to change the HTTP client and pass optional extra parameters to it when invoked.

Comments/suggestions welcome to @aschroder.



======================================

 Copyright 2011 Ross Jourdain

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.


Xero API private application access to Xero using Java
===

This is a simple project to show you how to use Java to access your Xero data via the Xero API. 
This project uses the 2-legged OAuth approach (OAuth 1.1a),
referred to by the Xero API as Private Applications.

Step 1:  Setup a Xero application

Follow the instructions here:
http://blog.xero.com/developer/api-overview/setup-an-application/#private-apps

Step 2:  Add your private key, consumer key and secret

Put your private key into: privateKey.pem
Put your consumer key and secret into: xeroApi.properties

Step 3:  Get the Schemas

Start with the modified Xero API schemas here:
https://github.com/rossjourdain/XeroAPI-Schemas

They should be up to date but if not, you can get the latest Xero API schemas here:
https://github.com/XeroAPI/XeroAPI-Schemas

Step 4:  Download this project

Step 5:  Add the schemas to src/main/resources/XeroSchemas/v2.00/

Step 6:  Build and Hack


This project uses the following projects:

-- Maven JAXB2 Plugin - XML to Java Object Unmarshalling --
http://confluence.highsource.org/display/MJIIP/Maven+JAXB2+Plugin
http://confluence.highsource.org/display/MJIIP/User+Guide

-- Java OAuth - OAuth implementation --
http://code.google.com/p/oauth/


