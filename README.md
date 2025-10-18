# 環境構築手順メモ
```shell
sudo apt update
```

```shell
sudo apt install build-essential libbz2-dev libdb-dev \
  libreadline-dev libffi-dev libgdbm-dev liblzma-dev \
  libncursesw5-dev libsqlite3-dev libssl-dev \
  zlib1g-dev uuid-dev tk-dev
```

```shell
python3 --version
# Python 3.10.12
```

```shell
sudo apt install python3.10-venv -y
```

```shell
python3 -m venv venv
# 実行場所配下に /venv が生成される
```

```shell
source venv/bin/activate
```

```shell
pip install --upgrade pip  
```

```shell
pip install mkdocs
```

```shell
mkdocs new [ディレクトリ名]
# ディレクトリ名配下に docs/ と mkdocs.yml が生成される
```
