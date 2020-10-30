# Github action: Box Test

This GitHub Action runs a Commandbox + Testbox based test suite for your project.

## Usage in Github actions workflow

```yml
# .github/workflows/ci.yml

steps:
  - name: Run tests
    uses: pixl8/github-action-box-test@v3
    with:
      boxjson_dir: /subdir
      test_dir: /tests
      test_server_json: /tests/server.json
      output_file: /tests/test-results.xml
      output_format: junit
      verbose: false
```

## Inputs

### `boxjson_dir`

The subdirectory in your project where your `box.json` file lives. The default is to use the root folder. This `box.json` should define a testbox section.

### `test_dir`

Root directory of your tests. We will start a box server from here. Default is `/tests`.

### `test_server_json`

`server.json` file for your test server. Default is `${test_dir}/server.json`


### `output_file`

A file path with which to output results.


### `output_format`

Output format of results for the output file. Available formats are: json,xml,junit,antjunit,simple,dot,doc,min,mintext,doc,text,tap,codexwiki

### `verbose`

Whether or not to output all test results, or only a summary and failures. Defaults to `false` (only summary and failures).


## License

This project is licensed under the GPLv2 License - see the [LICENSE.txt](https://github.com/pixl8/github-action-box-install/blob/stable/LICENSE.txt) file for details.

## Authors

The project is maintained by [The Pixl8 Group](https://www.pixl8.co.uk). The lead developer is [Dominic Watson](https://github.com/DominicWatson).

## Code of conduct

We are a small, friendly and professional community. For the eradication of doubt, we publish a simple
 [code of conduct](https://github.com/pixl8/github-action-box-install/blob/stable/CODE_OF_CONDUCT.md) and expect all contributors, users and passers-by to observe it.
