# examples for rsync-copy

## 1. ssh-server to local

```sh
message:master.cf
SOURCE_URL=scalebox@10.255.128.1/etc/postfix TARGET_URL=/tmp FILE_NAME=master.cf  scalebox app create

message:scalebox@10.255.128.1/etc~postfix/master.cf~/tmp
FILE_NAME=scalebox@10.255.128.1/etc~postfix/master.cf~/tmp scalebox app create

message:scalebox@10.255.128.1/etc/postfix~master.cf~/tmp
FILE_NAME=scalebox@10.255.128.1/etc/postfix~master.cf~/tmp scalebox app create

message:scalebox@10.255.128.1/~etc/postfix/master.cf~/tmp
FILE_NAME=scalebox@10.255.128.1/~etc/postfix/master.cf~/tmp scalebox app create

```

## 2. local to ssh-server

```sh

message:master.cf
SOURCE_URL=/etc/postfix TARGET_URL=scalebox@10.255.128.1/tmp FILE_NAME=master.cf  scalebox app create

message:/etc~postfix/master.cf~scalebox@10.255.128.1/tmp
FILE_NAME=/etc~postfix/master.cf~scalebox@10.255.128.1/tmp scalebox app create

message:/~etc/postfix/master.cf~scalebox@10.255.128.1/tmp
FILE_NAME=/~etc/postfix/master.cf~scalebox@10.255.128.1/tmp scalebox app create

message:/etc/postfix~master.cf~scalebox@10.255.128.1/tmp
FILE_NAME=/etc/postfix~master.cf~scalebox@10.255.128.1/tmp scalebox app create

```

## 3. rsync-server to local

```sh

```

## 4. local to rsync-server

```sh

```
