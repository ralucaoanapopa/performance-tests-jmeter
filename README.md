# Setup

1. [Install Java](https://www.java.com/en/download/help/index_installing.html)

2. Check Java is installed and set in PATH

```
java -version
```

3. Install [JMeter](https://jmeter.apache.org/download_jmeter.cgi) from binaries

4. Start JMeter from jmeter/bin: ApacheJMeter.jar file

# Run performance tests

## From command line / non-GUI mode

```
jmeter -n -t <jmeter_file.jmx> -l <location_result_file>
```

-n = execute jmeter in non gui mode
-t = location of jmeter script
-l = location of result file

# Results

# Web sites used for testing

- [Shop Demo QA](https://shop.demoqa.com/)
- [Blaze Demo](https://blazedemo.com/)
- [Ecommerce Lambda Test](https://ecommerce-playground.lambdatest.io/)

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

Listener is a component that shows the results of the samples. The results can be shown in a tree, tables, graphs or simply written to a log file

Latency = when starting to get the response

*Throughput* is a measure of how many units of work are being processed. In the case of load testing, this is usually hits per second, also known as requests per second.

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
- Blazemeter - [Chrome Plugin](https://chrome.google.com/webstore/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi/related?hl=en): can download .jmx file only when logged in
- export recorded requests from the "Network" tab from developer tools in form of *.HAR* file and convert this file into a JMeter test script using [BlazeMeter Converter](https://converter.blazemeter.com/); this is not an easy solution for website which use lots of media resources as each is logged as an entry and becomes a request in JMeter plan.

Record navigations / actions on a website then export as .jmx file.