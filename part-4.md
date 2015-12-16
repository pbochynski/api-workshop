# API Billioner - part 4

# Exercise - make your service more resilient

## Start service

	```
	git clone https://github.com/pbochynski/spotify
	npm install
	node index.js
    ```


## Generate some load

	```
	npm install -g bench-rest
	bench-rest -n 100 -c 50 http://localhost:3000/statistics/loadtest
	```
	
You should get results similar to these:

	```
	errors:  0
    stats:  { totalElapsed: 29966.033288002014,
      main: 
       { meter: 
          { mean: 3.337431559894907,
            count: 100,
            currentRate: 3.485550977233192,
            '1MinuteRate': 1.1500644370651443,
            '5MinuteRate': 0.27914520273452764,
            '15MinuteRate': 0.09617021080360737 },
         histogram: 
          { min: 164.28184401988983,
            max: 29920.29207599163,
            sum: 1185664.6324920058,
            variance: 70015985.43336506,
            mean: 11856.646324920059,
            stddev: 8367.55552317193,
            count: 100,
            median: 11032.140416502953,
            p75: 17089.299232020974,
            p95: 28467.981525839856,
            p99: 29914.296768491862,
            p999: 29920.29207599163 
          } 
       } 
    }
    ```
	
## Fix service

* max response time should not exceed 1 sec.
* service should survive bigger load: ```bench-rest -n 10000 -c 50```


	