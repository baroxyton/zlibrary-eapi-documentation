# zlibrary-eapi-documentation
Documentation of the zlibrary android app API
# Notes
## Usage
A working, official zlibrary domain must be used. These include 1lib.fr, singlelogin.me and loginzlib2vrak5zzpcocc3ouizykn6k5qecgj2tzlnab5wcbqhembyd.onion. Requests can be sent to the endpoints and POST parameters provided here. A user agent must be provided
## Logging in
To create API requests using an account, provide a `remix-userid` header as well as a `remix-userkey` header. In some cases, it may also be necessary to provide the login as the cookies `remix_userid` and `remix_userkey`
## POST requests
The POST request body is in url encoded parameters, eg. `param1=value1&param2=value2`. Furthermore, the following request header is necessary: `Content-Type: application/x-www-form-urlencoded`. Arrays that are sent use the bracket notation, eg. `languages[]=german&languages[]=english&languages[]=french`
## Downloading
Due to recent changes, it is now necessary to use [personal zlibrary domains](https://www.bleepingcomputer.com/news/technology/z-library-now-has-secret-personal-domains-for-each-user/) to download books

# Known endpoints
    /eapi/book/most-popular (GET); query: switch-language
    
    /eapi/book/recently (GET)
    
    /eapi/user/book/recommended (GET)
    
    /eapi/user/book/{id}/delete (GET)
    
    /eapi/user/book/{bookId}/unsave (GET)
    
    /eapi/book/{id}/{hash}/formats (GET)
    
    /eapi/user/donations (GET)
    
    /eapi/user/book/downloaded (GET); query: order, page, limit
    
    /eapi/info/extensions (GET)
    
    /eapi/info/domains (GET)
    
    /eapi/info/languages (GET)
    
    /eapi/info/plans (GET); query: switchLanguage
    
    /eapi/user/book/saved (GET); query: order, page, limit
    
    /eapi/info (GET); query: switchLanguage
    
    /eapi/user/login (POST); body parameters: email, password
    
    /eapi/user/hide-banner (GET)
    
    /eapi/user/password-recovery (POST); body parameters: email
    
    /eapi/user/registration (POST); body parameters: email, password, name
    
    /eapi/user/email/confirmation/resend (POST)
    
    /eapi/user/book/{bookId}/save (GET)
    
    /eapi/book/search (POST); body parameters: message, yearFrom, yearTo, languages, extensions, e, page, limit, order
    
    /eapi/book/{id}/{hash}/send-to-{type} (GET)
    
    /eapi/book/{id}/{hash} (GET); query: switchLanguage
    
    /eapi/book/{id}/{hash}/similar (GET)
    
    /eapi/user/token-sign-in (POST); body parameters: name, id_token
    
    /eapi/user/update (POST); body parameters: email, password, name, kindle_email
    
    /eapi/user/profile (GET)
# Implementations
- Python API for Z-library by bipinkrish: https://github.com/bipinkrish/Zlibrary-API
- JS zlib-CLI by myself: https://github.com/baroxyton/zlibrary-CLI
