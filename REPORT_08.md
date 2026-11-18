# 第8回 Webエンジニアリング演習 レポート
## 学籍番号
4724204
## コンポーネント構成
import type { Todo } from "../types";
import { TodoItem } from "./TodoItem";

type TodoListProps = {
    todos: Todo[];
};

export function TodoList({ todos }: TodoListProps) {
    return (
      <ul>
        {todos.map((todo: Todo) => (
            <TodoItem key={todo.id} todo={todo} />
        ))}
      </ul>
    );
}
## `TodoItem`のProps型
type TodoItemProps = {
  todo: Todo;
};
## 期限あり・なしの画面確認結果
export function TodoItem({ todo }: TodoItemProps) {
  const today = new Date().toISOString().split("T")[0];

  return (
    <li>
      <strong>{todo.title}</strong>
      <span> {todo.completed ? "(完了)" : "(未完了)"}</span>
      {todo.dueDate && (
        <span style={{ color: todo.dueDate < today ? "red" : "inherit" }}>
          {" "}期限: {todo.dueDate}
        </span>
      )}
    </li>
  );
}

期限があるかつ過ぎているものは赤文字で表示された。
