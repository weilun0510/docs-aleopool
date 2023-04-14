# 礦池模式

## 一、開通礦池及新建賬戶

1. 登陸 [Aleo Pool 官方網站](https://aleopool.xyz)，並完成注冊登陸；
2. 前往「賬戶總覽」，在「挖礦賬戶」頁點擊「新增挖礦賬戶」

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

&#x20;3\. 記錄並保存您的挖礦賬戶名

## 二、推薦配置

* CPU：4核/GPU (如7542是32核，則搭配8 GPU)&#x20;
* GPU：2080Ti/3080/3090\*8&#x20;
* 顯存：5G以上
* 內存：每 GPU 預留 8G 以上，最大化內存通道&#x20;
* 固態：128G (能存下系統和日志就行)
* **需要安裝最新顯卡驅動，當前僅支持 NVIDIA 顯卡**
* **Ubuntu 20.04 需要確保OpenSSL版本爲1.1.1**

## 三、下載 aleo-pool-prover

### 最近更新：2023-01-09

* [Ubuntu 18.04 (GPU)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_1804\_gpu)
* [Ubuntu 18.04 (CPU)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_1804\_cpu)
* [Ubuntu 20.04 (GPU)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_2004\_gpu)
* [Ubuntu 20.04 (CPU)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_2004\_cpu)
* [Windows (CPU)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo-pool-prover\_cpu\_windows.exe)
* [Apple (Intel)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_cpu\_x86\_64-apple-darwin)
* [Apple (Silicon)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_cpu\_aarch64-apple-darwin)

## 四、運行 aleo-pool-prover

1. 進入 aleo-pool-prover 所在的目錄
2. 運行以下代碼

```
./aleo-pool-prover_ubuntu_1804_gpu --account_name test_account --miner_name test_miner
#確認程序包與下載的名字壹致
#修改「test_account」爲您的挖礦賬戶
#「test_miner」可自定義，用于網頁端設備的區分
```

3\. 如若需要調整資源使用可在命令行後補充

```
-j 任務數（默認填寫1即可） -t 單個任務線程數量
```

4\. 如若使用雙 GPU，每個 GPU 啓動壹個進程，通過 CUDA\_VISIBLE\_DEVICES 環境變量控制當前進程使用的GPU

```
export CUDA_VISIBLE_DEVICES=0
./aleo-pool-prover_ubuntu_1804_gpu --account_name test_account --miner_name test_miner
export CUDA_VISIBLE_DEVICES=1
./aleo-pool-prover_ubuntu_1804_gpu --account_name test_account --miner_name test_miner
```

## 五、開始挖礦

配置完成後礦機將在1分鍾左右自動添加至您 Aleo 礦池，測試的算力速度可以在設備後台查看實時數據。也可以通過Aleo Pool網頁端查看。網頁端統計的是15分鍾的平均算力，所以顯示數據會在15分鍾後和後台數據同步正常。

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

## 六、FAQ

### Q：運行程序提示「權限不夠」？

```
// 進入程序所在目錄, 確認程序包與下載的名字壹致
// 運行以下指令
chmod +x ./aleo-pool-prover_ubuntu_1804_gpu
```

### Q: 提示「error while loading shared libraries: libssl.so.1.1」?

```
// 安裝以下組件依賴
http://nz2.archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2.16_amd64.deb
```
