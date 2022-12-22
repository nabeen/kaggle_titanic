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

### 2022-12-22

- 昨日の続き、Kaggle のチュートリアルを読みながら進めていく
  - https://www.amazon.co.jp/dp/B09P87T6L5
- グラフが書けなかったのは、`%matplotlib inline`を書けって話だった
- 写経の時間がもったいないので、サポートサイトからコードをコピペして進めていく
  - https://www.currypurin.com/tutorial_ver6_support
- ざざっと可視化して、各特徴量の関係を見ていく
  - こうして見ると、相関のある特徴量や逆に関係のない特徴量が見えてきて面白い
  - 関係ない特徴量を落としたり新しい特徴量を作ったりするのがいわゆる特徴量エンジニアリングってやつなのかな
- LightGBM をやっていく
  - 欠損値の対応
  - ダミー変数の作成
  - 連続データの離散化等は不要
  - 文字データを数値に置き換えれば OK
- カテゴリ変数を変換する
  - Sex、Embarked などに入っている文字データを変換
  - One-Hot エンコーディング
- ライブラリの使い方覚えればえいやっと投げられそう
  - あとは他の手法も
  - XGBoost とか
- 大体流れは理解した
