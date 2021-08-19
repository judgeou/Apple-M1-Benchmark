# Apple-M1-Benchmark

## zstd v1.5.0

### Macbook Air M1 16GB
```sh
% cc --version
Apple clang version 12.0.5 (clang-1205.0.22.11)
Target: arm64-apple-darwin20.6.0
Thread model: posix
InstalledDir: /Library/Developer/CommandLineTools/usr/bin

% ./zstd -T1 -b1 -e5 ../../lzbench/silesia.tar
 1#silesia.tar       : 211962880 ->  73495800 (2.884), 542.9 MB/s ,1446.7 MB/s 
 2#silesia.tar       : 211962880 ->  69579825 (3.046), 436.8 MB/s ,1342.9 MB/s 
 3#silesia.tar       : 211962880 ->  66664863 (3.180), 359.2 MB/s ,1325.1 MB/s 
 4#silesia.tar       : 211962880 ->  65488885 (3.237), 323.3 MB/s ,1325.3 MB/s 
 5#silesia.tar       : 211962880 ->  63793700 (3.323), 184.1 MB/s ,1287.2 MB/s
 
% ./zstd -T4 -b1 -e5 ../../lzbench/silesia.tar
 1#silesia.tar       : 211962880 ->  73584770 (2.881),1914.1 MB/s ,1445.9 MB/s 
 2#silesia.tar       : 211962880 ->  69682045 (3.042),1483.9 MB/s ,1342.5 MB/s 
 3#silesia.tar       : 211962880 ->  66740063 (3.176),1183.2 MB/s ,1298.9 MB/s 
 4#silesia.tar       : 211962880 ->  65608085 (3.231), 893.1 MB/s ,1299.0 MB/s 
 5#silesia.tar       : 211962880 ->  63889049 (3.318), 584.1 MB/s ,1262.3 MB/s
 
% ./zstd -T8 -b1 -e5 ../../lzbench/silesia.tar
 1#silesia.tar       : 211962880 ->  73584770 (2.881),2472.2 MB/s ,1439.7 MB/s 
 2#silesia.tar       : 211962880 ->  69682045 (3.042),2015.9 MB/s ,1318.2 MB/s 
 3#silesia.tar       : 211962880 ->  66740063 (3.176),1389.9 MB/s ,1298.5 MB/s 
 4#silesia.tar       : 211962880 ->  65608085 (3.231), 963.5 MB/s ,1299.6 MB/s 
 5#silesia.tar       : 211962880 ->  63889049 (3.318), 651.4 MB/s ,1262.6 MB/s
```

### Intel(R) Xeon(R) CPU E5-2603 v4 @ 1.70GHz 12core 64GB
```sh
# cc --version
cc (Ubuntu 10.1.0-2ubuntu1~18.04) 10.1.0
Copyright (C) 2020 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

# ./zstd -T1 -b1 -e5 ../../lzbench/silesia.tar
 1#silesia.tar       : 211962880 ->  73495800 (2.884), 169.8 MB/s , 567.1 MB/s 
 2#silesia.tar       : 211962880 ->  69579825 (3.046), 135.6 MB/s , 490.8 MB/s 
 3#silesia.tar       : 211962880 ->  66664863 (3.180),  99.0 MB/s , 461.3 MB/s 
 4#silesia.tar       : 211962880 ->  65488885 (3.237),  94.1 MB/s , 429.8 MB/s 
 5#silesia.tar       : 211962880 ->  63793700 (3.323),  61.0 MB/s , 437.4 MB/s 

# ./zstd -T4 -b1 -e5 ../../lzbench/silesia.tar
 1#silesia.tar       : 211962880 ->  73584770 (2.881), 612.1 MB/s , 550.3 MB/s 
 2#silesia.tar       : 211962880 ->  69682045 (3.042), 469.9 MB/s , 478.1 MB/s 
 3#silesia.tar       : 211962880 ->  66740063 (3.176), 342.3 MB/s , 462.2 MB/s 
 4#silesia.tar       : 211962880 ->  65608085 (3.231), 326.6 MB/s , 429.7 MB/s 
 5#silesia.tar       : 211962880 ->  63889049 (3.318), 215.6 MB/s , 439.9 MB/s 
 
# ./zstd -T8 -b1 -e5 ../../lzbench/silesia.tar
 1#silesia.tar       : 211962880 ->  73584770 (2.881),1053.0 MB/s , 548.3 MB/s 
 2#silesia.tar       : 211962880 ->  69682045 (3.042), 803.1 MB/s , 493.7 MB/s 
 3#silesia.tar       : 211962880 ->  66740063 (3.176), 488.7 MB/s , 461.3 MB/s 
 4#silesia.tar       : 211962880 ->  65608085 (3.231), 424.3 MB/s , 432.2 MB/s 
 5#silesia.tar       : 211962880 ->  63889049 (3.318), 317.8 MB/s , 421.9 MB/s

```

