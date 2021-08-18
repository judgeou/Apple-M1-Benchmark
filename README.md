# Apple-M1-Benchmark

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
