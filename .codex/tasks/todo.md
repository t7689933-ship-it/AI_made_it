# TODO

## Plan
- [x] 既存のバランス・Ascension・ショップ・購入処理の構造確認
- [x] 種銭系 / +GPS系 / ジュニア採掘機・採掘機強化 / 序盤エクスカベーター弱体化
- [x] Ascend時の累計ゴールド・レガシーツリーのリセット導入
- [x] Ascensionショップ拡充（維持解放・開始資金強化・追加GPS強化）
- [x] Ascensionの新機能拡充（自動購入の解放トリガーを追加）
- [x] 自動購入機能（UI設定 + 実行ループ）
- [x] 検証ログ記録

## Progress Log
- config.js: ユニット序盤バランスを調整（ジュニア/採掘機強化、エクスカベーター序盤弱体化）。
- config.js: 種銭系・GPS系の恒久強化を拡張し、Ascensionショップへ特殊解放を追加。
- engine.js: Ascend時に累計ゴールド/レガシーツリーをリセット、Ascensionショップ購入で維持可能に実装。
- ui.js / index.html: 自動購入機能を追加し、Ascensionショップ購入で解放される設計に実装。
- state.js: 自動購入設定の保存項目を追加。

## Verify Log
- `node --check game/config.js && node --check game/state.js && node --check game/engine.js && node --check game/ui.js` : 成功
- スクリーンショット取得を browser tool + Playwright で試行したが、`run_playwright_script` がタイムアウトし取得不可
