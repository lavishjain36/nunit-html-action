# NUnit HTML Report

This Github Action generates an HTML report from NUnit XML test results.

![](example.png)

## Usage

```yaml
on:
  pull_request:
  push:
jobs:
  test:
    name: Test 
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: # run your tests

      - name: Generate test report
        uses: rempelj/nunit-html-action@v1
        if: always()
        with:
          inputXmlPath: artifacts/results.xml
          
      - uses: actions/upload-artifact@v2 
      # upload your test result artifacts
```

## License

The scripts and documentation in this project are released under the MIT License
