# 第4回 Webエンジニアリング演習レポート
## 学籍番号
4724204
## `const`と`let`の 宣言・ 再代入に 使用したコード
const courseName = "Web Engineering";
let retryCount = 1;

courseName = "Other Course";
retryCount = 2;
console.log(courseName);
console.log(retryCount);
## VSCodeと`pnpm run check`に 表示されたエラー
定数であるため、'courseName'に代入することはできません。 ts(2588)
count
## 修正後の 実行結果と `const`・ `let`の 違いの 説明
@4724204 ➜ /workspaces/web-eng-typescript (main) $ pnpm run check
$ tsc --noEmit src/index.ts
@4724204 ➜ /workspaces/web-eng-typescript (main) $ pnpm run start
$ tsx src/index.ts
2

constは再代入できず、letは再代入できる。今回の課題では、constへの再代入はエラーになったが、letの値は1から2へ変更できた。
