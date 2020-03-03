# cpuminer-opt-yespowersugar-sugarchain
Optimized CPU miner yespowersugar algo for Sugarchain

**in ver 1.4 add yespowersugar algo for Sugarchain coin**  - http://cpu-pool.com/ - best pool for CPU coins

Sugarchain wallet - https://github.com/sugarchain-project/sugarchain/releases/latest

cmd for mining - Sugarchain
```css
cpuminer-sse2.exe -a yespowersugar -o stratum+tcp://cpu-pool.com:63418 -u WALLET_ADDRESS
```


Download miner for Windox x64 - https://github.com/cpu-pool/cpuminer-opt-yespowersugar-sugarchain/releases/download/1.4/cpuminer-opt-yespowersugar-sugarchain-win64.zip

Download Linux static miner - https://github.com/cpu-pool/cpuminer-opt-yespowersugar-sugarchain/releases/download/1.4/cpuminer-opt-yespowersugar-sugarchain-linux64.tar.gz

or cmd for download Linux miner
```css
wget https://github.com/cpu-pool/cpuminer-opt-cpupower/releases/download/1.4/Cpuminer-opt-cpu-pool-linux64.tar.gz && tar zxvf Cpuminer-opt-cpu-pool-linux64.tar.gz
```

cmd for auto - download and start mining *one line CMD for Linux mining* 
(replace WALLET_ADDRESS!!!)
```css
wget https://github.com/cpu-pool/cpuminer-opt-cpupower/releases/download/1.4/Cpuminer-opt-cpu-pool-linux64.tar.gz && tar zxvf Cpuminer-opt-cpu-pool-linux64.tar.gz && echo '#!/bin/sh
while [ 1 ]; do
./cpuminer -a yespowersugar -o stratum+tcp://cpu-pool.com:63418 -u WALLET_ADDRESS
done' > autominer.sh && chmod +x autominer.sh && ./autominer.sh
```


**Sugarchain mining profit calculator** - https://cpu-mining.info/?coin=12

affinity sample
---------

option: ``` --cpu-affinity=0x555```
and do not forget ```-t 6``` parametrs (6 - number of threads)

                          Good for 16 cores
                          Cores 0,1
                          0x3
                          Cores 0,1,2
                          0x7
                          Cores 0,1,2,3
                          0xF
                          Cores 0,1,2,3,4
                          0x1F
                          Cores 0,1,2,3,4,5
                          0x3F
                          Cores 0,1,2,3,4,5,6
                          0x7F
                          Cores 0,1,2,3,4,5,6,7
                          0xFF
                          Cores 0,1,2,3,4,5,6,7,8
                          0x1FF
                          Cores 0,1,2,3,4,5,6,7,8,9
                          0x3FF
                          Cores 0,1,2,3,4,5,6,7,8,9,10
                          0x7FF
                          Cores 0,1,2,3,4,5,6,7,8,9,10,11
                          0xFFF
                          Cores 0,1,2,3,4,5,6,7,8,9,10,11,12
                          0x1FFF
                          Cores 0,1,2,3,4,5,6,7,8,9,10,11,12,13
                          0x3FFF
                          Cores 0,1,2,3,4,5,6,7,8,9,10,11,12,13,14
                          0x7FFF
                          Cores 0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15
                          0xFFFF
                          
                          Windows affinity, Physical cores
                          Windows enumerates cores differently than linux.
                          Cores 0,2
                          0x5
                          Cores 0,2,4
                          0x15
                          Cores 0,2,4,6
                          0x55
                          Cores 0,2,4,6,8
                          0x155
                          Cores 0,2,4,6,8,10
                          0x555
                          Cores 0,2,4,6,8,10,12
                          0x1555
                          Cores 0,2,4,6,8,10,12,14
                          0x5555
                          Cores 0,2,4,6,8,10,12,14,16
                          0x15555
                          Cores 0,2,4,6,8,10,12,14,16,18
                          0x55555
                          Cores 0,2,4,6,8,10,12,14,16,18,20
                          0x155555
                          Cores 0,2,4,6,8,10,12,14,16,18,20,22
                          0x555555
                          Cores 0,2,4,6,8,10,12,14,16,18,20,22,24
                          0x1555555
                          Cores 0,2,4,6,8,10,12,14,16,18,20,22,24,26
                          0x5555555
                          Cores 0,2,4,6,8,10,12,14,16,18,20,22,24,26,28
                          0x15555555
                          Cores 0,2,4,6,8,10,12,14,16,18,20,22,24,26,28,30
                          0x55555555

sample for CPU 12 threads and 6 cores
```cpuminer.exe -a yespowersugar -o stratum+tcp://cpu-pool.com:63418 -u WALLET_ADDRESS -t 6 --cpu-affinity=0x555```
