# Project title
Assignment — Producer/Consumer (Assignment 1) & CSV Sales Analysis (Assignment 2)

## Short description
### Assignment 1
Classic Producer–Consumer implementation in Java demonstrating thread synchronization, a bounded blocking queue, and wait/notify coordination between producer and consumer threads.
### Assignment 2
Sales data analysis in Java using Streams / functional programming. Reads a CSV and performs aggregations (grouping, sums, top-k, averages etc.) with unit tests for the analysis methods.
(Implementation languages: Java; unit tests and example mains are included in the repository.)

## Repository structure (top-level view)

```
Assignment/
  ├─ assignment1/
  │   ├─ src/
  │   │   ├─ utils/          # BoundedBlockingQueue, Producer, Consumer, etc.
  │   │   ├─ tests/          # Test harnesses / demo mains for assignment1
  │   │   └─ App.java
  │   └─ README.md
  ├─ assignment2/
  │   ├─ src/
  │   │   ├─ utils/          # SalesDataAnalyzer.java, SalesRecord.java, SalesAnalysisApp.java
  │   │   ├─ tests/          # SalesDataAnalyzerTest.java (test runner)
  │   │   └─ resources/      # sales.csv
  │   └─ README.md
  └─ README.md               # <-- this file (top-level)
```

## Prerequisites
1. JDK 11 or later recommended (the code uses core Java features compatible with Java 8+, but newer JDKs are fine).
2. Command line (Linux / macOS / Windows).
3. No external libraries required (CSV parsing uses simple parsing in the repo; see Known issues below).

## How to compile & run
### Compile and run Assignment 1 (Producer–Consumer)
  1. Compile:
```
cd Assignment/assignment1
javac -d bin src/utils/*.java src/tests/*.java
```

  2. Run the demo / tests (example):
```
java -cp bin tests.TestProducerConsumer
# or run the demo main
java -cp bin App

```

## Compile and run Assignment 2 (CSV Sales Analysis)
  1. Compile:
```
cd Assignment/assignment2
javac -d bin src/utils/*.java src/tests/*.java
```

  2. Run the analysis app:
```
java -cp bin utils.SalesAnalysisApp
# or if there's a top-level App:
java -cp bin App
```

  3. Run the test harness:
```
java -cp bin tests.SalesDataAnalyzerTest
```


## Expected outputs
1. Compilation: no output on success (javac is silent if there are no errors).
2. Running tests / apps: you should see console output from the test harness and analysis app, e.g. messages like:
   
   2.1.  Loaded N records from sales.csv
   
   2.2.  Total revenue by item: ...
   
   2.3.  top items by revenue: ...
   
   2.4.  Test pass/fail messages produced by the test harness (the project uses a simple custom harness which prints result lines).
