# kaggle_titanic

## Logs

### 2022-12-21

- Kaggle のチュートリアルを読みながら進めていく
  - https://www.amazon.co.jp/dp/B09P87T6L5
- Kaggle への submit の確認
  - Notebook で submit
  - コードで submit
  - ローカルからファイルで submit
    - CLI も用意されている
    - `kaggle competitions submit -c titanic -f submission.csv -m "Message"`
  - 最初に触れた数年前と結構変わってる気がする？
- pandas で対象データの色々を確認していく
  - `notebook/titanic-notebook.ipynb`
  - ローカルで動かしたい
    - WSL 内で anaconda 入れたりが必要そうなので後回し
    - しばらくは Kaggle 上の Notebook を使う
- pandas_profiling でサマリーを見る
  - なにこれすごい
- matplotlib, seaborn での可視化
  - うまく `japanize_matplotlib` が入らない
    - デフォルトだと外部接続できないように設定されている
    - Settings から on にして解決
  - うまく可視化出来ない
    - typo はしてなさそう
    - version 変わって API も変わった可能性？
  - 原因もつかめないので切り上げ
  - GitHub 連携したら Kaggle 上から GitHub に突っ込めて便利
