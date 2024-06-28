# ai_ws
　講義「人工知能」の環境を提供するプロジェクトです。`python3 venv`を使って仮想化を行なっているため他のプロジェクトに影響を与えずにプロジェクトの作成ができます。他にもいくつか別のプロジェクトを用意してあります。

- **[講義：人工知能用プロジェクト `ai_ws`](projects/ai_ws)**
- **[画像処理用プロジェクト `vision`](projects/vision)**

## macOSとLinux環境下でインストールする
以下の手順でセットアップします。

1. このリポジトリをクローンしてください。
   ```bash
   git clone https://github.com/GAI-313/ai_ws.git
   ```

2. クローンしたプロジェクトディレクトリに移動します。
   ```bash
   cd ai_ws
   ```

3. `ai_ws`環境を構築します。
   ```bash
   python3 -m venv ai_ws
   ```

4. 構築した`ai_ws`を起動（アクティベート）します。
   ```bash
   source ai_ws/bin/activate
   ```

5. 必要になるPythonパッケージをインストールします。
   ```bash
   pip install -r requirements.txt
   ```


## Windows環境下でインストールする
以下の手順でセットアップします。

1. このリポジトリをクローンしてください。
   ```
   git clone https://github.com/GAI-313/ai_ws.git
   ```

2. クローンしたプロジェクトディレクトリに移動します。
   ```
   cd ai_ws
   ```

3. `ai_ws`環境を構築します。
   ```
   python -m venv ai_ws
   ```

4. 構築した`ai_ws`を起動（アクティベート）します。Windowsではパスが少し異なります。
   ```
   ai_ws\Scripts\activate
   ```

5. 必要になるPythonパッケージをインストールします。
   ```
   pip install -r requirements.txt
   ```

## 起動
　プロジェクトディレクトリ内で以下のコマンドを実行すると jypiter notebook が起動します。
```bash
jupyter notebook
```

以下のようなエラーメッセージが表示されたら、`ai_ws/bin/activate` を通していないことを示しています。 
```
-bash: jupyter: command not found
```

## パッケージの更新
　仮想環境で新たなパッケージをインストールした場合は、`ai_ws` 直下に移動して以下のコマンドを実行して、 `requirements.txt` を更新してください。
```bash
pip freeze > requirements.txt
```

## 仮想環境の終了
　以下のコマンドを実行すると仮想環境が終了します。
```bash
deactivate
```
