# ベースイメージに軽量な Python を使う（汎用的で素早い）
FROM python:3.11-slim

# 基本ツール
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential git curl ca-certificates \
 && rm -rf /var/lib/apt/lists/*

# apt-get update : パッケージ情報更新
# apt-get install ... → 開発でよく使う基本ツールをインストール
    # build-essential: C系のビルドに必要（Pythonパッケージの一部がC拡張を使うため）
    # git: ソースコードの取得に使う
    # curl: 通信テストやダウンロードに便利
    # ca-certificates: HTTPS通信を安全にする証明書セット
# --no-install-recommends → 余計なパッケージを入れない
# rm -rf /var/lib/apt/lists/* → イメージを小さくするためキャッシュ削除

WORKDIR /workspace

# 依存ファイルをコンテナにコピーしてインストール（キャッシュ効く）
COPY requirements.txt /workspace/requirements.txt
RUN pip install --no-cache-dir -r /workspace/requirements.txt

# コンテナ起動時に利用するポート
EXPOSE 8000

# デフォルトのコマンドは起動せず、VS Code からコマンド実行する想定
CMD ["bash"]
