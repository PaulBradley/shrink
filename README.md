# shrink

`shrink` is a command-line utility which minifies HTML via streams. A HTML file is piped into the command, and minified HTML is output. Depending on the original content, the resulting HTML will be around 30% smaller. The 64-bit program works on Windows, Linux and OSX.

## usage

``` bash
./shrink < input.html > output.html
```

## performance

The size reduction will be dependent on the source input file. However, in the example shown below, the `output.html` was 39% smaller than the original.

``` bash
-rw-rw-r-- 1 12010 May  1 08:46 input.html
-rw-rw-r-- 1  7430 May  2 07:18 output.html
```

