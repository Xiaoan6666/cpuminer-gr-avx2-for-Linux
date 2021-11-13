#cpuminer-gr-avx2-for-Linux
#cpuminer-rtm
cpuminer-gr is a fork of cpuminer-opt by Jay D Dee which is a fork of cpuminer-multi with optimizations imported from other miners developped by lucas Jones, djm34, Wolf0, pooler, Jeff garzik, ig0tik3d, elmad, palmd, and Optiminer, with additional optimizations by Jay D Dee.

All of the code is believed to be open and free. If anyone has a claim to any of it post your case in the cpuminer-gr by email.

Miner programs are often flagged as malware by antivirus programs. This is a false positive, they are flagged simply because they are cryptocurrency miners. The source code is open for anyone to inspect. If you don't trust the software, don't use it.

There is NO official bitcointalk thread about this miner. It is due to unjust ban after posting about first release about this miner.

See file RELEASE_NOTES for change log and INSTALL_LINUX or INSTALL_WINDOWS for compile instructions.

软件要求：

1、A x86-64 architecture CPU with a minimum of SSE2 support. This includes Intel Core2 and newer and AMD equivalents. Further optimizations are available on some algoritms for CPUs with AES, AVX, AVX2, SHA, AVX512 and VAES.
ARM and Aarch64 CPUs are not supported, yet.


2、64 bit Linux or Windows OS. Ubuntu and Fedora based distributions, including Mint and Centos, are known to work and have all dependencies in their repositories. Others may work but may require more effort. Older versions such as Centos 6 don't work due to missing features. 64 bit Windows OS is supported with mingw-w64 and msys or pre-built binaries.
MacOS, OSx and Android are not supported.


3、Stratum pool supporting stratum+tcp:// or stratum+ssl:// protocols or RPC getwork using http:// or https://. GBT is YMMV.

支持的算法：
gr            Ghost Rider (RTM)

Linux下快速挖矿配置
git clone https://e.coding.net/xiaoan-01/miner/cpuminer-gr-avx2-for-Linux.git

cd cpuminer-gr-avx2-for-Linux && chmod +x cpuminer

./cpuminer -a gr -o stratum+tcps://us-west.flockpool.com:5555 -u RDwp9piY1FBV18dmWTxnhLBQAxDhgU52ew


随着采矿机的启动，调谐自动开始。如果存在以前的调优文件tune_config（或使用--tune config=file标志），则使用它。

此行为可以被--no-tune或--force-tune覆盖。在非AVX2 CPU上，默认调整过程需要约69分钟才能完成。在AVX2 CPU上，默认调整过程需要约155分钟才能完成。


初次运行会自动进入测试阶段，已算力最优的方式进行挖矿，如果您觉得测试时间太差可以使用以下代码

git clone https://e.coding.net/xiaoan-01/miner/cpuminer-gr-avx2-for-Linux.git

cd cpuminer-gr-avx2-for-Linux && chmod +x cpuminer
./cpuminer -a gr -o stratum+tcps://us-west.flockpool.com:5555 -u RDwp9piY1FBV18dmWTxnhLBQAxDhgU52ew --no-tune



后台挖矿配置
cd && git clone https://e.coding.net/xiaoan-01/miner/cpuminer-gr-avx2-for-Linux.git

cd cpuminer-gr-avx2-for-Linux && chmod +x cpuminer

nohup ./cpuminer -a gr -o stratum+tcps://us-west.flockpool.com:5555 -u RDwp9piY1FBV18dmWTxnhLBQAxDhgU52ew --no-tune &

ping localhost -c 5 && more nohup.out


打赏捐赠
RTM：RDwp9piY1FBV18dmWTxnhLBQAxDhgU52ew
