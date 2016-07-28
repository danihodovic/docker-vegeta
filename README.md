# docker-vegeta

Docker image for the Vegeta HTTP load testing tool (https://github.com/tsenart/vegeta).

## Usage

Reporting to stdout

    $ docker run danihodovic/vegeta bash -c 'echo GET https://google.com | vegeta attack -duration=1s | vegeta report'
  
Reporting to a file on host and reading the report

    $ docker run -v $(pwd):/app danihodovic/vegeta bash -c 'echo GET https://google.com | vegeta attack -duration=1s > report.bin'
    $ docker run -v $(pwd):/app danihodovic/vegeta bash -c 'cat report.bin | vegeta report'

    
