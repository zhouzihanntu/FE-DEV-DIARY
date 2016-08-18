#CSS Design Pattern

* avoid using element selector
* avoid using group selector
* consider amount and import order of external files
* naming convention

##Patterns

###OOCSS 
Object Oriented CSS

seperating structure from skin and container from content

###SMACSS
Scalable and Modular Architecture for CSS
* Base
* Layout
* Module
* State
* Theme

###Meta CSS
no-semantic naming convention, these low-readablity classes with their predefined rules will only be applied to elements when necessary, the code can be redundant sometimes but the thought of separating out universal rules could be taken as an example.

    .mt10{
      margin-top: 10px;
    }
    .f10{
      font-size: 10px;
    }
  
###BEM
* Block
* Element
* Modifier

readable naming convention:

    .block{}
    .block__element{}
    .block--modifier{}
