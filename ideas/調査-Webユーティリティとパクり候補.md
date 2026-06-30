# 調査：よく使われるWebユーティリティとパクり＋α候補（※旧版・tier寄り）

> **訂正：** 依頼は「Webツールの**利用ランキング**からパクる」だった。本ファイルは tier メーカーに寄りすぎ。  
> **→ `調査-Webユーティリティ利用ランキング.md` が正しい調査。**

「上位互換を作る」ための市場調査。  
大手SaaS（Slack、Canva等）ではなく、**個人でも作れるシンプルWebツール** に絞る。

---

## 結論サマリ

| 優先度 | カテゴリ | 代表サービス | パクり＋αのしやすさ |
|--------|----------|--------------|---------------------|
| ◎ | **Tier表メーカー** | TierMaker | 高。自分も興味あり。差別化ポイント明確 |
| ○ | **投票（Poll）** | StrawPoll | 中。シンプルだが StrawPoll が強い |
| ○ | **ルーレット** | SpinTheWheel 等 | 中。飽和気味 |
| △ | 画像圧縮 | TinyPNG, Squoosh | 低。激戦区・技術勝負 |
| △ | QR生成 | 多数 | 低。完全コモディティ |
| △ | PDFツール | ilovepdf | 低。機能競争になりがち |
| × | 文字数カウント等 | 各種 | 単機能すぎて拡散弱い |

**第一候補は tier メーカー。** 第二候補は poll / ルーレット。

---

## カテゴリ別：代表サービスと特徴

### 1. Tier表メーカー（ランキング表）◎

| サービス | URL | 特徴 | 弱点（＝αの入り口） |
|----------|-----|------|---------------------|
| **TierMaker** | tiermaker.com | 最大手。テンプレ数百万。Live Voting、Alignment Chart、トーナメントも | **広告多い・英語UI・重い**。登録周りが煩い |
| **TierBuddy** | tierbuddy.com | 「TierMakerより10倍速・無広告・無料」が訴求 | 既に TierMaker の上位互換を名乗っている |
| **TierAny** | tierany.site | PNG 1920×1080 出力、Pro で透かし除去 | 差別化は出力品質寄り |
| **tierlist-marker.com** | tierlist-marker.com | **日本語・登録不要・30秒** | 認知は TierMaker より低い |
| **tier-maker.vercel.app** | tier-maker.vercel.app | 個人製。日本語。シンプル | 機能少なめ |

**市場の空き：** 「日本語で最速・無広告・テキストだけ tier も可・変なお題プリセット」

**拡散：** 完成 PNG が X / Discord にそのまま貼られる。めっちゃカメレオン的「結果が素材」。

---

### 2. 投票（Poll）○

| サービス | URL | 特徴 | 弱点 |
|----------|-----|------|------|
| **StrawPoll** | strawpoll.com | 登録不要。2.3Mユーザー。リアルタイム結果 | 汎用poll。個性を出しにくい |
| TierMaker Live Voting | tiermaker.com | tier 特化のライブ投票 | tier 専用 |

**+α案：** 「今日のお題に1秒投票」、匿名・消える投票、大喜利お題付き poll

---

### 3. ルーレット / ランダム選択 ○

| サービス | URL | 特徴 |
|----------|-----|------|
| **SpinTheWheel.io** | spinthewheel.io | カスタムルーレット、保存 |
| **SpinWheel.app** | spinwheel.app | 日本語対応、教室・家族向け |
| **Random Wheel Spin** | randomwheelspin.com | 隠しアクティビティ付き |

**+α案：** 配信者向け、お題ガチャと連携、結果を画像で吐く

---

### 4. 画像・PDF・QR（激戦区 △）

| カテゴリ | 代表 | 備考 |
|----------|------|------|
| 画像圧縮 | TinyPNG, Squoosh, ToolShare Lab | WASM・サーバー非送信が標準に。新規参入はSEO戦争 |
| PDF | ilovepdf | 多機能。個人では重い |
| QR | webtools-lab, KIZUNA Works 等 | 完全同質化 |
| カラー変換 | webtools-lab | 開発者向け。拡散弱い |

