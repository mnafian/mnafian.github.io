---
layout : post
tittle: How to create good and API for backend developer and mobile developer
---
This post is just my humble opinion about how to create an accepted and good API for both developer for increasing development speed. It mean will good for backend developer as an API writer, and good for mobile developer as an API consumer. I wrote this because usually I faced a problem to dealing with backend developer about ***how is data return from server should be***, ***how is good url should be***, ***how is handle session*** and etc.

## General Principles

 - API Should Do One Thing and Do it Well
 - API Should Be As Small As Possible But No Smaller
 - Implementation Should Not Impact API
 - Minimize Accessibility of Everything
 - Names Matter–API is a Little Language
 - Documentation Matters
 - Document Religiously
 - Consider Performance Consequences of API Design Decisions
 - Effects of API Design Decisions on Performance are Real and Permanent
 - API Must Coexist Peacefully with Platform

## Class Design

 - Minimize Mutability
 - Subclass Only Where it Makes Sense 
 - Design and Document for Inheritance or Else Prohibit it

## Method Design

 - Don't Make the Client Do Anything the Module Could Do
 - Don't Violate the Principle of Least Astonishment
 - Fail Fast - Report Errors as Soon as Possible After They Occur
 - Provide Programmatic Access to All Data Available in String Form
 - Overload With Care
 - Use Appropriate Parameter and Return Types
 - Use Consistent Parameter Ordering Across Methods
 - Avoid Long Parameter Lists
 - Avoid Return Values that Demand Exceptional Processing

I found that all point from explanation by [Joshua Bloch](https://www.google.com/search?q=How+to+Design+a+Good+API+and+Why+it+Matters&gws_rd=ssl).

Happy Coding!
