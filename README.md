# MikroORM 4 vs TypeORM benchmark

This benchmark is using SQLite 3, comparing CRUD operations on 10 000 entities.

## Running

```sh
# for mikro-orm 
cd mikro-orm
yarn
yarn start
cd ..

# for typeorm 
cd typeorm
yarn
yarn start
cd ..
```

## Results

Measured on MacBook Pro 15" 2018, 2,2 GHz 6 core Intel Core i7, 16 GB RAM

### MikroORM 4.0.0-rc.5

```
➜  mikro-orm yarn start
yarn run v1.22.4
$ tsc && node --expose-gc perf
round 1
0.7575823789522909 ops/s insert 1,319.9884630143642 ms, 90.359375 MB memory
3.079504004690222 ops/s find 324.7276179790497 ms, 98.67578125 MB memory
0.8171382944686062 ops/s update 1,223.7830570042133 ms, 103.46875 MB memory
2.862082107681792 ops/s remove 349.3959859907627 ms, 107.20703125 MB memory
round 2
0.9187852418816814 ops/s insert 1,088.3936249911785 ms, 111.46875 MB memory
4.255327315516708 ops/s find 234.9995490014553 ms, 124.1484375 MB memory
0.9817556431647438 ops/s update 1,018.5833989977837 ms, 126.7421875 MB memory
3.3291832289097254 ops/s remove 300.3739750087261 ms, 128.375 MB memory
round 3
0.9924124441665777 ops/s insert 1,007.6455669999123 ms, 131.21484375 MB memory
3.9653716622665227 ops/s find 252.18317100405693 ms, 143.30859375 MB memory
0.9771941300480337 ops/s update 1,023.3381159901619 ms, 134.94140625 MB memory
3.367285039725782 ops/s remove 296.97515600919724 ms, 136.5546875 MB memory
round 4
1.002180391768816 ops/s insert 997.8243519961834 ms, 139.3671875 MB memory
4.39435386843244 ops/s find 227.56474101543427 ms, 144.203125 MB memory
0.9432723801017461 ops/s update 1,060.139171987772 ms, 138.94921875 MB memory
3.3762921606283323 ops/s remove 296.1828989982605 ms, 140.59765625 MB memory
round 5
0.99630119495989 ops/s insert 1,003.7125369906425 ms, 143.23046875 MB memory
4.4685460937971175 ops/s find 223.786435008049 ms, 146.30078125 MB memory
1.0015612396719114 ops/s update 998.44119399786 ms, 138.52734375 MB memory
3.282159812167071 ops/s remove 304.6774249970913 ms, 140.25390625 MB memory
total (avg per round) 2710.543287396431
```

## TypeORM 0.2.25

```
➜  typeorm yarn start
yarn run v1.22.4
$ tsc && node --expose-gc perf
round 1
4.525359583337206 ops/s insert 220.9769150018692 ms, 145.99609375 MB memory
0.9780044567845373 ops/s find 1,022.490227997303 ms, 379.96484375 MB memory
0.19770322345034283 ops/s update 5,058.08647197485 ms, 436.85546875 MB memory
0.22030758301770964 ops/s remove 4,539.1083970069885 ms, 194.0859375 MB memory
round 2
6.652012106967682 ops/s insert 150.33045399188995 ms, 218.6015625 MB memory
1.122793428678825 ops/s find 890.6357789933681 ms, 407.1640625 MB memory
0.20844853067715802 ops/s update 4,797.3473199903965 ms, 398.73828125 MB memory
0.20772414281625912 ops/s remove 4,814.0769120156765 ms, 399.01953125 MB memory
round 3
7.946944797305345 ops/s insert 125.83452200889587 ms, 439.30078125 MB memory
1.1203018044615551 ops/s find 892.6166110038757 ms, 624.80078125 MB memory
0.21150472972416365 ops/s update 4,728.026655972004 ms, 648.19140625 MB memory
0.2358717890250605 ops/s remove 4,239.591365009546 ms, 648.20703125 MB memory
round 4
7.925221855243086 ops/s insert 126.17943298816681 ms, 718.73046875 MB memory
1.2412288608777315 ops/s find 805.6531970202923 ms, 909.36328125 MB memory
0.2065403694243861 ops/s update 4,841.668496996164 ms, 928.71875 MB memory
0.22470917468353946 ops/s remove 4,450.196577012539 ms, 928.90234375 MB memory
round 5
4.7263743546665005 ops/s insert 211.57867002487183 ms, 915.80078125 MB memory
1.103684371160679 ops/s find 906.0561389923096 ms, 474.921875 MB memory
0.21020848176078363 ops/s update 4,757.181972980499 ms, 497.140625 MB memory
0.21929670808405316 ops/s remove 4,560.0319710075855 ms, 497.29296875 MB memory
total (avg per round) 10427.53361759782
```
