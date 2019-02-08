# Web App Performance Optimization
---
This guide applies only for Single Page Application (SPA)

### UX optimization (related to user psychology)
1. Show loading

1. Progressive loading. (facebook news feed example) Show mock and load content after.

1. Use AppShell [link](https://github.com/mgechev/angular-performance-checklist#use-application-shell) 
    - [Google Instant Loading Web Apps with an Application Shell Architecture](https://developers.google.com/web/updates/2015/11/app-shell)

1. Use event capturing and reproduce events after load (App shell)
    - Load script while user fills fields or read some information

### Browser optimization 

1. [Critical Path and Render Blocking Resources (CSS + JS)](https://www.keycdn.com/blog/website-performance-optimization#4-critical-path-and-render-blocking-resources-css-js)

1. No more then 7 connections to the server in the same time.
    - Inline images
    - Inline js
    - Inline css
    
1. Ordering of loading
    - Index.html
    - `<head>` async loading of css/js `deffer` for js (??)
    - why we put <script> into end of the index.htm (???)
    - http/2 file loading order (???)
    
1. Parsing js/ First paint (???)

1. [www.webpagetest.org](https://www.webpagetest.org)


### Network (size optimization)
1. Reduce HTTP Requests (time to connect with server)
    - DNS resolve(chaching DNS)
    - Inline js, html, json

1. Budgeting
    * [performance budget](http://www.performancebudget.io/)

1. Images optimization
    - JPG 80 vs JPG 100 critical/non critical
        * [tinypng](https://tinypng.com/)
        * [kraken.io](https://kraken.io/)
        * [jpegmini.com](http://www.jpegmini.com/)
    - SVG when possible
    - FontIcons vs SVG or compile your own (???)
    - Custom fonts vs SVG
    - Inline base64 vs separated files
    - Images Retina (Sprites are dead) (???)
    - webp (???)
    - Images alternative text with size `<img alt='' width='' height='' />`
    - Save with optimization (???) photoshop save as

1. Gzip one file VS. many Gzip + many bundles
    - [brotli](https://github.com/google/brotli)
    - option on the server
    
1. Caching files
    - ngnix, Apache, IIS

1. Fast delivery
    - (CDNs)[https://www.keycdn.com/blog/website-performance-optimization#5-reduce-latency-with-a-content-delivery-network-cdn] 

### Angular

1. Code minification
    - `ng build --prod`

1. Lazy loading / Preloading
    - Angular modules (??)
        * Example for login page. LoginPageModule without dependencies. UnAutorazedUser.
        * Lazy-loading + preloading stratagy (???) (link)[https://medium.com/@adrianfaciu/custom-preloading-strategy-for-angular-modules-b3b5c873681a]
        
    - Load images that only on the screen
        * [Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API)
        
1. Analyse files
    - web pack bundle anyliser (???)

### Optional. Performance optimization depends on application.

1. Delivery only what is needed
    - Reduce first bundle
    - Optimise critical pages

1. Virtual scroll

1. Reduce DOM elements
    - `<ng-container></ng-container>`

1. Web workers for highly performance calculations 
    - [Page good to be optimized with this approach](https://blog.jonlu.ca/posts/ryan-air)

1. Prefetching 
    - [angular prefetching modules from links](https://github.com/mgechev/ngx-quicklink) (???) example code
    
1. Angular
    - [*ngFor directive](https://github.com/mgechev/angular-performance-checklist#ngfor-directive)
    
    - [Run outside Angular](https://github.com/mgechev/angular-performance-checklist#run-outside-angular)
    
    - [Change Detection](https://github.com/mgechev/angular-performance-checklist#change-detection)



(???) Define types of application and provide check lists
- CRM
    - Admin panels
    - User panel
    
- Mobile application
- Landing pages
- E-shop
- Site builder


