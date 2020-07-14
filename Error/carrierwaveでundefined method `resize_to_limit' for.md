# carrierwaveを使っている時にundefined method `resize_to_limit' for
## 考えられる原因
 - MiniMagickかRmagickがインストールされているかGemfile.lockを確認する
   - インストールされていない場合はインストール
 - 作成したuploaderファイルで上記のGemをインクルードしているか確認する
   - ploaderファイルでインクルードされていない場合は以下を参考にインクルード

```
class HogeUploader < CarrierWave::Uploader::Base
  # Include RMagick or MiniMagick support:
  # include CarrierWave::RMagick
  # include CarrierWave::MiniMagick

  # 上記の２行のインクルードの内、インストール済みのどちらかのコメントアウトを外す
```
