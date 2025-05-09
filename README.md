#  Ruby 標準ライブラリ logger の読み込み漏れ
Railsは標準ライブラリの Logger に依存していますが、Ruby 3.0以降では logger が明示的に require されていないと使えない 場合があります。

解決策1：logger を明示的に読み込む
プロジェクトの config/boot.rb の先頭あたりに以下を追加
```config/boot.rb
require 'logger'
```
