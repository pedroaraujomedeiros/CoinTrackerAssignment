# Android assignment 3

## Crypto Currency Tracker

For theis assignment you will write an app that tracks Crypto Currencies. You will implemnet the MVVM architecure we have been studying with a repositry and both persistent (Room/SQLite) storage and netwrok data (retrofit REST API). 

The starter code has most of the parts already implemented. The Network, Database, and Domain objecst are already defined for you. The starter code uses Refrofit and Moshi to consume JSON from the REST API and produces a list of Kotlin objects. 

The ViewModel get the list of coins from the network layer and displays them at application startup time. The app takes a long time to startup, because of the time it takes to get the data from the internet. You will implement a repository layer, and a database layer to act as a persistant cache and speed up start times. 

In this assignment you are to take the starter code and 

*  Implement a repository layer 
* Follow the pattern used in the DevBytesTracker codelab.
* implement a refreshCoins() method in the repository that gets the data from the network API and updates the local database. 
*  The viewModel should observe a LiveData object from the database. 
* Use workmanager to ensure that the database is refreshed every 15 min.  
  * Implemnet a refresh stratagy similar to the one used in the DevBytesTracker codelab. 
  * Create an Application class  
  * Use workmanager to refresh the data every 15 min. 



## procudure

1. Copy or fork the starter code from this repository  `https://github.com/dburchill/CoinTrackerAssignment.git`  into a public repository in your own github account. 
2. Do the assignmnet and commit on the Main branch in your repository 
3. Submit a text file to this dropbox with a link to your repository (include the commit number you want me to grade if it's not the last commit on the main branch)





The starter code uses the free tier of the ConeMarketCap API, you will need to go to [Coin Market Cap]( https://coinmarketcap.com/api/pricing/ ) and request an API Key for the free tier and change the line

 `private const val YOUR_API_KEY = "81c565ce-9f80-4d9a-816f-0e216ca23013"`

 to use your key instead of the one included in the starter file. The key in the starter file may work for a while, but there is a limited number of free requests that can be made per day wich will quickly run out if everyone uses the same key. 



### Notes

* The starter code uses the free tier of the ConeMarketCap API, you will need to go to [Coin Market Cap]( https://coinmarketcap.com/api/pricing/ ) and request an API Key for the free tier and change the line  `private const val YOUR_API_KEY = "81c565ce-9f80-4d9a-816f-0e216ca23013"` to use your key instead of the one included in the starter file. 
* The key in the starter file may work for a while, but there is a limited number of free requests that can be made per day wich will quickly run out if everyone uses the same key. 



* When writing an app that consumes an API, especily a third party API 
  * You should start by looking at the API's how to [guides](https://coinmarketcap.com/api/documentation/v1/) and using a tool like Postman to query the API and see what the JSON it returns looks like and what filter options are available. 
  * You can try out the free "JSON to Kotlin Class" plugin, you can install it from plugin marketplace from the project settings / plugins  in your Android Studio IDE.

