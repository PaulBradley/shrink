# shrink

`shrink` is a command-line utility which minifies HTML via streams. A HTML file is piped into the command, and minified HTML is output. Depending on the original content, the resulting HTML will be around 30% smaller. The 64-bit program works on Windows, Linux and OSX.

## usage

``` bash
./shrink < input.html > output.html
```

## shrink smaller

By default the minification is conservative as it retains document tags like `head` and keeps optional end tags like `</p>`. It also keeps javascript variable names unchanged. If you want the smallest file possible and don't mind your javascript variables being rewritten and made smaller then use the `--smallest` command line flag. This will remove default attribute values, document level tags and remove optional end tags. It will also rewrite javascript variables to smaller alternatives.

``` bash
./shrink --smallest < input.html > output.html
```

## performance

The size reduction will be dependent on the source input file. However, in the example shown below, the `output.html` file was 39% smaller than the original.

``` bash
-rw-rw-r-- 1 12010 May  1 08:46 input.html
-rw-rw-r-- 1  7473 May 19 07:12 output.html
-rw-rw-r-- 1  7430 May 19 07:12 output-smallest.html
```
