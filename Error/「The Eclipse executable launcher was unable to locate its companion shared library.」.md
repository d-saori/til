# WindowsPCでeclipseの設定時にエラー「The Eclipse executable launcher was unable to locate its companion shared library.」発生

- このエラーは「Eclipseを起動するために必要なファイルが見つからない」のが原因
- 解凍先フォルダ名が長すぎると、解凍に失敗するケースがある
  - 例）「マイドキュメント」フォルダ、「ダウンロード」フォルダ

# 解決法
- Eclipseのzipファイルを「ダウンロード」フォルダ内ではなく、「C:¥」直下で解凍する
