# 第9回 Webエンジニアリング演習 レポート
## 学籍番号
4724204
## Stateの一覧と役割
todos: TODOの一覧を保持する。追加や更新が行われると、画面の一覧表示に反映される。
title: 入力欄に入力中の文字列を保持する。
## 完了ボタンから画面更新まで
完了ボタンのクリックをきっかけに、子コンポーネントから渡されたonToggle(todo.id)が呼ばれ、Appの更新処理からsetTodosが実行される。
Stateの更新によって更新されたtodos が Propsとして渡されることで画面表示が更新される。
## 空白入力を防ぐコードと確認結果
function handleSubmit(event: FormEvent<HTMLFormElement>) {
    event.preventDefault();

　　const normalizedTitle: string = title.trim();
　　if (normalizedTitle === "") {
  　　return;
　　}


    const newTodo: Todo = {
      id: Date.now(), title, completed: false,
    };
    setTodos((current) => [...current, newTodo]);
    setTitle("");
  }

  結果
  空文字のまま送信：一覧の件数が変わらない
  半角スペース３文字を送信：一覧の件数が変わらない
  「　レポートを書く　」を送信：前後の空白が除かれて１件追加された
  「Reactを復習する」をEnterで送信：1件追加され、入力欄が空になった
