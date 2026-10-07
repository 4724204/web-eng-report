# 第2回 Webエンジニアリング
## 学籍番号
4724204

## コンフリクトが演習 レポート発生した理由
同じ main から作成した 2 つのブランチで、README.md の同じ行に対して異なる変更を加えてマージしようとしたため、コンフリクトが発生した。

## 解決手順
1. practice/conflict-b ブランチで git pull --no-rebase origin main を実行してコンフリクトを発生させた。
2. README.md 内の競合を削除し、「- ブランチを使い、コンフリクトも自分で解決する」に編集した。
3. 変更をコミット・プッシュし、GitHub 上でプルリクエストをマージした。

## 履歴
*   fa8084a (HEAD -> main, origin/main, origin/HEAD) Merge pull request #3 from 4724204/practice/conflict-b
|\  
| *   93ae0c9 (origin/practice/conflict-b, practice/conflict-b) Resolve README conflict
| |\  
| |/  
|/|   
* |   600952d Merge pull request #2 from 4724204/practice/conflict-a
|\ \  
| * | 58d5d92 (origin/practice/conflict-a, practice/conflict-a) Update goal in conflict A
|/ /  
| * ab7e93a Update goal in conflict B
|/  
*   9860973 Merge pull request #1 from 4724204/feature/add-readme
|\  
| * 4ffcc82 (origin/feature/add-readme) Add README
|/  
* b78ca7f Add REPORT_01.md
* 80c22e8 Add index.html
* dcf4ff8 Create devcontainer.json
* 16f0452 Initial commit
(END)