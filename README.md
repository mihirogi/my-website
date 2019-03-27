## my-website
2019年春版に作り直してる最中

### 開発プロセス周り
#### Pushする前に

1. `npm run format:check`でフォーマット確認
2. `npm run format`でフォーマットする
3. `npm run test-headless`が通る
4. Push!!!

#### ブランチ運用

基本的にGitFlowにのっとる

* master
* develop
* hotfix/XXXXX
  + masterから分岐する
* feature/XXXXX
  + developから分岐する
* bugfix/XXXXXX
  + developから分岐する

#### マージ

マージは、プルリクエストをちゃんと出す

* feature/XXXX -> develop
  + Squash and merge
* bugfix/XXXX -> develop
  + Squash and merge
* hotfix/XXXX -> master
  + Create a merge commit
* develop -> master
  + Create a merge commit
