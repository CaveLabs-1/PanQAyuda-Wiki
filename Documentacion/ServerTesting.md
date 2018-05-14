# Resultados de testing v1.0:

## Test 1

panqayuda@ubuntu-panqayuda:~$ ab -n 1000 -c 5 -C "somecookie=rawr" http://138.68.224.112/
This is ApacheBench, Version 2.3 <$Revision: 1706008 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking 138.68.224.112 (be patient)
Completed 100 requests
Completed 200 requests
Completed 300 requests
Completed 400 requests
Completed 500 requests
Completed 600 requests
Completed 700 requests
Completed 800 requests
Completed 900 requests
Completed 1000 requests
Finished 1000 requests


Server Software:        nginx/1.10.3
Server Hostname:        138.68.224.112
Server Port:            80

Document Path:          /
Document Length:        2356 bytes

Concurrency Level:      5
Time taken for tests:   3.782 seconds
Complete requests:      1000
Failed requests:        0
Non-2xx responses:      1000
Total transferred:      2545000 bytes
HTML transferred:       2356000 bytes
Requests per second:    264.39 [#/sec] (mean)
Time per request:       18.912 [ms] (mean)
Time per request:       3.782 [ms] (mean, across all concurrent requests)
Transfer rate:          657.09 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.2      0       4
Processing:     9   19   3.1     19      32
Waiting:        6   19   3.1     19      32
Total:          9   19   3.1     19      32

Percentage of the requests served within a certain time (ms)
  50%     19
  66%     20
  75%     21
  80%     21
  90%     23
  95%     24
  98%     26
  99%     27
 100%     32 (longest request)


## Test 2


panqayuda@ubuntu-panqayuda:~$ ab -kc 10 -t 30 http://138.68.224.112/
This is ApacheBench, Version 2.3 <$Revision: 1706008 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking 138.68.224.112 (be patient)
Completed 5000 requests
Finished 8194 requests


Server Software:        nginx/1.10.3
Server Hostname:        138.68.224.112
Server Port:            80

Document Path:          /
Document Length:        2356 bytes

Concurrency Level:      10
Time taken for tests:   30.001 seconds
Complete requests:      8194
Failed requests:        0
Non-2xx responses:      8194
Keep-Alive requests:    8114
Total transferred:      20894300 bytes
HTML transferred:       19305064 bytes
Requests per second:    273.12 [#/sec] (mean)
Time per request:       36.614 [ms] (mean)
Time per request:       3.661 [ms] (mean, across all concurrent requests)
Transfer rate:          680.12 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.2      0       5
Processing:    14   37   4.7     36     107
Waiting:        9   37   4.7     36     107
Total:         14   37   4.7     36     107

Percentage of the requests served within a certain time (ms)
  50%     36
  66%     38
  75%     39
  80%     40
  90%     42
  95%     45
  98%     48
  99%     52
 100%    107 (longest request)
