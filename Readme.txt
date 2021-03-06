Readme

This document explains the figures involved in this project as well as their specific contributions, should you need any direction. 

------------------Fabrice Bellard------------------------
Contact info: fabrice@bellard.org

QuickJS: https://bellard.org/quickjs/
Allows one to script in C using javascript
This is where one can download/compile/install quickjs, which is only 200 kilobytes. QuickJS accepts the latest specification of javascript, ES2020 (For comparison, Max’s js object only accepts a 10 year old version of Javascript, ES 5)
Documentation on quickjs exists here as well, although it is a little sparse

------------------Jerry Sievert-------------------------------
Contact info: code@legitimatesounding.com

https://github.com/VCVRack/VCV-Prototype/blob/master/src/QuickJSEngine.cpp
This code by Jerry Sievert allows the VCV Rack Protoype module to interface with quickjs
https://github.com/VCVRack/VCV-Prototype/issues/15
This appears to be the thread where Jerry Sievert discusses his impetus for creating the library in the first place. Jerry also discusses the shortcomings of the approach. 


---------------Aria Salvatrice----------------------------------
Contact info: woof@aria.dog

https://github.com/AriaSalvatrice/AriaVCVModules/blob/master/src/javascript.hpp
This is a VCV rack module that leverages the quickjs library while also bypassing the Prototype object  
This appears even simpler to understand than Jerry Sievert’s code, since it excludes a lot of boiler-plate code specific to the “Prototype” object within VCV Rack. 

https://community.vcvrack.com/t/experimenting-with-quickjs-in-my-plugin-outside-of-vcv-prototype/10321
This is the thread where Aria discusses her motivation to create such a module in the first place.

---------------------Nakul Tiruviluamala--------------------
Contact info: ntiruvil@ucsd.edu

https://docs.google.com/document/d/1XQwmG8AKvvGJIfyVIq7v66Gla4hFZuapwtkQDGPDNjU/edit
This code represents Miller Puckette and Nakul’s attempt to create a puredata external that can interface with quickjs
As of October 5th, 2020, this code has not reconciled the contributions of Jerry Sievert or Aria Salvatrice
Part of the impetus of creating this document is so that more progress can be made
Nakul Tiruviluamala has a desire to make this happen, but has a limited level of external coding proficiency
Miller Puckette has extensive proficiency in coding externals, but has limited time as well as limited experience with the quickjs interface


IoT Compatibility
My correspondence with Fabrice Bellard:
Will IoT things work also? (fetch and network requests for instance?) 
- Nakul
Provided you implement them they will work. There are examples in quickjs-libc.c.
- Fabrice














