# CADファイル配置ガイド

このフォルダには以下のファイルを配置してください：

## Fusion 360ファイル
- `storage-box-main.f3d` - メインボックスの設計ファイル
- `storage-box-lid.f3d` - 蓋部分の設計ファイル（オプション）
- `storage-box-assembly.f3d` - アセンブリファイル

## 汎用交換フォーマット
- `storage-box-main.step` - 他CADソフトでも開けるSTEPファイル
- `storage-box-main.iges` - IGESファイル（古いソフト用）

## 3Dプリント用ファイル
- `storage-box-main.stl` - プリント用STLファイル
- `storage-box-lid.stl` - 蓋のSTLファイル

## ファイル命名規則
- プロジェクト名_部品名_バージョン.拡張子
- 例: `storage-box_main_v1.0.stl`

## Git LFS設定
大容量ファイル（.f3d, .step等）はGit LFSで管理されます。
初回コミット前に以下を実行：

```bash
git lfs track "*.f3d"
git lfs track "*.step"
git lfs track "*.iges"
```