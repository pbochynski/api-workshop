# api-workshop

# Useful tools

* [git](https://git-scm.com/downloads)
* [SourceTree](https://www.sourcetreeapp.com/)
* [JSONView chrome plugin](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc)
* [cURL](http://curl.haxx.se/latest.cgi?curl=win64-ssl-sspi)
* [Postman](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop)
* [Node.js](https://nodejs.org/en)


# First API calls

## Chuck Noris jokes

Open link in browser: [http://api.icndb.com/jokes/random](http://api.icndb.com/jokes/random)

Documentation: [http://www.icndb.com/api/](http://www.icndb.com/api/)

## Weather API

Weather in Gliwice: [http://apidev.accuweather.com/currentconditions/v1/275786.json?language=pl&apikey=meSocYcloNe](http://apidev.accuweather.com/currentconditions/v1/275786.json?language=pl&apikey=meSocYcloNe)

Documentation: [http://apidev.accuweather.com/developers/samples](http://apidev.accuweather.com/developers/samples)

## Twitter API

* Register account (if you don't have it already)
* Register app: [https://apps.twitter.com](https://apps.twitter.com)
* Get token

    ```
    curl -u consumer_key:consumer_secret -X POST -d "grant_type=client_credentials" https://api.twitter.com/oauth2/token
    ```

* Search tweets

    ```
    curl -H "Authorization: Bearer TOKEN" "https://api.twitter.com/1.1/search/tweets.json?q=%23polsl&result_type=recent"
    ```

## YaaS Product API

Follow getting started guide at [https://devportal.yaas.io/gettingstarted/](https://devportal.yaas.io/gettingstarted/)

* Get token
  
  ```
  curl -u client_id:client_secret -H "Content-Type: application/x-www-form-urlencoded" -X POST -d "grant_type=client_credentials&scope=hybris.product_view" https://api.yaas.io/hybris/oauth2/b1/token
  ```

* Get Products
  
  ```
  curl -H "Authorization: Bearer TOKEN" https://api.yaas.io/hybris/product/b1/apitest/products
  ```
  



