# 第6回 Webエンジニアリング演習 レポート
## 学籍番号
4724204
## `Todo`型の定義
const todos: Todo[] = [
    { id: 1, title: "型を定義する", completed: true },
    { id: 2, title: "関数を作る", completed: false },
    { id: 3, title: "レポートを書く", completed: true },
];
## 未完了件数を返す関数の引数と戻り値の型
export async function countIncompleteTodos(): Promise<number> {
  const currentTodos = await fetchTodos();
  const incompleteTodos = currentTodos.filter(
    (todo) => !todo.completed,
  );
  return incompleteTodos.length;
}
## 未完了件数の実行結果
[
  { id: 1, title: '型を定義する', completed: true },
  { id: 2, title: '関数を作る', completed: false },
  { id: 3, title: 'レポートを書く', completed: true }
]
未完了のTODO件数: 1