## lzbench 

```
lzbench 1.8 (64-bit MacOS)  (m1)
Assembled by P.Skibinski

Compressor name         Compress. Decompress. Compr. size  Ratio Filename
memcpy                  29792 MB/s 29863 MB/s   211962880 100.00 silesia.tar
density 0.14.2 -1        2323 MB/s  2989 MB/s   133054498  62.77 silesia.tar
density 0.14.2 -2        1009 MB/s  1540 MB/s   101641644  47.95 silesia.tar
density 0.14.2 -3         536 MB/s   598 MB/s    87649352  41.35 silesia.tar
fastlz 0.5.0 -1           362 MB/s   733 MB/s   104631274  49.36 silesia.tar
fastlz 0.5.0 -2           398 MB/s   714 MB/s   100909120  47.61 silesia.tar
lizard 1.0 -10            660 MB/s  5297 MB/s   103395318  48.78 silesia.tar
lizard 1.0 -11            479 MB/s  4951 MB/s    93880812  44.29 silesia.tar
lizard 1.0 -12            246 MB/s  4859 MB/s    86228072  40.68 silesia.tar
lizard 1.0 -13            170 MB/s  4921 MB/s    83768704  39.52 silesia.tar
lizard 1.0 -14            150 MB/s  4963 MB/s    82201394  38.78 silesia.tar
lz4 1.9.3                 691 MB/s  3877 MB/s   100883711  47.59 silesia.tar
lz4fast 1.9.3 -3          787 MB/s  3798 MB/s   107063555  50.51 silesia.tar
lz4fast 1.9.3 -17        1188 MB/s  4112 MB/s   131741552  62.15 silesia.tar
lzf 3.6 -0                399 MB/s   771 MB/s   105685269  49.86 silesia.tar
lzf 3.6 -1                393 MB/s   800 MB/s   102044344  48.14 silesia.tar
lzfse 2017-03-08          108 MB/s  1067 MB/s    67622780  31.90 silesia.tar
lzjb 2010                 369 MB/s   658 MB/s   122676119  57.88 silesia.tar
lzo1b 2.10 -1             254 MB/s   816 MB/s    97038306  45.78 silesia.tar
lzo1c 2.10 -1             261 MB/s   820 MB/s    99555162  46.97 silesia.tar
lzo1f 2.10 -1             228 MB/s   806 MB/s    99744863  47.06 silesia.tar
lzo1x 2.10 -1             589 MB/s   902 MB/s   100552614  47.44 silesia.tar
lzo1y 2.10 -1             600 MB/s   908 MB/s   101237218  47.76 silesia.tar
lzrw 15-Jul-1991 -1       280 MB/s   636 MB/s   113766411  53.67 silesia.tar
lzrw 15-Jul-1991 -3       376 MB/s   727 MB/s   105428976  49.74 silesia.tar
lzrw 15-Jul-1991 -4       412 MB/s   703 MB/s   100135668  47.24 silesia.tar
lzrw 15-Jul-1991 -5       175 MB/s   732 MB/s    90814452  42.84 silesia.tar
lzvn 2017-03-08            82 MB/s  1261 MB/s    80817022  38.13 silesia.tar
pithy 2011-12-24 -0       605 MB/s  1940 MB/s   103224325  48.70 silesia.tar
pithy 2011-12-24 -3       579 MB/s  1953 MB/s    97252492  45.88 silesia.tar
pithy 2011-12-24 -6       512 MB/s  2067 MB/s    92017637  43.41 silesia.tar
pithy 2011-12-24 -9       487 MB/s  2106 MB/s    90355341  42.63 silesia.tar
quicklz 1.5.0 -1          489 MB/s   628 MB/s    94728941  44.69 silesia.tar
quicklz 1.5.0 -2          280 MB/s   686 MB/s    84559641  39.89 silesia.tar
shrinker 0.1             1623 MB/s  5282 MB/s   160535633  75.74 silesia.tar
snappy 2020-07-11         514 MB/s  2038 MB/s   102200650  48.22 silesia.tar
tornado 0.6a -1           434 MB/s   479 MB/s   107425030  50.68 silesia.tar
tornado 0.6a -2           362 MB/s   490 MB/s    90101451  42.51 silesia.tar
tornado 0.6a -3           211 MB/s   280 MB/s    72619148  34.26 silesia.tar
zstd 1.5.0 -1             532 MB/s  1425 MB/s    73495800  34.67 silesia.tar
zstd 1.5.0 -2             430 MB/s  1320 MB/s    69579825  32.83 silesia.tar
zstd 1.5.0 -3             353 MB/s  1302 MB/s    66664863  31.45 silesia.tar
zstd 1.5.0 -4             318 MB/s  1303 MB/s    65488885  30.90 silesia.tar
zstd 1.5.0 -5             180 MB/s  1264 MB/s    63793700  30.10 silesia.tar
done... (cIters=1 dIters=1 cTime=3.0 dTime=16.0 chunkSize=1706MB cSpeed=0MB)
```

