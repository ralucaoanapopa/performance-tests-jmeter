# Setup

1. [Install Java](https://www.java.com/en/download/help/index_installing.html)

2. Check Java is installed and set in PATH

```
java -version
```

3. Install [JMeter](https://jmeter.apache.org/download_jmeter.cgi) from binaries

4. Start JMeter from jmeter/bin: ApacheJMeter.jar file

# Run performance tests

# Results

# Notes

Thread properties:
- number of users
- ramp-up period (seconds)

*Ramp-up* is the amount of time it will take Apache JMeter™ to add all test users (threads) to a test execution. Or in other words, how long it will take for JMeter to start execution of all the threads.

## Assertions

Common Assertions
- Response Assertion
- Duration Assertion
- Size Assertion
- HTML Assertion
- XPath Assertion (used for API)

## Listeners

Listener = component that shows the results of the samples. The results can be shown in a tree, tables, graphs or simply written to a log file

Latency = when starting to get the response

*View Results Tree* should not be used for heavy load up.

*Graph Results*: usually we need to see *Average* and *Throughput*; this is also a high lead memory consumer listener, so it's not recomended to have it enabled while executing script with a heavy load.

Common Listeners
- View Results in Table
- View Results in Tree
- Aggregate Report
- Summary Report
- Graph Results
- Sample Data Writer - the only listener to use when running tests with heavy load (many users)

## Tools available for recording UI web tests and export to JMeter
- Blazemeter - [Chrome Plugin](https://chrome.google.com/webstore/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi/related?hl=en)

Record navigations / actions on a website then export as .jmx file.