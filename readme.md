# KeiLib.java
## made by Kei
## Features

競技プログラミングライクなライブラリです。
1ファイル完結で動くので自分のプラグインのパッケージを通すだけで使えます。
メソッド名は適当ですが、ファイルを短くすることに特化したライブラリなので、理解してください。

## Tech

Player Send Message  
KeiLib#psm(org.bukkit.entity.Player p, String... s);
```java
KeiLib.psm(player, "message1", "message2", "message3");
```
> メッセージをプレイヤーに表示します。  
 第２引数以降は複数引数を指定可能です。  
第２引数以降は別のStringとしてメッセージ送信の処理を行います。  
>(内部処理stream -> forEach)  

Random pick a online player  
KeiLib#p1p();  
```java
org.bukkit.entity.Player player = KeiLib.p1p();
```
> サーバーにいるプレイヤーからランダムで一人を取得します。  

sender Permission check  
KeiLib#pexc(org.bukkit.command.CommandSender sender);  
```java
// OnCommand (CommandExecutor)
if(KeiLib.pexc(sender)) return true; // OP以外を弾く
```
> CommandSenderがOP以外のときにtrueを返します。  
"権限がありません"のメッセージも追加で送信します。  
> コマンドの処理でOP以外を弾く際にメッセージを同時に送信するのがめんどくさいため作成。  
