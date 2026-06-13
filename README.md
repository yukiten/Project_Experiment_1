# Project Experiment 1

## 概要

食材名を入力すると、機械学習モデルが料理カテゴリを予測し、対応するレシピを提案するWebアプリケーション。

大学のプロジェクト実験においてチームで開発を行った。機械学習による料理カテゴリ推薦機能に加え、レシピ検索、ユーザー投稿、ログイン機能などを実装している。

## システム構成

<img width="1171" height="442" alt="pro1" src="https://github.com/user-attachments/assets/425f7f9e-9dff-4ff1-8b31-a59da37621e3" />

## 使用技術

| 分野               | 技術                               |
| ---------------- | -------------------------------- |
| Backend          | Flask, SQLite                    |
| Frontend         | HTML, CSS, JavaScript            |
| Machine Learning | scikit-learn, MeCab, TF-IDF, MLP |
| Development      | Git, GitHub, Git LFS             |

## 主な機能

* 食材からのレシピ検索
* カテゴリ別レシピ検索
* レシピ一覧・詳細表示
* 機械学習による料理カテゴリ推薦
* ユーザー投稿機能
* ログイン機能

## 機械学習モデル

楽天レシピから収集した約24,000件のレシピデータを用いて、以下の6カテゴリ分類モデルを構築した。

* 日本料理
* 中国料理
* 韓国料理
* イタリア料理
* フランス料理
* エスニック料理

前処理にはMeCabによる形態素解析およびTF-IDFを利用し、分類モデルにはMLP（Multi Layer Perceptron）を採用した。

## 特徴

* 約24,000件のレシピデータを用いた料理カテゴリ分類
* FlaskによるWebアプリケーション実装
* 機械学習モデルとWebアプリケーションの統合
* GitHubを利用したチーム開発
* Git LFSによる大容量ファイル管理

## セットアップ

### 1. リポジトリをクローン

```bash
git clone https://github.com/hiroats/Project_Experiment_1.git
cd Project_Experiment_1
```

### 2. ブランチを取得

```bash
git fetch origin <branch名>
git checkout <branch名>
git pull origin <branch名>
```

### 3. Git LFSをインストール

Windows: Git LFS Installer を利用

Linux:

```bash
sudo apt install git-lfs
git lfs install
git lfs pull
```

### 4. 仮想環境の作成（任意）

```bash
python -m venv venv
```

Windows

```bash
venv\Scripts\activate
```

Linux / macOS

```bash
source venv/bin/activate
```

### 5. パッケージをインストール

```bash
pip install -r requirements.txt
```

### 6. Flaskアプリを設定

Linux / macOS

```bash
export FLASK_APP=run.py
```

Windows

```bash
set FLASK_APP=run.py
```

### 7. アプリを起動

```bash
flask run
```
