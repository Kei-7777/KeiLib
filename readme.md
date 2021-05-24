# KeiLib.java
## made by Kei
## Features

競技プログラミングライクなライブラリです。
1ファイル完結で動くので自分のプラグインのパッケージを通すだけで使えます。
メソッド名は適当ですが、ファイルを短くすることに特化したライブラリなので、理解してください。

## Tech

KeiLib#psm(org.bukkit.entity.Player p, String... s);
```java
KeiLib.psm(player, "message1", "message2", "message3");
```
> メッセージをプレイヤーに表示します。  
 第２引数以降は複数引数を指定可能です。  
第２引数以降は別のStringとしてメッセージ送信の処理を行います。  
>(内部処理stream -> forEach)  
