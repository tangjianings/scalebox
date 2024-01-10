# examples for ftp-copy

## 1. anonymous ftp-server to local

```sh

message:ftp://ftp.ncbi.nlm.nih.gov/mwa/tar1302106648~1302106648_1302111372_ics.dat.zst~/tmp/file
FILE_NAME=ftp://ftp.ncbi.nlm.nih.gov/mwa/tar1302106648~1302106648_1302111372_ics.dat.zst~/tmp/file~/tmp ACTION=PULL scalebox app create

message:1302106648_1302111372_ics.dat.zst
SOURCE_URL=ftp://ftp.ncbi.nlm.nih.gov/mwa/tar1302106648 TARGET_URL=/tmp/file FILE_NAME=1302106648_1302111372_ics.dat.zst ACTION=PULL  scalebox app create

```

## 2. non-anonymous ftp-server to local

```sh

```
## 3. local to ftp-server



```sh
bug:73:cmd_mkdir_remote="lftp -c \"open ${ftp_url}; mkdir -p ${remote_dir}\" 2> /work/mkdir-stderr.txt"
73:cmd_mkdir_remote="lftp -c \'open ${ftp_url}; mkdir -p ${remote_dir}\' 2> /work/mkdir-stderr.txt"

message:/tmp/file~1302106648_1302111372_ics.dat.zst~ftp://ftp.ncbi.nlm.nih.gov/tang
FILE_NAME=ftp://ftp.ncbi.nlm.nih.gov/mwa/tar1302106648~1302106648_1302111372_ics.dat.zst~/tmp/file~/tmp ACTION=PUSH ENABLE_RECHECK_PUSH=yes scalebox app create

message:1302106648_1302111372_ics.dat.zst
SOURCE_URL=/tmp/file TARGET_URL=ftp://ftp.ncbi.nlm.nih.gov/tang FILE_NAME=1302106648_1302111372_ics.dat.zst ACTION=PUSH 
ENABLE_RECHECK_PUSH=yes scalebox app create


```
