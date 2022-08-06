# SASS Starter Guide
**SASS allows you to write CSS more like a dynamic programming language.**

**KEYWORDS**
* ***CSS Pre-processor / CSS ön-derleyici*** 
* ***NPM SASS module***
* ***Koala-App***
*( You can use this interfaced app for compiling Sass instead of npm sass node module. )*

**What it does SASS offer?**
```javascript
> Variables		        > Conditionals
> Nesting		        > Inheritance
> Partials / Imports		> Operators & Calculations
> Functions & Mixins		> Color Functions
```

**There are two different extension you will encounter when using SASS**
* **.scss**
* **.sass**

*.scss is usually preferred over .sass as it uses the same syntax as regular css*

**DIFFERENCES between .sass and .scss**
```scss
SASS				SCSS				CSS
$color: red                    	$color: #f00;			a {
$color2: lime			$color2: #0f0;			   color: red;		
a				a {				}
   color: $color		   color: $color;		a:hover {
   &:hover			   &:hover {			   color: lime;
      color: $color2		      color: $color2;		}
				   }
			  	}
```

## 1. Create your first sass app

**To be able to use SASS, init your package.json first.**

    npm init -y    

*"-y" means skip the questions and create the package.json with default values.*

**Install SASS module**

    npm install node-sass

**In order to use Node SASS, we also create an NPM script inside the "scripts" property which is inside the package.json file that we created**

    "sass": "node-sass -w scss/ -o dist/css"

    "-w" is a watch flag it constantly watch a folder
    "-o" refers to output dir
    "-dist" refers where basically our project is going to live 

**Eventually your code have to be like:**

    "sass": "node-sass -w scss/ -o dist/css/ --recursive"

**Finally Run SASS**

    npm run sass

***Now It's going to constantly watch the scss folder that we created and any SASS files in it and as soon as we save it will compile into dist css, which we haven't even created.***

## @Author

- LinkedIn - [Oğuzhan Kuşlar](https://www.linkedin.com/in/oguzhankuslar/)
- GitHub - [@kushadige](https://github.com/kushadige)
- Youtube - [@crabizo](https://www.youtube.com/c/crabizo)
