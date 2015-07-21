Meta Refresh Conference : 16th - 17th April 2015

Yogesh Note:

Sharing my learning at the meta refresh conference, plus some of the key web technologies used by frontend developers:

###How JavaScript flow works in browser###
  - Compile the JavaScript code
  - Generate binary code
  - Interpreter interprets the binary code
  - Initialize context variable
  - Executes 
	
###Why Use JavaScript - it does below actions on browser###
 - Template (templating with less memory is the idea need to achieve)
 - Animation
 - Validation
 - Execution

###Event Bubbling - capturing###
 - Events are heavy
 - Event should be captured on propagation stage
 - All the handlers works on bubbling stage, means all the events will be available form targeted item to parent item which is not a good approach. But using addEventListener(type, method, true) we can avoid bubbling stage, which is the only way to capture the event in capturing phase.
 - We  can avoid bubbling phase using  event.cancleBubble=true for IE and event.stopProppagtion() for rest browsers
		
###Event propagation on Canvas###
 - When event fired on the canvas the browser engine initialize the event and observe the event.
 - Then call the event
 - Inline events handlers are lazy to complie
 - Never bind scroll event in Mobile web and apps. Best way is use touch start and touch end functionality.
		
###PkQuery.js###
 - Conceptual framework for data interactivity
 - Best for organize complexity around data-driven interactive Single page web/apps
	
###Component approach for building web application ###
 - Building application based on component 
 - Web component consists of 4 technology  [Custom element, html imports, templates and Shadow DOM ]
 - One of the good library is Google polymer (which follows Atomic design pattern)

###Vulcanize:###
 - This library helps in processing web components into one output file.
 - Reduces load on html file 
 - its dependent html imports into a single file
	
###Sprite.js###
 - This is a framework that let user create animation and games using sprites in effective ways.
 - This is a common framework can be used across the platform
 - Always binds and unbinds as event to the DOM element.
	
###Bracket:###
 - Adobe introduces it as a free open source code editor for web
 - Brackets open a live connection to the user's browser when live files preview is enabled.
 - Browser shows real time changes to the css class & properties , html markup as user type-
	
###Optimizing critical rendering path
 - Analyze web performance using Chrome extension
 - Use Chrome web inspector => Time line => Paint to observe the site performance
 - Add all relevant css on top inside the style tag
 - Then load the rest of the css and javascript using loadCss() and loadJS() functions.

Sudip's Note:
Day -1

###Talk 1- What’s your web? 
by Souvik Das Gupta (@souvikdg), co-founder design studio Miranj
The talk was generally focused on stats of usage of web, mobile web & its reach.

 - What does my webpage cost?
 - Need of “view desktop” version?
 - India is 2nd on the chart where users access webpage on mobile
 - “The map is not the territory” – Ethan Marcotte
 - The Web is Agreement – http://thewebisagreement.com - A collection of doodles by Paul Downey 

###Talk 2 - How I Learned to Stop Worrying and Love the Flux by Jaseem Abid (), calm.io

 - Deep dive into flux, the principles and components
 - Analyze responsibilities of each components and look at a sample implementation
 - Walk through a non-trivial example application and understand data flow and actions.
 - Show how to do common tasks like routing, error handling etc in a unidirectional data flow model.
 - Facebook’s Immutable-js 

###Talk 3 – I will JavaScript you! by Dron Rathod (), FE Developer at housing.com 

Importance of writing concise, optimized JavaScript code by deeply understanding the JS, lower level design patterns of it, and how it binds with DOM, for Mobile Web given its limitations. Neglecting JavaScript performance issues on mobile, with less memory having templating, adding a cool MVC framework blindfolded just to make ourselves comfortable is a bad attitude. A deep understanding of JavaScript engine with a topping of lower level architecture and how it binds with DOM, where does we often fail, what all things we take for granted that causes a fail for gaining performance and what all we can work upon to gain it back.

 - Events are heavy
 - Don’t load too many libraries on mobile
 - Too Many events slows down
 - skia is an open source 2D graphics library which provides common APIs that work across a variety of hardware and software platforms. It serves as the graphics engine for Google Chrome and Chrome OS, Android, Mozilla Firefox and Firefox OS, and many other products.
 - https://github.com/DronRathore/eventMan eventMan binds all of the listener at the root level.

