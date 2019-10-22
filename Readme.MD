# Performance workshops setup

## Sitespeed
To perform a single run, go for:

`docker-compose run -v $(pwd)/sitespeed-config:/sitespeed.io sitespeed.io --config config.json urls.txt`

## Jmeter
To run the tests from the command line, run `jmeter -n -t [path-to-file] -l [path-to-output-csv] -e -o [path-to-web-report-directory]`

## Siege
[concise docs](https://www.linode.com/docs/tools-reference/tools/load-testing-with-siege/)

Try `siege -c 25 --time 1m -f urls.txt -l` to run a 1 minute long load test with 25 concurrent users, using urls.txt as the source of your urls, and to create a log file at the end.
