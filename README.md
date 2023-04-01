# JMeter Performance Testing

This is a sample project for performance testing with [JMeter](https://jmeter.apache.org/).
It includes a test plan and all necessary settings to run JMeter tests.

## Overview

Performance testing gathers all the tests that verify an application’s speed, robustness, reliability, and correct sizing.
It examines several indicators such as a browser, page and network response times, server query processing time, number of acceptable concurrent users architected, CPU memory consumption, and number/type of errors which may be encountered when using an application.

The performance tests you run will help ensure your software meets the expected levels of service and provide a positive user experience.
They will highlight improvements you should make to your applications relative to speed, stability, and scalability before they go into production.
Applications released to the public in absence of testing might suffer from different types of problems that lead to a damaged brand reputation, in some cases, irrevocably.

JMeter may be used to test performance both on static and dynamic resources, Web dynamic applications.
It can be used to simulate a heavy load on a server, group of servers, network or object to test its strength or to analyze overall performance under different load types.

## Available gradle tasks

The tasks in [build.gradle](build.gradle) file were built with simplicity in mind to automate as much repetitive tasks as possible and help developers focus on what really matters.

The next tasks should be executed in a console inside the root directory:

- `./gradlew tasks` - Displays the tasks for this project.
- `./gradlew check` - Runs all checks.
- `./gradlew lint` - Checks that source code satisfies formatting steps.
- `./gradlew format` - Applies code formatting steps to source code in-place.
- `./gradlew jmGui` - Launch JMeter GUI to edit tests.
- `./gradlew jmRun` - Execute JMeter Tests.
- `./gradlew jmReport` - Create JMeter test Reports.
- `./gradlew jmClean` - Clean JMeter test Reports.
- `./gradlew clean` - Deletes the build directory.
- `./gradlew help` - Displays a help message.

For more details, read the [Command-Line Interface](https://docs.gradle.org/current/userguide/command_line_interface.html) documentation in the [Gradle User Manual](https://docs.gradle.org/current/userguide/userguide.html).

## Launching JMeter

JMeter includes an user interface that you can use to create and edit your test plans.
Test Plan is where you add elements required for your JMeter test.
It stores all the elements (like ThreadGroup, Timers etc) and their corresponding settings required to run your desired tests.

To start JMeter, you can use the next command:

```bash
./gradlew jmGui
```

After, you can create a new Test Plan or edit the [example.jmx](src/test/jmeter/example.jmx) file.

## Linting and formatting code

A linter is a static code analysis tool used to flag programming errors, bugs, stylistic errors and suspicious constructs.
This project uses [Spotless](https://github.com/diffplug/spotless) a general-purpose formatting plugin used by several projects on GitHub.

To enforce best practices, you can use the next command:

```bash
./gradlew lint
```

Many problems can be automatically fixed with `./gradlew format` command.
Depending on our editor, you may want to add an editor extension to lint and format your code while you type or on-save.

## Running performance testing

Performance testing is the practice of evaluating how a system performs in terms of responsiveness and stability under a particular workload.

To execute the performance tests, you can use the next command:

```bash
./gradlew jmRun
```

After running the performance tests, you can create the HTML report for the test results.
Use `./gradlew jmReport` to create JMeter test reports.
You can find JMeter test reports in the `build/jmeter-report` folder.

## Reference documentation

For further reference, please consider the following articles:

- [Official Gradle documentation](https://docs.gradle.org)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Git Hooks Tutorial](https://www.atlassian.com/git/tutorials/git-hooks)
- [JMeter User's Manual](https://jmeter.apache.org/usermanual/index.html)
