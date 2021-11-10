# Performant And Accessible Angular Apps As PWAs

## Pato Vargas

### Description

As web performance and user experience across both mobile and desktop devices continue to increase in importance, so do progressive web apps (PWAs). PWAs are becoming more popular because they have lots of enhancements that help your application perform better and they make apps accessible even to users with limited internet connections. In this talk, you are going to learn the advantages of using PWAs and how to turn your Angular application into a PWA.

### Thoughts

- PWA - Progressive Web Applications. PWAs are web applications with "super powers"
  - Tinder, Microsoft, Starbucks, Google, Samsung
- [pwastats](https://www.pwastats.com/)

### PWA Super Powers

- Installability
- SEO Friendly
- Push Notiifications Friendly
- Performant
- Great User Experience
- Offline Experience
- Payment Processing
- Multiplatform

https://whatpwacando.today/

### Disadvantages

- Less access to system features than a native app
- No review standard
- Apple needs to catch up with tech

### Main Components of a PWA

- Manifest.json
  - The manifest.json is a simple JSON file in your webstie that tells the browser about your website on user's mobile device or desktop. Having a manifest is required by browser to show the Add to Home Screen prompt.
- Service Worker JS
  - A service worker is a script that is running separately from our website - in the background.
    - https://developers.google.com
    - Can cache network requests
    - Can handle how network requests are done iin your website
    - Can make the use of the Background Sync API which allows you to defer actions until the user has stable connectivity
    - Can cache things from your website, like static assets
    - Can receive push notifications when the app is not active
    - Can stay inactive when it's not in use When it gets the "signal" to be used, it reactivates again.
    - Can be used to make your app work offline.
  - Registering the Service Worker
    - check that your navigator supports the service worker
  - Installing the Service Worker
  - Intercepting Server Calls
  - Activate Service Worker
  -
- Web App
- By default you only have one service worker
- It's good practice to have your service workers living in your root directory
- Utilizing the cache can be found in the dev tools in the application tab
- `ng add @angular/pwa --project YourProjectName`
  - see picture
- ngsw-config.json
  - assetGroups
    - Assets are resources that are part of the application version that update along with the application.
    - lazy requesting strategy - you do not cache anything unless you request it first
  - dataGroups
    - data requests are not versioned along with the applications. They're cached according to manually-configured poilcies that are more useful for situations such as API requests and other data dependencies.
- https://create-react-app.dev/docs/making-a-progressive-web-app/
  - docs to set up a pwa with create react app
- The app will know that the new version is available with the cache comparison
- https://www.electronjs.org/docs/latest/api/service-workers
  - electron app service workers
