# Web App Performance Optimization
---
This guide applies only for Single Page Application (SPA)

### Size optimization (Network)
1. Reduce HTTP Requests
    - Inline js, html, json

1. Budgeting
    * [performance budget](http://www.performancebudget.io/)

1. Images optimization
    - JPG 80 vs JPG 100 critical/non critical
        * [tinypng](https://tinypng.com/)
        * [kraken.io](https://kraken.io/)
        * [jpegmini.com](http://www.jpegmini.com/)
    - SVG when possible
    - FontIcons vs SVG
    - Custom fonts vs SVG
    - Inline base64 vs separated files
    - Images Retina (Sprites are dead)
    - Images alternative text with size `<img alt='' width='' height='' />`

1. Gzip vs http/2/chanking
    - [brotli](https://github.com/google/brotli)

1. Caching files
    - ngnix, Apache, IIS

1. Fast delivery
    - (CDNs)[https://www.keycdn.com/blog/website-performance-optimization#5-reduce-latency-with-a-content-delivery-network-cdn] 

1. Code minification
    - `ng build --prod`

1. Lazy loading / Preloading
    - Angular modules
        
    - Load images that only on the screen
        * [Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API)
        
1. Analyse files
    

### Browser optimization 

1. (Critical Path and Render Blocking Resources (CSS + JS))[https://www.keycdn.com/blog/website-performance-optimization#4-critical-path-and-render-blocking-resources-css-js]

1. No more then 7 connections to the server in the same time.

### UX optimization (related to user psychology)
1. Show loading

1. Add placeholders

1. Use AppShell [link](https://github.com/mgechev/angular-performance-checklist#use-application-shell) 
    - [Google Instant Loading Web Apps with an Application Shell Architecture](https://developers.google.com/web/updates/2015/11/app-shell)

1. Use event capturing and reproduce events after load

1. Load script while user fills fields or read some information

### Performance optimization

1. Delivery only what is needed
    - Reduce first bundle
    - Optimise critical pages

1. Virtual scroll

1. Reduce DOM elements
    - `<ng-container></ng-container>`

1. Web workers for highly performance calculations 
    - [Page good to be optimized with this approach](https://blog.jonlu.ca/posts/ryan-air)

1. Prefetching 
    - [angular prefetching modules from links](https://github.com/mgechev/ngx-quicklink)
    
1. Angular
    - [*ngFor directive](https://github.com/mgechev/angular-performance-checklist#ngfor-directive)
    
    - [Run outside Angular](https://github.com/mgechev/angular-performance-checklist#run-outside-angular)
    
    - [Change Detection](https://github.com/mgechev/angular-performance-checklist#change-detection)
