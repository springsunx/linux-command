figlet
===

字符串转为 “字画符”。

## 安装

+ Ubuntu 等系统

```shell
apt-get update
apt-get install -y figlet
```

+ CentOS 等系统

```shell
yum install epel-release
yum install -y figlet
```

## 概要

```shell
figlet [ message ] [ -option ]
```

## 主要用途

- 将普通字符串转为有简单字符拼接而成的 “字画符”。

## 参数

message 是需要转换的字符串。
当没有输入 message 时，会读取标准输入，因此可以配合管道符等使用。

## 选项

```shell
-w      限制输出宽度，默认为 '80'
-c      居中显示
-f      指定字体，默认为 'standard'
-k      保留字符之间的空隙
-t      对齐宽度到当前终端的宽度，这个参数优先级比 -w 高
-v      显示版本信息
```

## 返回值

字符串，由简单字符拼接而成的 “字画符”。

## 示例

### 从参数输入

```shell
figlet 'Hello, World!'
```

```bash
 _   _      _ _         __        __         _     _ _
| | | | ___| | | ___    \ \      / /__  _ __| | __| | |
| |_| |/ _ \ | |/ _ \    \ \ /\ / / _ \| '__| |/ _` | |
|  _  |  __/ | | (_) |    \ V  V / (_) | |  | | (_| |_|
|_| |_|\___|_|_|\___( )    \_/\_/ \___/|_|  |_|\__,_(_)
```

### 配合管道符输入

```shell
echo 'Hello, World!' | figlet
```

```bash
 _   _      _ _         __        __         _     _ _
| | | | ___| | | ___    \ \      / /__  _ __| | __| | |
| |_| |/ _ \ | |/ _ \    \ \ /\ / / _ \| '__| |/ _` | |
|  _  |  __/ | | (_) |    \ V  V / (_) | |  | | (_| |_|
|_| |_|\___|_|_|\___( )    \_/\_/ \___/|_|  |_|\__,_(_)
```

### 限制宽度

```shell
figlet 'Hello, World!' -w 40
```

```bash
 _   _      _ _
| | | | ___| | | ___
| |_| |/ _ \ | |/ _ \
|  _  |  __/ | | (_) |
|_| |_|\___|_|_|\___( )
                    |/
__        __         _     _ _
\ \      / /__  _ __| | __| | |
 \ \ /\ / / _ \| '__| |/ _` | |
  \ V  V / (_) | |  | | (_| |_|
   \_/\_/ \___/|_|  |_|\__,_(_)
```

### 居中显示

```shell
figlet 'Hello, World!' -w 40 -c
```

```bash
         _   _      _ _
        | | | | ___| | | ___
        | |_| |/ _ \ | |/ _ \
        |  _  |  __/ | | (_) |
        |_| |_|\___|_|_|\___( )
                            |/
    __        __         _     _ _
    \ \      / /__  _ __| | __| | |
     \ \ /\ / / _ \| '__| |/ _` | |
      \ V  V / (_) | |  | | (_| |_|
       \_/\_/ \___/|_|  |_|\__,_(_)
```

### 指定字体

```shell
figlet 'Hello, World!' -w 40 -c -f slant
```

```bash
            __  __     ____
           / / / /__  / / /___
          / /_/ / _ \/ / / __ \
         / __  /  __/ / / /_/ /
        /_/ /_/\___/_/_/\____( )
                             |/
     _       __           __    ____
    | |     / /___  _____/ /___/ / /
    | | /| / / __ \/ ___/ / __  / /
    | |/ |/ / /_/ / /  / / /_/ /_/
    |__/|__/\____/_/  /_/\__,_(_)
```

### 保留字符之间的空隙

```shell
figlet 'Hello, World!' -w 40 -c -k
```

```bash
       _   _        _  _
      | | | |  ___ | || |  ___
      | |_| | / _ \| || | / _ \
      |  _  ||  __/| || || (_) |_
      |_| |_| \___||_||_| \___/( )
                               |/
  __        __            _      _  _
  \ \      / /___   _ __ | |  __| || |
   \ \ /\ / // _ \ | '__|| | / _` || |
    \ V  V /| (_) || |   | || (_| ||_|
     \_/\_/  \___/ |_|   |_| \__,_|(_)
```
