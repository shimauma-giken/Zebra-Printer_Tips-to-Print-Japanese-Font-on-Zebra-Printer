#### Zebra-Printer_Tips-to Print Japanese Font on Zebra Printer

# まとめ：Zebra プリンタで利用できる日本語フォント一覧

Updated: 2024/10/14


<img height="700" src="https://images.unsplash.com/photo-1512580526143-1f24419088a3?q=80&w=1976&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">

<br>


ゼブラプリンタには利用シーンに応じて適切なフォントが利用できるように多くのプリンタ内蔵フォントが用意されている。
コスト・スペックに応じて、適したフォントを選択すること。

- サードパーティ製フォントを用いた印刷はメーカのフルサポートが受けられないため、実機検証の上で利用可否を判断すること。

<br>

| SKU | File Name | Type | Description | Where to Get | 
| --- | --- | --- | --- | --- |  
| 56068-002      | ANMDJ.TTF    | Gothic | Scalable Font Pack Andale Japanese | Purchaseable online* 
| 77840-002      | GOTHIC24.FNT | Gothic | JA Bitmap Gothic font for 203dpi | Purchasable online*
| 77840-002      | MINCHO24.FNT | Mincho | JA Bitmap Mincho font for 203dpi | Purchasable online*
| 77841-002      | GOTHIC35.FNT | Gothic | JA Bitmap Gothic font for 300dpi | Purchasable online*
| 77841-002      | MINCHO35.FNT | Mincho | JA Bitmap Mincho font for 300dpi | Purchasable online*
| 77848-002      | GOTHIC.FNT   | Gothic | Scaleable Font Pack, Japanese HGP Gothic B | Purchasable online*
| -              | JIS.DAT      | -      | JA JIS/S-JIS Font Map | Downloadable from zebra.com*
| -              | SGMTJ.TTF    | Gothic | JA Scaleble Gothic font | Downloadable from zebra.com*
| -              | NOTOMRJ.TTF  | Gothic | JA Scaleble Gothic font | Downloadable from zebra.com*
| -              | GT16NF55.CPF | Gothic | JA Bitmap Gothic font (16dots) | Pre-installed font**
| -              | GT24NF55.CPF | Gothic | JA Bitmap Gothic font (24dots) | Pre-installed font**
| -              | xxxxx.TTF    | - | 3rd Party TTF Font | 

