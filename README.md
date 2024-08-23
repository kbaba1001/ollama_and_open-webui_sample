# Ollama and open-webui

次の2つを素振りする

* https://github.com/ollama/ollama
* https://github.com/open-webui/open-webui

## 使い方

[elyza/Llama-3-ELYZA-JP-8B-GGUF](https://huggingface.co/elyza/Llama-3-ELYZA-JP-8B-GGUF) から `Llama-3-ELYZA-JP-8B-q4_k_m.gguf` をダウンロードして、このリポジトリにおく。

### Ollama と Open WebUI の起動

docker compose で起動できます。

```
docker compose up -d
```

Llama-3-ELYZA-JP-8B の model を登録。

```
docker compose exec ollama ollama create llama-3-elyza-jp-8b -f ./Modelfile
```

### Open WebUI での操作

* http://localhost:8080 にアクセスして適当にアカウントを作ってログインする。
* 左下の名前をクリックして、設定 > 管理者設定 > モデル と進む
* 「Ollama モデルを管理」のURLが `http://ollama:11434` になっていることを確認する
* 「Ollama モデルを管理」のURLの右側の↓ボタンを押下してモデル情報を取得する
* 「モデルを選択」で `llama-3-elyza-jp-8b` を選択

トップページに戻って、会話ができる。