```
lzbench 1.8 (64-bit Linux)  Intel(R) Xeon(R) CPU E5-2603 v4 @ 1.70GHz
Assembled by P.Skibinski

Compressor name         Compress. Decompress. Compr. size  Ratio Filename
memcpy                   7580 MB/s  6811 MB/s   211962880 100.00 silesia.tar
density 0.14.2 -1         538 MB/s   562 MB/s   133054498  62.77 silesia.tar
density 0.14.2 -2         307 MB/s   335 MB/s   101641644  47.95 silesia.tar
density 0.14.2 -3         168 MB/s   149 MB/s    87649352  41.35 silesia.tar
fastlz 0.5.0 -1           140 MB/s   357 MB/s   104631274  49.36 silesia.tar
fastlz 0.5.0 -2           135 MB/s   353 MB/s   100909120  47.61 silesia.tar
lizard 1.0 -10            204 MB/s  1204 MB/s   103395318  48.78 silesia.tar
lizard 1.0 -11            131 MB/s  1101 MB/s    93880812  44.29 silesia.tar
lizard 1.0 -12             64 MB/s  1116 MB/s    86228072  40.68 silesia.tar
lizard 1.0 -13             40 MB/s  1132 MB/s    83768704  39.52 silesia.tar
lizard 1.0 -14             36 MB/s  1147 MB/s    82201394  38.78 silesia.tar
lz4 1.9.3                 249 MB/s  1708 MB/s   100883711  47.59 silesia.tar
lz4fast 1.9.3 -3          296 MB/s  1734 MB/s   107063555  50.51 silesia.tar
lz4fast 1.9.3 -17         450 MB/s  1903 MB/s   131741552  62.15 silesia.tar
lzf 3.6 -0                148 MB/s   319 MB/s   105685269  49.86 silesia.tar
lzf 3.6 -1                155 MB/s   326 MB/s   102044344  48.14 silesia.tar
lzfse 2017-03-08           31 MB/s   318 MB/s    67622780  31.90 silesia.tar
lzjb 2010                 143 MB/s   164 MB/s   122676119  57.88 silesia.tar
lzo1b 2.10 -1             100 MB/s   329 MB/s    97038306  45.78 silesia.tar
lzo1c 2.10 -1             105 MB/s   338 MB/s    99555162  46.97 silesia.tar
lzo1f 2.10 -1              96 MB/s   301 MB/s    99744863  47.06 silesia.tar
lzo1x 2.10 -1             248 MB/s   349 MB/s   100552614  47.44 silesia.tar
lzo1y 2.10 -1             250 MB/s   342 MB/s   101237218  47.76 silesia.tar
lzrw 15-Jul-1991 -1       119 MB/s   262 MB/s   113766411  53.67 silesia.tar
lzrw 15-Jul-1991 -3       142 MB/s   284 MB/s   105428976  49.74 silesia.tar
lzrw 15-Jul-1991 -4       146 MB/s   253 MB/s   100135668  47.24 silesia.tar
lzrw 15-Jul-1991 -5        66 MB/s   276 MB/s    90814452  42.84 silesia.tar
lzsse4fast 2019-04-18     117 MB/s  1305 MB/s    95924999  45.26 silesia.tar
lzsse8fast 2019-04-18     118 MB/s  1374 MB/s    94945126  44.79 silesia.tar
lzvn 2017-03-08            27 MB/s   454 MB/s    80817022  38.13 silesia.tar
pithy 2011-12-24 -0       236 MB/s   810 MB/s   103224325  48.70 silesia.tar
pithy 2011-12-24 -3       217 MB/s   803 MB/s    97252492  45.88 silesia.tar
pithy 2011-12-24 -6       178 MB/s   816 MB/s    92017637  43.41 silesia.tar
pithy 2011-12-24 -9       155 MB/s   815 MB/s    90355341  42.63 silesia.tar
quicklz 1.5.0 -1          209 MB/s   253 MB/s    94728941  44.69 silesia.tar
quicklz 1.5.0 -2          107 MB/s   232 MB/s    84559641  39.89 silesia.tar
shrinker 0.1              558 MB/s  1892 MB/s   160535633  75.74 silesia.tar
snappy 2020-07-11         198 MB/s   685 MB/s   102200650  48.22 silesia.tar
tornado 0.6a -1           161 MB/s   216 MB/s   107425030  50.68 silesia.tar
tornado 0.6a -2           129 MB/s   205 MB/s    90101451  42.51 silesia.tar
tornado 0.6a -3            76 MB/s   117 MB/s    72619148  34.26 silesia.tar
zstd 1.5.0 -1             171 MB/s   571 MB/s    73495800  34.67 silesia.tar
zstd 1.5.0 -2             135 MB/s   494 MB/s    69579825  32.83 silesia.tar
zstd 1.5.0 -3              99 MB/s   465 MB/s    66664863  31.45 silesia.tar
zstd 1.5.0 -4              93 MB/s   434 MB/s    65488885  30.90 silesia.tar
zstd 1.5.0 -5              61 MB/s   442 MB/s    63793700  30.10 silesia.tar
done... (cIters=1 dIters=1 cTime=3.0 dTime=16.0 chunkSize=1706MB cSpeed=0MB)
```

