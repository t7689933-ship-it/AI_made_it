# Task TODO

- [x] Plan: 重要経路（集計計算・進行計算）を確認して不具合候補を抽出
- [x] Execute: バグを最小差分で修正
- [x] Verify: 再現/検証コマンドを実行
- [ ] Report: 変更内容と検証結果を報告

## Progress Log
- 2026-03-07: `game/engine.js` の集計関数を確認し、実績ボーナス適用コードより前に `return` しているため、実績効果が恒久計算に反映されない不具合を特定。
- 2026-03-07: 早期 `return` を削除し、実績ボーナス適用後の `return` のみが実行されるよう修正。

## Verification Log
- 2026-03-07: `node --check game/engine.js && node --check game/ui.js && node --check game/state.js && node --check game/config.js` を実行し、全ファイルの構文チェック通過。
