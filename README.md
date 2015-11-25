# Curl-Latency-Diagnoser
Combination of curl options for diagnosing application latency behavior over networks

### Usage

- download the latency-print.txt to your server<br>
```curl -L -o latency-print.txt http://tinyurl.com/pllhtu2```

- replace google.com with an IP or the domainname you like to test

- Print results to screen in one second loops:<br>
```while true; do echo -n `date`; curl -sLo /dev/null -w@latency-print.txt google.com ; sleep 1; done ```

- Print results to a file(latency-results.txt) for future usage in one second loops:<br>
```while true; do echo -n `date`; curl -sLo /dev/null -w@latency-print.txt google.com ; sleep 1; done | tee latency-results.txt```
