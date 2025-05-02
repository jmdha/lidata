# lidata
A tool to download and filter Lichess data.

## Building
> [!IMPORTANT]
> It depends on [curl](https://curl.se/libcurl/). This should already be installed on any linux distribution, but should be easy to install on windows or mac.
This tool uses [cmake](https://cmake.org/) to build.
Navigate to the directory wherein the project resides and create a build folder.
```
cmake -S . -B build
cmake --build build --config Release
```

## Using
Output of `./lidata --help`
```
Downloads Lichess data, extracts it, then inserts into local Postgres instance
Usage:
  LichessToDB [OPTION...]

  -h, --help             Print usage
  -t, --test             Runs test
  -r, --range arg        Download all months within the spcified range 
                         (default: 01/2013-01/2013)
      --temp_path arg    Temporary path for download and extraction 
                         (default: ./temp)
  -p, --path arg         Path for extracted data (default: ./data.csv)
      --min_rating arg   Minimum player rating
      --max_rating arg   Maximum player rating
      --termination arg  Allowed termination type
                         0 - Normal
                         1 - TimeForfeit
                         2 - Abandoned
                         3 - RulesInfranction
                         4 - Unterminated
``