###Talk 4 – Design for Delight by Bhaskar Chatterjee (@bhasky) , Vivek Raghavan (), Product Managers at Intuit 
[Interesting Talk]
To outline a customer driven methodology to innovate and delight the customer.In-depth look in designing a new mobile product using a very customer centric methodology call Design for Delight. Walked through techniques used to get delight and innovation, starting with understanding the customer, their motivations, testing ideas, experimentation and failing fast.

 - Know your customer than they know themselves
 - Have open ended question
 - What made the web
 - Analyze your data
 - A/B test and experiment constantly 
 - Don't build the product first, build the experience first

Flash Talk 

1. Ritvvij Parrikh (@ritvvijparrikh) on PykCharts.js and PykQuery.js  [This was a good 

talk] 

Slides: http://www.slideshare.net/ritvvijparrikh/pykqueryjs

###Talk 5 – UIs for Values by Shashi Gowda () UI for Julia programming language Flash Talk 

1. Waarta 0.2 - Open Source communication and collaboration tool

2. Why you still play games? By Jason 
 - Story, mechanics
 - Minimal
 - UI
 - Feedback
 - Art
 - Music
 - Games teach you UX

###Talk 6 – Now that we have an app, let's kill our mobile site! by Harish Sivaramakrishnan (@harish_io) [best talk]

A technical, deep, highly irreverent lowdown on how freecharge.in went ahead and built a mobile web experience, despite they have apps for all major platforms

 - Look at the data
 - Create component before UI
 - Rocket animation on freecharge using css
 - Shocking stats – After SnapDeal acquired freecharge, they found Opera mini and UC browser mini are the 2 most common browsers being used by users.
 - Common sense > Data
 - Mobile != Apps

###Day -2

###Talk 1- DOM animations almost native by Arun Subramaniam (), 

 - Mobile canvas at 60 FPS
 - Prefer requestAnimationFrame over setInterval 
 - JavaScript can effect animation
 - velocityJS, famo.us

###Talk 2- Building Application frontends the Web Components Way by Vinci Rufus ()

Components based approach to designing and developing web apps and how it can significantly help improve productivity across various streams of UX, Visual Design and Development

 - Shadow DOM, HTML import, Polymer
 - Polyfil
    - webcomponent js
	- webcomponent-light js
 - Reduce http request
 - components.io

###Talk 3 – Testing webpages across devices by Priyanka Herur (), Adobe

 - Preview and test webpages across multiple browsers, multiples devices at different screen resolutions using Edge Inspect
 - CPU, GPU & Battery can’t be emulated
 - Now Edge Inspect support multi device scrolling

###Talk 4- Optimizing the Critical Rendering Path by Brahmeshmadhav (), Sapient

 - Must optimize critical rendering path
 - Inline critical css above the fold
 - Use page insights and other tools to analyze the performance of the page

###Talk 5 - Mobile web in an app world by Wishy Arora (), Cleartrip Cleartrip’s experiences building for the mobile web. 

 - Why mobile web still matters for Cleartrip - traffic patterns, user behavior, conversion
 - Behavior differences between mobile web, apps and desktop
 - Using mobile web for customer acquisition
 - Mobile web as a testing ground for new features
 - The future of mobile web
 - You need to acquire users not traffic. Traffic is not yours.
 - True a/b test can be done only using mobile web
 - Help users create shortcuts
Obuli's Note: 
Venue : MLR convention center- Bangalore (16th and 17th April 2015) 

Just given hints taken from the sessions

###What is your web ? ###
 - W3C oneweb intiative
 - whatdomobileuserwanttodo.com
 - Map is not the teritory
 
### Flux ###
 - https://facebook.github.io/flux/
 - More of programming pattern than framework
 - Not a MVC framework
 - Uni-directional data flow
 - Data flows as : Action -> Dispatcher -> Store -> View
 - Action created by user interaction with the view (Controller View)

### JavaScript on mobile ###
 - Use fewer libraries for Mobile
 - Reduce JS data processing like JSON to HTML, instead provide redered HTML response for AJAX loading
 - Handle events in capturing phase
 
### Making maps work on mobile ###
 - https://www.mapbox.com/
 - Fast loading
 - Switch to Custom style
 - Colud based data
 
