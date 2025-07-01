# 🖨️ プリントファイル配置ガイド

このフォルダには3Dプリント関連のファイルを配置します。

## Gコードファイル
スライス済みの印刷用ファイル：

### ファイル命名規則
`部品名_材料_設定_プリンター.gcode`

### 例
- `storage-box-main_PLA_standard_Neptune4Pro.gcode`
- `storage-box-main_PETG_high-quality_Neptune4Pro.gcode`
- `storage-box-lid_PLA_standard_Neptune4Pro.gcode`

## スライサー設定ファイル
設定を共有するためのプロファイル：

### Cura用
- `Neptune4Pro_PLA_Standard.curaprofile`
- `Neptune4Pro_PETG_HighQuality.curaprofile`

### PrusaSlicer用
- `Neptune4Pro_PLA_Standard.ini`
- `Neptune4Pro_PETG_HighQuality.ini`

## プリント記録
実際のプリント結果を記録：

### print-log.md の内容例
```markdown
# プリント記録

## 2025-07-01 - storage-box-main v1.0
- 材料: eSUN PLA+ (グレー)
- 設定: 標準品質
- 時間: 3時間45分
- 結果: 成功
- 注意点: 初層がわずかに浮き気味、次回ベッド温度+5℃

## 2025-07-02 - storage-box-lid v1.0  
- 材料: eSUN PLA+ (グレー)
- 設定: 高品質
- 時間: 2時間20分
- 結果: 成功
- 注意点: 完璧な仕上がり
```

## ファイルサイズ注意
- Gコードファイルは数MB～数十MBになることがあります
- GitHubの単一ファイル100MB制限に注意
- 必要に応じてGit LFS使用を検討

## 推奨しないファイル
以下は.gitignoreで除外済み：
- *.tmp, *.temp - 一時ファイル
- *.backup* - バックアップファイル
- 実験的なファイル（テスト印刷用など）

## バージョン管理
設定変更時は新しいファイル名で保存：
- v1.0 → v1.1 → v2.0
- 重要な変更点はprint-log.mdに記録