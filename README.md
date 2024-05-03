# nujabec/myrocker-shiny

## 概要

base: nujabec/myrocker
add: shiny-server

## 使い方

```bash
# renvのcache用にvolume作成(初回のみ)
docker volume create renv

# イメージのpull
docker pull nujabec/myrocker-shiny:20240503

# (イメージの作成)
# docker compose build 

# コンテナの起動
docker compose up -d
```
## push方法

```bash
docker login
docker push nujabec/myrocker-shiny:20240503
```

## オフライン環境にdocker imageを持っていく方法

```bash
# オンライン端末でイメージを作成
# docker imageをtarファイルに変換
docker save nujabec/myrocker-shiny:20240503 > myrocker-shiny_20240503.tar
# オフライン端末で、tarファイルからdocker imageを読む
docker load < myrocker-shiny_20240503.tar
```