```
lzbench 1.8 (64-bit Linux)  Intel(R) Core(TM) i7-9700K CPU @ 3.60GHz
Assembled by P.Skibinski

Compressor name         Compress. Decompress. Compr. size  Ratio Filename
memcpy                   8383 MB/s  8236 MB/s   211962880 100.00 silesia.tar
density 0.14.2 -1        1559 MB/s  2115 MB/s   133054498  62.77 silesia.tar
density 0.14.2 -2         813 MB/s  1378 MB/s   101641644  47.95 silesia.tar
density 0.14.2 -3         434 MB/s   466 MB/s    87649352  41.35 silesia.tar
fastlz 0.5.0 -1           350 MB/s   819 MB/s   104631274  49.36 silesia.tar
fastlz 0.5.0 -2           348 MB/s   808 MB/s   100909120  47.61 silesia.tar
lizard 1.0 -10            502 MB/s  2623 MB/s   103395318  48.78 silesia.tar
lizard 1.0 -11            337 MB/s  2397 MB/s    93880812  44.29 silesia.tar
lizard 1.0 -12            166 MB/s  2463 MB/s    86228072  40.68 silesia.tar
lizard 1.0 -13            103 MB/s  2505 MB/s    83768704  39.52 silesia.tar
lizard 1.0 -14             91 MB/s  2547 MB/s    82201394  38.78 silesia.tar
lz4 1.9.3                 672 MB/s  3992 MB/s   100883711  47.59 silesia.tar
lz4fast 1.9.3 -3          764 MB/s  3988 MB/s   107063555  50.51 silesia.tar
lz4fast 1.9.3 -17        1133 MB/s  4183 MB/s   131741552  62.15 silesia.tar
lzf 3.6 -0                387 MB/s   765 MB/s   105685269  49.86 silesia.tar
lzf 3.6 -1                379 MB/s   787 MB/s   102044344  48.14 silesia.tar
lzfse 2017-03-08           63 MB/s   867 MB/s    67622780  31.90 silesia.tar
lzjb 2010                 372 MB/s   421 MB/s   122676119  57.88 silesia.tar
lzo1b 2.10 -1             251 MB/s   748 MB/s    97038306  45.78 silesia.tar
lzo1c 2.10 -1             257 MB/s   749 MB/s    99555162  46.97 silesia.tar
lzo1f 2.10 -1             228 MB/s   679 MB/s    99744863  47.06 silesia.tar
lzo1x 2.10 -1             610 MB/s   781 MB/s   100552614  47.44 silesia.tar
lzo1y 2.10 -1             613 MB/s   750 MB/s   101237218  47.76 silesia.tar
lzrw 15-Jul-1991 -1       288 MB/s   665 MB/s   113766411  53.67 silesia.tar
lzrw 15-Jul-1991 -3       353 MB/s   705 MB/s   105428976  49.74 silesia.tar
lzrw 15-Jul-1991 -4       367 MB/s   641 MB/s   100135668  47.24 silesia.tar
lzrw 15-Jul-1991 -5       167 MB/s   604 MB/s    90814452  42.84 silesia.tar
lzsse4fast 2019-04-18     305 MB/s  3603 MB/s    95924999  45.26 silesia.tar
lzsse8fast 2019-04-18     293 MB/s  3758 MB/s    94945126  44.79 silesia.tar
lzvn 2017-03-08            70 MB/s   968 MB/s    80817022  38.13 silesia.tar
pithy 2011-12-24 -0       595 MB/s  1757 MB/s   103224325  48.70 silesia.tar
pithy 2011-12-24 -3       561 MB/s  1739 MB/s    97252492  45.88 silesia.tar
pithy 2011-12-24 -6       460 MB/s  1830 MB/s    92017637  43.41 silesia.tar
pithy 2011-12-24 -9       397 MB/s  1859 MB/s    90355341  42.63 silesia.tar
quicklz 1.5.0 -1          512 MB/s   647 MB/s    94728941  44.69 silesia.tar
quicklz 1.5.0 -2          260 MB/s   695 MB/s    84559641  39.89 silesia.tar
shrinker 0.1             1355 MB/s  3636 MB/s   160535633  75.74 silesia.tar
snappy 2020-07-11         494 MB/s  1588 MB/s   102200650  48.22 silesia.tar
tornado 0.6a -1           404 MB/s   480 MB/s   107425030  50.68 silesia.tar
tornado 0.6a -2           326 MB/s   468 MB/s    90101451  42.51 silesia.tar
tornado 0.6a -3           195 MB/s   306 MB/s    72619148  34.26 silesia.tar
zstd 1.5.0 -1             455 MB/s  1486 MB/s    73495800  34.67 silesia.tar
zstd 1.5.0 -2             356 MB/s  1379 MB/s    69579825  32.83 silesia.tar
zstd 1.5.0 -3             261 MB/s  1347 MB/s    66664863  31.45 silesia.tar
zstd 1.5.0 -4             244 MB/s  1325 MB/s    65488885  30.90 silesia.tar
zstd 1.5.0 -5             174 MB/s  1305 MB/s    63793700  30.10 silesia.tar
done... (cIters=1 dIters=1 cTime=3.0 dTime=16.0 chunkSize=1706MB cSpeed=0MB)
```