### A framework for building data-driven interactive front-ends ###
 - http://www.pykquery.com/
 - Conceptual framework
 - Data driven Interactivity
 - Useful for e-commerce like websites where vast amount of data is processed like filtering the products based on brand, color, specs etc.
 - Front-end and Back-end tightly coupled
 - Write SQL query in JSON in  browser and call the pykqueryAPI which in turn connect to DB and returns the data
 
### Now that we have an app, let's kill our mobile site! ###
 - Kill mobile site based on customer statistics
 - Free recharge, Rocket animation using CSS3

### CSS Blend Mode ###
- Apply blend effects to images similar to Photoshop
- Supports for Images, Gifs, Video, Canvas, SVG
- Support : Opera, Chrome, Safari, Spartan
- Composition & Blending (Spec)
- '@support' CSS spec

### Building application frontends the Web Components way ###
 - Web components consisting of own CSS, JS, HTML
 - Custom Elemnts, HTML Imports, HTML Template, Shadow DOM
 - Libs :  Pplymer (Google), X-Tag (Mozilla), Bosonic
 - Shadow Dom : Encapsulate CSS from rest of the page, use ::shadow for styling, JS scoped globally, JS events retargetted
 - Atomic Design Systems
 - Vulvanize npm plugin to reduce http request of multiple Web components

### Realtime Communications on Mobile ###
 - WebRTC, Peer-to-Peer communication
 - No need of server to communicate
 - Need signaling server (ex. EC2, skylink.io) to initiate the communication
 - Enterprise firewall prevents P2P
 - Not so fast
 - Multiplke commication is not efficient

### Website testing on Mobile devies ###
 - Emulators
 - Bracket
 - Adobe Edge Inspect
 - Adobe Sync Preview

### #Perffirst - Optimizing the Critical Rendering Path ###
 - Ref. High Perfomance Browser book
 - Don't render the entire page
 - Use lazyloading
 - Round Trip Render

### Mobile Web Animation ###
 - requestAnimationFrame JS API
 - using setinterval drop frames
 - Heavier DOM slower the animation
 - Enable GPU acceleration by adding 3D transform to BODY tag
 - Use DOM spirites
 - Libs : sprite.js, velocity animation, Greensock animation

Smita's Note:
Sharing my learning at the meta refresh conference, plus some of the key web technologies used by frontend developers:

###How JavaScript flow works in browser###
  - Compile the JavaScript code
  - Generate binary code
  - Interpreter interprets the binary code
  - Initialize context variable
  - Executes 
	
###Why Use JavaScript - it does below actions on browser###
 - Template (templating with less memory is the idea need to achieve)
 - Animation
 - Validation
 - Execution

###Event Bubbling - capturing###
 - Events are heavy
 - Event should be captured on propagation stage
 - All the handlers works on bubbling stage, means all the events will be available form targeted item to parent item which is not a good approach. But using addEventListener(type, method, true) we can avoid bubbling stage, which is the only way to capture the event in capturing phase.
 - We  can avoid bubbling phase using  event.cancleBubble=true for IE and event.stopProppagtion() for rest browsers
		
###Event propagation on Canvas###
 - When event fired on the canvas the browser engine initialize the event and observe the event.
 - Then call the event
 - Inline events handlers are lazy to complie
 - Never bind scroll event in Mobile web and apps. Best way is use touch start and touch end functionality.
		
###PkQuery.js###
 - Conceptual framework for data interactivity
 - Best for organize complexity around data-driven interactive Single page web/apps
	
###Component approach for building web application ###
 - Building application based on component 
 - Web component consists of 4 technology  [Custom element, html imports, templates and Shadow DOM ]
 - One of the good library is Google polymer (which follows Atomic design pattern)

###Vulcanize:###
 - This library helps in processing web components into one output file.
 - Reduces load on html file 
 - its dependent html imports into a single file
	
###Sprite.js###
 - This is a framework that let user create animation and games using sprites in effective ways.
 - This is a common framework can be used across the platform
 - Always binds and unbinds as event to the DOM element.
	
###Bracket:###
 - Adobe introduces it as a free open source code editor for web
 - Brackets open a live connection to the user's browser when live files preview is enabled.
 - Browser shows real time changes to the css class & properties , html markup as user type-
	
###Optimizing critical rendering path###
 - Analyze web performance using Chrome extension
 - Use Chrome web inspector => Time line => Paint to observe the site performance
 - Add all relevant css on top inside the style tag
 - Then load the rest of the css and javascript using loadCss() and loadJS() functions.
