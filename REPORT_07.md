# 第7回 Webエンジニアリング演習 レポート
## 学籍番号
4724204
## 2画面の見出しと本文
const app = document.querySelector("#app");

if (app === null) {
  throw new Error("#appが見つからない");
}

window.addEventListener("hashchange", () => {
    const page = location.hash;
    console.log(page);
    console.log(location.hash);

    if (page === "#detail") {
        app.innerHTML = `
            <h1>詳細ページ</h1>
            <p>この文章はTypeScriptから追加した。</p>
            <nav>
                <a href="#compare">比較</a>
                <a href="#detail">詳細</a>
            </nav>
        `;
    } else if (page === "#compare") {
        app.innerHTML = `
            <h1>比較ページ</h1>
            <p>比較のページです。</p>
            <nav>
                <a href="#compare">比較</a>
                <a href="#detail">詳細</a>
            </nav>
        `;
    }
});

## クリック後のURLとNetworkの確認
URLのアドレスバーの末尾が#compareから#detailに切り替わった。
https://opulent-space-trout-pj5jgrrj594pcr9j6-3000.app.github.dev/csr/#compare
https://opulent-space-trout-pj5jgrrj594pcr9j6-3000.app.github.dev/csr/#detail

新しいHTMLファイルがサーバーから新たに取得されていないことを確認した。
## 画面を切り替える処理の要点
window.addEventListener("hashchange", () => {
    const page = location.hash;
    console.log(page);
    console.log(location.hash);
