# 第5回 Webエンジニアリング演習 レポート
## 学籍番号
4724204
## TODO配列のコード
const todos = [ 
    { id: 1, title: "型を復習する", completed: true },
    { id: 2, title: "配列を学ぶ", completed: false },
    { id: 3, title: "レポートを書く", completed: true },
    { id: 4, title: "課題を提出する", completed: false }
];
## TODOを更新した条件
for (const todo of todos) {
    if (!todo.completed) {
        todo.completed = true;
        console.log(`更新後: ${todo.title} [完了]`);
    }
}
## 完了件数の 更新前後の 実行結果
ID: 1, タイトル: 型を復習する, ステータス: 完了
ID: 2, タイトル: 配列を学ぶ, ステータス: 未完了
ID: 3, タイトル: レポートを書く, ステータス: 完了
ID: 4, タイトル: 課題を提出する, ステータス: 未完了
更新後: 配列を学ぶ [完了]
更新後: 課題を提出する [完了]
完了件数: 更新前 2件 -> 更新後 4件
