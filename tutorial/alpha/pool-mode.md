# 풀 모드

## 1. 등록 및 새 계정 추가

1. [Aleo Pool](https://aleopool.xyz)에 로그인하여 등록을 완료합니다.
2. "대시 보드"로 이동하여 "마이너" 페이지에서 "계정 추가"를 클릭합니다.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

&#x20;3\. 마이닝 계정 이름을 기록하고 저장합니다.

## 2. 하드웨어 추천

* **CPU:** 4 코어 CPU
* **GPU:** 2080Ti/3080/3090\*8
* **VRAM:** 5G 이상
* **RAM：**8G/GPU
* **SSD：**128G
* **최신 그래픽 카드 드라이버를 설치해야 하며, 현재는 NVIDIA 그래픽 카드만 지원됩니다.**

## **3. aleo-pool-prover 다운로드**

**최신 업데이트: 2023-01-09**

* [Ubuntu 18.04 (GPU) ](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_1804\_gpu)
* [Ubuntu 18.04 (CPU)](https://github.com/aleo-pool/prover/releases/download/v1.1.0/aleo-pool-prover\_ubuntu\_1804\_cpu)
* [Ubuntu 20.04 (GPU)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_2004\_gpu)
* [Ubuntu 20.04 (CPU)](https://github.com/aleo-pool/prover/releases/download/v1.1.0/aleo-pool-prover\_ubuntu\_2004\_cpu)
* [Windows (CPU)](https://github.com/aleo-pool/prover/releases/download/v1.1.0/aleo-pool-prover\_cpu\_windows.exe)
* [Apple (Intel)](https://github.com/aleo-pool/prover/releases/download/v1.1.0/aleo-pool-prover\_cpu\_x86\_64-apple-darwin)
* [Apple (Silicon)](https://github.com/aleo-pool/prover/releases/download/v1.1.0/aleo-pool-prover\_cpu\_aarch64-apple-darwin)

## 4. aleo-pool-prover 실행

1. aleo-pool-prover 디렉토리로 이동합니다.
2. 다음 코드를 실행합니다.

```
./aleo-pool-prover_ubuntu_1804_gpu --account_name test_account --miner_name test_miner
#Make sure the prover name as same as you downloaded one
#Replace "test_account" with your mining account name
#"test_miner" with a customizable one for web-based device differentiation.
```

3. 자원 사용량을 조정해야하는 경우, 명령 줄 뒤에 다음을 추가 할 수 있습니다.

```
-j number of tasks (default is 1) -t number of threads for a single task
```

4. 이중 GPU를 사용하는 경우, 각 GPU는 프로세스를 시작하며 현재 프로세스에서 사용하는 GPU는 CUDA\_VISIBLE\_DEVICES 환경 변수로 제어됩니다.

```
export CUDA_VISIBLE_DEVICES=0
./aleo-pool-prover_ubuntu_1804_gpu --account_name test_account --miner_name test_miner
export CUDA_VISIBLE_DEVICES=1
./aleo-pool-prover_ubuntu_1804_gpu --account_name test_account --miner_name test_miner
```

## 5. 채굴 시작하기

구성 후, 광부는 약 1 분 후에 자동으로 Aleo 풀에 추가되며, 기기 백엔드에서 실시간으로 테스트 된 전력 속도를 볼 수 있습니다. Aleo Pool 웹 페이지에서도 볼 수 있습니다. 웹 사이드의 통계는 15 분의 평균 컴퓨팅 파워이므로 데이터는 15 분 후에 백엔드 데이터와 동기화됩니다.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

## 6. FAQ

### Q1. "Permission Denied" 오류가 발생하는 경우 어떻게 해야 하나요?



```
#Run the following command
#Make sure the software name is correct
chmod +777 ./aleo-pool-prover_ubuntu_1804_gpu
```

### Q2. Cuda 오류?

현재, NVIDIA 버전 515 이상을 다운로드하는 것을 권장합니다.


### Q3. "error while loading shared libraries: libssl.so.1.1"


```
#Install the following package
http://nz2.archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2.16_amd64.deb
```

