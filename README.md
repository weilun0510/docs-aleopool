# Alpha (Ubuntu/Windows/OS X)

## 1、Регистрация и добавление новой учетной записи

1. Вход в систему [Aleo Pool](https://aleopool.xyz)，и завершить регистрацию;
2. Перейдите в "Dashboard" и нажмите "Add Account" на странице "Miners".
3. Записывайте и сохраняйте имена счетов для майнинга

## 2、Ubuntu

### Горное оборудование и окружающая среда

1. Система：Ubuntu 18.04/20.04
2. Оборудование:

Пока не протестировано на минимальной конфигурации

Рекомендуемая конфигурация**:**

* **CPU:** 4 cores CPU
* **GPU:** 2080Ti/3080/3090\*8
* **RAM：**8G/GPU
* **SSD：**128G
* **Необходимо установить последнюю версию драйвера видеокарты, в настоящее время поддерживаются только видеокарты NVIDIA**

### Скачать шахтер

* [Ubuntu 18.04 (GPU) ](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_1804\_gpu)
  * Server：wget https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_1804\_gpu
* [Ubuntu 18.04 (CPU)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_1804\_cpu)
  * Server：wget https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_1804\_cpu
* [Ubuntu 20.04 (GPU)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_2004\_gpu)
  * Server：wget https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_2004\_gpu
* [Ubuntu 20.04 (CPU)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_2004\_cpu)
  * Server：wget https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_ubuntu\_2004\_cpu

### Запустить шахтера

1. cd команда переходит в каталог, в котором находятся файлы программы майнера (игнорировать, если они уже загружены в текущий каталог)команда переходит в каталог, в котором находятся файлы программы майнера (игнорировать, если они уже загружены в текущий каталог)
2. Запустить шахтера

* **Single GPU**：
  * <mark style="color:green;">.</mark><mark style="color:blue;">/aleo-pool-prover\_ubuntu\_1804\_gpu</mark> --account\_name <mark style="color:green;">test\_account</mark> --miner\_name <mark style="color:green;">test\_miner</mark>
* **Dual GPU**
  * export CUDA\_VISIBLE\_DEVICES=0
  * <mark style="color:green;">.</mark><mark style="color:blue;">/aleo-pool-prover\_ubuntu\_1804\_gpu</mark> --account\_name <mark style="color:green;">test\_account</mark> --miner\_name <mark style="color:green;">test\_miner</mark>
  * export CUDA\_VISIBLE\_DEVICES=1
  * <mark style="color:green;">.</mark><mark style="color:blue;">/aleo-pool-prover\_ubuntu\_1804\_gpu</mark> --account\_name <mark style="color:green;">test\_account</mark> --miner\_name <mark style="color:green;">test\_miner</mark>
* **CPU**
  * <mark style="color:green;">.</mark><mark style="color:blue;">/aleo-pool-prover\_ubuntu\_1804\_cpu</mark> --account\_name <mark style="color:green;">test\_account</mark> --miner\_name <mark style="color:green;">test\_miner</mark>

<mark style="color:red;">**Примечание: Замените "test\_account" на имя вашей учетной записи для майнинга, а "test\_miner" - на настраиваемое для дифференциации устройств через Интернет.**</mark>

<mark style="color:red;">Если вам нужно настроить использование ресурсов, вы можете добавить после командной строки: -j количество задач (по умолчанию 1) -t количество потоков для одной задачи</mark>

## 3、Windows

### Скачать шахтер

* [Windows (CPU)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_cpu\_windows.exe)

### Запустить шахтера

1. Запустите программу через окно cmd (win+R enter cmd для входа в окно cmd)
2. cd команда переходит в каталог, в котором находятся файлы программы майнера (игнорировать, если они уже загружены в текущий каталог)команда переходит в каталог, в котором находятся файлы программы майнера (игнорировать, если они уже загружены в текущий каталог)
3. Запустить шахтера

* Windows
  * <mark style="color:blue;">.\aleo-pool-prover\_cpu\_windows.exe</mark> --account\_name <mark style="color:green;">test\_account</mark> --miner\_name <mark style="color:green;">test\_miner</mark>

<mark style="color:red;">**Примечание: Замените "test\_account" на имя вашей учетной записи для майнинга, а "test\_miner" - на настраиваемое для дифференциации устройств через Интернет.**</mark>

<mark style="color:red;">Если вам нужно настроить использование ресурсов, вы можете добавить после командной строки: -j количество задач (по умолчанию 1) -t количество потоков для одной задачи</mark>

## 4、OS X

### Скачать шахтер

* [Apple (Intel)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_cpu\_x86\_64-apple-darwin)
* [Apple (Silicon)](https://nd-valid-data-bintest1.oss-cn-hangzhou.aliyuncs.com/aleo/aleo-pool-prover\_cpu\_aarch64-apple-darwin)

### Запустить шахтера

1. Open Terminal
2. cd команда переходит в каталог, в котором находятся файлы программы майнера (игнорировать, если они уже загружены в текущий каталог)команда переходит в каталог, в котором находятся файлы программы майнера (игнорировать, если они уже загружены в текущий каталог)
3. Запустить шахтера

* Apple (Intel)
  * <mark style="color:blue;">./aleo-pool-prover\_cpu\_x86\_64-apple-darwin</mark> --account\_name <mark style="color:green;">test\_account</mark> --miner\_name <mark style="color:green;">test\_miner</mark>
* Apple (Silicon)
  * <mark style="color:blue;">./aleo-pool-prover\_cpu\_aarch64-apple-darwin</mark> --account\_name <mark style="color:green;">test\_account</mark> --miner\_name <mark style="color:green;">test\_miner</mark>

<mark style="color:red;">**Примечание: Замените "test\_account" на имя вашей учетной записи для майнинга, а "test\_miner" - на настраиваемое для дифференциации устройств через Интернет.**</mark>

<mark style="color:red;">Если вы получаете запрос на разрешение, попробуйте использовать следующий код и повторите попытку</mark>

* chmod +rwz <mark style="color:blue;">aleo-pool-prover\_cpu\_x86\_64-apple-darwin</mark>
* chmod +rwz <mark style="color:blue;">aleo-pool-prover\_cpu\_aarch64-apple-darwin</mark>

## 5、Начать добычу полезных ископаемых

После настройки майнеры будут автоматически добавлены в ваш пул Aleo примерно через 1 минуту, а протестированную скорость мощности можно посмотреть в режиме реального времени в бэкенде устройства. Вы также можете просмотреть ее на веб-странице пула Aleo. Статистика на веб-странице - это средняя вычислительная мощность за 15 минут, поэтому данные будут синхронизированы с данными бэкенда через 15 минут.
