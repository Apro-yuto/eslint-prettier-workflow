# eslint-prettier-workflow
## 概要
- 個人的に現状使用してるGitFlowに簡単にフロントのCIを組み込みたかっただけ
- あと楽しそうだった
#### *注意点.  そもそも自分用だからymlファイルは適宜編集してね。

## 使用方法
> Git

ワークフローが実行されるデフォルトの**ブランチ**は以下の三つになります。
- master
- develop
- feature/**

> npm(Node)

  ```
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "format": "prettier --check ./src",
    "format:fix": "prettier --write ./src",
    "lint": "eslint ./src",
    "lint:fix": "eslint --fix ./src",
    "prepare": "husky install",
    "lint-staged": "lint-staged"
  }
  ```
  
  以下のコマンドをプロジェクトルートで実行する。
  ちなみに、eslintとprettier
  ```
  npm i --save-dev eslint prettier
  ```
