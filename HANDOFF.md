# 愛犬LP 受け渡しメモ（村松さん向け）

> 2026-06-12 作成 / 6/10 MTG合意フロー: RayがHTML納品 → 村松さんがWordPressに流し込み → 崩れが大きければRayが修正、軽微なら村松さんが微調整

## 1. WordPress流し込み手順

コピーするのは以下の3ブロックです（`index.html` 内）。

1. **Google Fonts 読み込み**（`<head>` 内の3行）
   ```html
   <link rel="preconnect" href="https://fonts.googleapis.com">
   <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
   <link href="https://fonts.googleapis.com/css2?family=Kiwi+Maru:wght@400;500&family=Noto+Sans+JP:wght@400;500;700;900&display=swap" rel="stylesheet">
   ```
2. **`<style>` ブロック全体**（CSSは `.tenku-dog-lp` で名前空間化済み。テーマCSSと衝突しにくい設計です）
3. **`<div class="tenku-dog-lp dog-lp">` 〜 `</div>` の本文全体** ＋ 末尾の **`<script>`（スクロールフェードイン用）**

- デザイン基準: デイグランピングLP（`.daytrip-bbq-lp`）と同じ作りを踏襲しています
- `<meta name="robots" content="noindex">` はモック用です。**本番公開時は外してください**

## 2. 画像

- `lp-assets/dog/` 一式（13枚・Web最適化済み）をWordPressメディアへアップロード
- HTML内の `lp-assets/dog/〜.jpg` をアップロード後のURLに一括置換してください

## 3. 設定済みの内容（確認だけお願いします）

- **予約CTA**: 公式「愛犬とグランピング」ページ（scene/dog）と同じ予約エンジンURLを設定済み
  `https://booking.kobetenku.com/booking/result?code=cac51cdc-8dd0-4d1f-8f4b-8f8aa29fee4c`
- **面積表記**: 公式ページに合わせて「250㎡＝お部屋＋お庭の貸切空間」「約690㎡＝共用ドッグラン」で統一済み

## 4. 残TODO（公開前に差し替え・確認が必要なもの）

| # | 項目 | 状態 |
|---|------|------|
| 1 | **「ペット追加料金0円」の条件**（大型犬2頭・3頭以上で追加発生の可能性） | 現場確認中。HTML内 `<!-- 要確認 -->` でマーク済み（チップ・料金表・FAQの3箇所） |
| 2 | ヒート中の受け入れ条件 | 「事前相談」とぼかして記載中 |
| 3 | 夜間救急動物病院の案内掲載可否 | 神戸夜間動物救急センターを記載中。NG なら削除 |
| 4 | キャンセル規定 | 「プランごと」の前提で記載。固定規定があれば差し替え |
| 5 | 口コミ3件 | **仮テキスト**。実際のGoogleクチコミに差し替え要 |
| 6 | 「撮影待ち」プレースホルダー5枚（大型犬/備品実物/エアコン/夕方ラン/ウェルカムボード） | 撮影リスト: `2026-05-29_ワンちゃんLP_撮影・素材リスト.md` |

## 5. プレビュー

GitHub Pages（noindex・URLを知る人のみ）で最新版を確認できます。