**日本のツール集（参考）：**
- [webtools-lab](https://webtools-lab.com/) — 180種以上
- [ToolShare Lab](https://webatives.com/) — 108種、画像圧縮強み
- [KIZUNA Works](https://kizuna-works.jp/tools/) — 印鑑・PDF・QR
- [ToolShed](https://toolshed.yuzlrin.jp/) — 文字数・JSON・SEO系

→ **1機能だけ抜き出して上位互換** なら可能だが、流行り感・拡散は tier より弱い。

---

### 5. TierMaker が持つ周辺機能（単体でも可）

| 機能 | 説明 | 単体化の可否 |
|------|------|--------------|
| **Alignment Chart** | 9マス／4象限で配置 | ○ シンプルに単体化しやすい |
| **Live Voting** | リアルタイムで tier 投票 | ○ tier とセットが自然 |
| **Tournament Bracket** | トーナメント表 | △ ニッチ |
| **Spin Wheel** | ルーレット | △ 既存多数 |

---

## 「パクる」とは何をコピーするか

法的・倫理的には **アイデア・UXパターン** を参考にし、**コード・デザイン・テンプレ画像の盗用はしない**。

パクる対象：

1. **コアループ**（ドラッグで tier に並べる → PNG 保存）
2. **ユーザーの期待**（登録不要、30秒、スマホ可）
3. **競合の弱点**（TierMaker の広告・英語・重さ）

パクらない／自前で：

- ブランド・おかしさ・制約（+α）
- 日本語お題、テキスト tier、速度

---

## Tierメーカー：上位互換の +α 案（本命）

TierBuddy が「速い・無広告」で TierMaker を殴っている。  
それ以上を狙うなら **速度・広告以外** で尖らせる。

| +α | 内容 | 参考にした例 |
|----|------|--------------|
| **日本語ファースト** | UI・お題・ヘルプすべて日本語 | tierlist-marker |
| **テキストだけ tier** | 画像いらない。PC勢・文字だけで ranking | 自分の setlog 議論と同型 |
| **秒で開く** | 初回ロード &lt; 1秒。広告ゼロ | TierBuddy |
| **変なお題プリセット** | 「人生で後悔した食べ物」「説明不能な夢」 | 流行り感・驚き |
| **60秒 tier** | 制限時間つき。慌てて並べる | setlog の制約 |
| **他人の平均 tier と差分表示** | 自分だけの変態ランクが見える | 拡散ネタ |
| **X 用サイズで即 export** | 1200×675 等ワンクリック | 結果が素材 |
| **URL だけで共有** | 完成 tier の URL。見る専も楽しい | StrawPoll 的 |
| **Live 投票** | 配信者がお題、視聴者が tier 投票 | 8番出口・めっちゃカメレオン的参加型 |

### MVP（最小）の提案

```
開く → テキスト or 画像を追加 → ドラッグで S〜D → PNG or URL で共有
```

**最初は画像テンプレなしでも可。** テキストだけ tier で十分回る。

---

## 第二候補：Poll / ルーレットの +α

### 超簡易 Poll

- StrawPoll のコア：登録不要・リンク共有・リアルタイム
- +α：「24時間で消える」「お題付き」「結果が画像」

### お題ルーレット

- SpinTheWheel のコア：項目入れて回す
- +α：「大喜利お題ガチャ」「会話ネタ30案」の実用寄り

---

## 参考事例との対応

| 参考にしたい感覚 | tier メーカーでの実装 |
|------------------|----------------------|
| 8番出口 | 毎日「お題 tier」1つ。全員同じリスト |
| めっちゃカメレオン | 完成 tier を晒して議論 |
| setlog | 1日1 tier だけ作れる制限モード |
| note | シンプル・広告なし・書く（並べる）だけ |

---

## 次のアクション

- [ ] tier メーカー MVP の画面1枚（ワイヤー）
- [ ] 競合3つ（TierMaker / tierlist-marker / TierBuddy）を実際に触って体感差をメモ
- [ ] 「テキストだけ tier」から始めるか「画像も」から始めるか決める
- [ ] 制作用WSへ渡す文書を `まとめ-制作用へ渡す.md` に追記

---

## 参考リンク

- TierMaker: https://tiermaker.com/
- TierBuddy: https://tierbuddy.com/
- tierlist-marker（日本語）: https://tierlist-marker.com/
- tier-maker.vercel.app（日本語・個人）: https://tier-maker.vercel.app/
- StrawPoll: https://strawpoll.com/
- SpinTheWheel: https://spinthewheel.io/ja
- webtools-lab: https://webtools-lab.com/