\* [zebra.com: Fonts for Zebra Printers](https://www.zebra.com/us/en/support-downloads/software/printer-software/printer-fonts.html)
\** 一部のモバイルプリンタにプリンインストールされている

###### 参考
[NOTOMRJ--SGMTJの入手とインストール方法](https://github.com/shimauma-giken/Zebra-Printer_How-to-download-and-install-NOTOMRJ--SGMTJ-fonts)


<br>
<br>

# フォント/プログラミング言語対応表

<img height=500 src="https://images.unsplash.com/photo-1557324232-b8917d3c3dcb?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">

<br>

プリンタやプログラミング言語によって使用できるフォントが異なるため、下記表を参考に適した印刷環境を構築すること。
特にLink-OS Basicは日本語フォント利用にあたって、制限が多いので注意が必要である。

<br>

| SKU | File Name | ZPL/Link-OS | CPCL/Link-OS | CPCL/Link-OS Basic |
| --- | --- | :---: | :---: | :---: |  
| 56068-002      | ANMDJ.TTF    |  x | x | 
| 77840-002      | GOTHIC24.FNT |  x |  | 
| 77840-002      | MINCHO24.FNT |  x |  | 
| 77841-002      | GOTHIC35.FNT |  x |  | 
| 77841-002      | MINCHO35.FNT |  x |  | 
| 77848-002      | GOTHIC.FNT   |  x |  | 
| -              | JIS.DAT      |  x | x | x
| -              | SGMTJ.TTF    |  x | x | 
| -              | NOTOMRJ.TTF  |  x | x | 
| -              | GT16NF55.CPF |  x | x | x
| -              | GT24NF55.CPF |  x | x | x
| -              | xxxxx.TTF    |  x* |   |

\* サードパーティ製フォントを用いた印刷はメーカのフルサポートが受けられないため、実機検証の上で利用可否を判断すること。

<br>
<br>

# フォントインストール方法

<img height=500 src="https://images.pexels.com/photos/577585/pexels-photo-577585.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1">

<br>
インストール方法についてはフォント付属のガイドに従って実施すること。
また、内蔵フォントにフォントを格納するための空き容量があるか確認すること。

###### 参考
[NOTOMRJ--SGMTJの入手とインストール方法](https://github.com/shimauma-giken/Zebra-Printer_How-to-download-and-install-NOTOMRJ--SGMTJ-fonts)
[USBメモリを利用してAndaleフォントをプリンタにインストールする方法](https://github.com/shimauma-giken/Zebra-Printer_Andale-Japanese--font-installer-for-Zebra-printer-by-USB-thumb-drive)
[ゼブラプリンタにIPA 明朝/ゴシックフォントをインストールする方法](https://github.com/shimauma-giken/Zebra-Printer_IPA-Japanese--font-installer-for-Zebra-printer-by-USB-thumb-drive)


<br>
<br>

# プリンタ内蔵のフォント確認・内蔵ドライブ空き容量確認方法

<img height=500 src="https://images.pexels.com/photos/33278/disc-reader-reading-arm-hard-drive.jpg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1">

<br>

下記コマンドにて確認すること。

<br>

##### Link-OS 

<pre>
! U1 do "file.dir" "E"

 "
- DIR E:*.* 
* E:ANMDJ.TTF  22927536    ★      
* E:DEMO01.ZPL      1034          
* E:GOTHIC24.FNT    536450 ★         
* E:GT16NF55.CPF    310457 ★         
* E:GT24NF55.CPF    606448 ★         
* E:NOTOMRJ.TTF  18257232  ★        
* E:SGMTJ.TTF   4248848    ★      
* E:TT0003M_.TTF    169238 ★        
* E:ZBI.NRD      2048  P       

-  87156224 bytes free E: ONBOARD FLASH 
</pre>

<br>

##### Link-OS Basic

<pre>
! U1 getvar "file.dir" 

"  Directory
   LOWPOWER.WML       189
   INDEX   .WML       853
   INFO_TIM.WML       426
   INFO_ACK.WML       393
   CONFIG  .WML      3488
   ICON    .CPF      5084
   NSMTTC16.CPF    909344
   DEJAVU12.CPF      5323
   DEJAVU14.CPF      7001
   DEJAVU16.CPF      8183
   DEJAVU20.CPF     10288
   SWIS721 .CSF     22219
   GT16NF55.CPF    310456　★
   GT24NF55.CPF    606448　★
   SGMTJ.TTF   4248848　★
   JIS     .DAT     28232
   8208000 Bytes Free
</pre>


<br>
<br>

# 内蔵フォントを利用して日本語を印刷する方法

<img height=500 src="https://images.pexels.com/photos/4440798/pexels-photo-4440798.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1">

<br>

## Zebra Designer 3 を用いた印刷

ZD3ではZPL/TTFの組み合わせのみサポートしている。詳細な手順は下記リンクを確認すること。
<br>

###### 参考
[Zebra Designer 3でプリンタ内蔵の日本語フォントを利用する方法](https://github.com/shimauma-giken/Zebra-Printer-Add-Japanese-Font-to-Windows-Driver-to-Utilize-in-Zebra-Designer)
[ZebraDesigner3でサポートされているフォント](https://github.com/shimauma-giken/Zebra-Printer_Supported-Japanese-fonts-on-ZebraDesigner3-)
[3rdパーティフォントをZebra Designer 3 で利用する方法](https://github.com/shimauma-giken/How-to-print-3rd-party-TTF-fonts-on-Zebra-Designer-3-)


<br>
<br>

## プログラミング言語を用いた印刷

アプリやPLCから印刷指示を送信する場合はプログラミング言語による印刷が多用される。
コードの詳細については各プログラミングガイドをzebra.comからダウンロードし、確認すること。
また、スクリプトコードををプリンタに送信する場合、矛盾した文字コードとならないように気を付けること。

<br>

### ZPL+TTF を用いた印刷（UTF-8）

#### サンプルコード

<pre>
^XA   
^FT39,105^A@N,21,21,ANMDJ.TTF^FH\^CI28^FDZ Andale J フォント^FS^CI27  
^FPH,1^FT39,171^AJN,50,50^FH\^CI28^FDZ Ja Gothic フォント^FS^CI27  
^FPH,1^FT42,239^AJN,50,50^FH\^CI28^FDZ Ja  Mincho フォント^FS^CI27  
^FPH,1^FT49,329^A@N,50,50,SGMTJ.TTF^FH\^CI28^FDZ MS Gothic フォント^FS^CI27  
^FPH,1^FT49,418^A@N,50,50,NOTOMRJ.TTF^FH\^CI28^FDZ Noto Sans フォント^FS^CI27  
^FPH,1^FT42,562^A@N,50,49,TT0003M_^FH\^CI28^FDZ Swiss Fonts^FS^CI27  
^XZ  
</pre>

<br>

### CPCL+TTF を用いた印刷（UTF-8）

#### サンプルコード

<pre>
! 0 200 200 600 1
COUNTRY UTF-8
SCALE-TEXT ANMDJ.TTF 	016 016 010 010 アンデール 
SCALE-TEXT NOTOMRJ.TTF 	016 024 010 050 NOTOMRJ.TTF フォント
SCALE-TEXT SGMTJ.TTF  	024 016 010 130 SGMTJ.TTF フォント
PRINT
</pre>

<br>


### CPCL+CPFを用いた印刷 (Shift-JIS)

#### サンプルコード

<pre>
! 0 200 200 200 1
; Set the country
COUNTRY JAPAN-S
; Print CPF fonts
TEXT GT16NF55.CPF 0 0 0 サイズ16
TEXT GT24NF55.CPF 0 0 30 サイズ24
PRINT
</pre>

<br>

------

<font size=1>
<br>
<br>

# 免責事項   

以下の内容について一切その責任を負いません。あらかじめご了承ください。   
  
1. 本ファイルは利用者の責任において本規約に基づき利用されるものとし、情報配信元は本規約に明示的に定められている場合を除き、本ファイルの利用について責任を負いません。   
2. 情報配信元は提供する本ファイルが正常に作動することおよび将来にわたり正常に作動すること、ならびに、本ファイルが全てのプリンタや運用環境において利用できることを保証しません。   
3. 本ファイルが正常に作動しないことおよび本ファイルが利用できないことによりお客様が損害を被った場合、情報配信元は当該損害に関して一切責任を負いません。   
5. 利用者の本ファイルの利用にあたり、運用データが破壊、消失または変更された場合、情報配信元は一切責任を負いません。   
7. 情報配信元は、利用者が本ファイルを通じて得た情報等につき、その正確性および特定の目的への適合性等について、いかなる保証もしません。   
7. 情報配信元は、利用者が他の利用者あるいは第三者との間に本ファイルを通じて提供された情報によって生じた権利侵害等の紛争に関して一切責任を負いません。   


</font>