```
lzbench 1.8 (64-bit Linux)  Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
Assembled by P.Skibinski

Compressor name         Compress. Decompress. Compr. size  Ratio Filename
memcpy                  14301 MB/s 14328 MB/s   211962880 100.00 silesia.tar
density 0.14.2 -1        1475 MB/s  2339 MB/s   133054498  62.77 silesia.tar
density 0.14.2 -2         715 MB/s  1171 MB/s   101641644  47.95 silesia.tar
density 0.14.2 -3         353 MB/s   362 MB/s    87649352  41.35 silesia.tar
fastlz 0.5.0 -1           268 MB/s   621 MB/s   104631274  49.36 silesia.tar
fastlz 0.5.0 -2           278 MB/s   618 MB/s   100909120  47.61 silesia.tar
lizard 1.0 -10            440 MB/s  2645 MB/s   103395318  48.78 silesia.tar
lizard 1.0 -11            289 MB/s  2468 MB/s    93880812  44.29 silesia.tar
lizard 1.0 -12            146 MB/s  2447 MB/s    86228072  40.68 silesia.tar
lizard 1.0 -13             94 MB/s  2480 MB/s    83768704  39.52 silesia.tar
lizard 1.0 -14             83 MB/s  2517 MB/s    82201394  38.78 silesia.tar
lz4 1.9.3                 528 MB/s  3317 MB/s   100883711  47.59 silesia.tar
lz4fast 1.9.3 -3          609 MB/s  3364 MB/s   107063555  50.51 silesia.tar
lz4fast 1.9.3 -17         914 MB/s  3680 MB/s   131741552  62.15 silesia.tar
lzf 3.6 -0                301 MB/s   543 MB/s   105685269  49.86 silesia.tar
lzf 3.6 -1                299 MB/s   558 MB/s   102044344  48.14 silesia.tar
lzfse 2017-03-08           43 MB/s   684 MB/s    67622780  31.90 silesia.tar
lzjb 2010                 271 MB/s   329 MB/s   122676119  57.88 silesia.tar
lzo1b 2.10 -1             185 MB/s   582 MB/s    97038306  45.78 silesia.tar
lzo1c 2.10 -1             190 MB/s   520 MB/s    99555162  46.97 silesia.tar
lzo1f 2.10 -1             147 MB/s   455 MB/s    99744863  47.06 silesia.tar
lzo1x 2.10 -1             295 MB/s   482 MB/s   100552614  47.44 silesia.tar
lzo1y 2.10 -1             315 MB/s   518 MB/s   101237218  47.76 silesia.tar
lzrw 15-Jul-1991 -1       182 MB/s   397 MB/s   113766411  53.67 silesia.tar
lzrw 15-Jul-1991 -3       228 MB/s   432 MB/s   105428976  49.74 silesia.tar
lzrw 15-Jul-1991 -4       224 MB/s   387 MB/s   100135668  47.24 silesia.tar
lzrw 15-Jul-1991 -5       100 MB/s   387 MB/s    90814452  42.84 silesia.tar
lzsse4fast 2019-04-18     161 MB/s  2463 MB/s    95924999  45.26 silesia.tar
lzsse8fast 2019-04-18     157 MB/s  2559 MB/s    94945126  44.79 silesia.tar
lzvn 2017-03-08            46 MB/s   782 MB/s    80817022  38.13 silesia.tar
pithy 2011-12-24 -0       439 MB/s  1353 MB/s   103224325  48.70 silesia.tar
pithy 2011-12-24 -3       436 MB/s  1338 MB/s    97252492  45.88 silesia.tar
pithy 2011-12-24 -6       397 MB/s  1385 MB/s    92017637  43.41 silesia.tar
pithy 2011-12-24 -9       347 MB/s  1395 MB/s    90355341  42.63 silesia.tar
quicklz 1.5.0 -1          405 MB/s   497 MB/s    94728941  44.69 silesia.tar
quicklz 1.5.0 -2          200 MB/s   476 MB/s    84559641  39.89 silesia.tar
shrinker 0.1             1068 MB/s  3701 MB/s   160535633  75.74 silesia.tar
snappy 2020-07-11         382 MB/s  1489 MB/s   102200650  48.22 silesia.tar
tornado 0.6a -1           318 MB/s   406 MB/s   107425030  50.68 silesia.tar
tornado 0.6a -2           266 MB/s   385 MB/s    90101451  42.51 silesia.tar
tornado 0.6a -3           160 MB/s   239 MB/s    72619148  34.26 silesia.tar
zstd 1.5.0 -1             364 MB/s  1204 MB/s    73495800  34.67 silesia.tar
zstd 1.5.0 -2             299 MB/s   881 MB/s    69579825  32.83 silesia.tar
zstd 1.5.0 -3             149 MB/s   847 MB/s    66664863  31.45 silesia.tar
zstd 1.5.0 -4              95 MB/s   668 MB/s    65488885  30.90 silesia.tar
zstd 1.5.0 -5              76 MB/s   807 MB/s    63793700  30.10 silesia.tar
done... (cIters=1 dIters=1 cTime=3.0 dTime=16.0 chunkSize=1706MB cSpeed=0MB)
```
