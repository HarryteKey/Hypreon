# Hypreon ビルドガイド

このビルドガイドの画像に出てくるパーツは、製品版と異なる場合があります

## 入っている部品

| 名前 | 数 | 備考 |
| ---- | ---- | --- |
| PCB | 2枚 | 緑基板 |
| トッププレート | 2枚 | 黒基板 |
| ボトムプレート | 1枚 | アクリル |
| M2スペーサー 3.5mm | 12個 | ネジ山あり |
| 中空スペーサー 2mm | 12個 | ネジ山なし |
| M2ネジ 8mm | 12個 | |
| M2ネジ 4mm | 12個 | |
| ワッシャー | 24個 | |
| ゴム足(大) | 4個 | |
| ゴム足(小) | 4個 | |

![Imgur](https://user-images.githubusercontent.com/52162386/135728342-e50f9885-ff26-4007-8fe0-8d173e92a0dd.jpg)

## 用意していただく部品

| 名前 | 数 | 備考 |
| ---- | ---- | --- |
| キースイッチ(Cherry MX) | 58～60個 | 片側で3箇所3pinのみ対応(5pinのキースイッチは足をカットする必要があります) |
| キーキャップ | | |
| TRRSケーブル | 1本 | 左右のキーボード間接続用 |
| USB-C ケーブル | 1本 | PCとの接続用 |

## 必要な道具

| 名前 | 備考 |
| ---- | ---- |
| プラスドライバー | |
| (任意)マスキングテープ | 組立時ネジの固定用 |

# 組み立て方

## トッププレートをつける

トッププレートの"Hypreon Keyboard"と書かれている面から、ワッシャーとM2 4mmネジを取り付けます

プレートの裏側からM2 3.5mmスペーサーを取り付けます

![Imgur](https://user-images.githubusercontent.com/52162386/135728364-3b41691a-55a7-4b7a-a258-f88fa2b21ed0.jpg)

## キースイッチをつける

トッププレートとPCBを重ね、キースイッチをはめ込みます

この時、PCB裏側のソケットを抑えながらスイッチをはめ込むとソケットが破損する可能性が低くなります

![Imgur](https://user-images.githubusercontent.com/52162386/135728425-0df4ea65-b645-49f9-a2a1-fef0a121e585.jpg)

なお、以下の図でキースイッチがはめ込まれていない部分は3pinのキースイッチのみ対応しています

![Imgur](https://user-images.githubusercontent.com/52162386/135728407-3f90f4cc-d631-460a-9817-93b32bd16785.jpg)

この部分に5pinのキースイッチを使用する場合、足をカットしてください

![Imgur](https://user-images.githubusercontent.com/52162386/135728414-12cb0108-20e3-4afa-969d-bee25a70ad8d.jpg)

## ボトムプレートをつける

ゴム足をボトムプレートの彫刻が無い面に貼ります。この作業は組み立ての最後に行っても構いません。

![Imgur](https://user-images.githubusercontent.com/52162386/135728439-dfb05b0f-f66e-44be-83f8-9c25ebda679a.jpg)

ボトムプレートの彫刻が無い面から、ワッシャーとM2 8mmネジを取り付けます

ネジの頭をマスキングテープ等で固定し、プレートの裏側から中空 2mmスペーサーを取り付けます

ボトムプレートをPCBにネジ止めします

![Imgur](https://user-images.githubusercontent.com/52162386/135728449-e39a4ef7-cfc0-4b21-a7f6-488e82060fc8.jpg)

## 完成

最後にキーキャップを取り付けて完成です

![Imgur](https://user-images.githubusercontent.com/52162386/135728468-83ed31ac-a6bd-4337-9d00-2e0bfe0ba173.jpg)

# ファームウェアについて

すぐに使えるよう、PCBにはファームウェアが書き込まれています

キーマップは以下の通りです

![Imgur](https://user-images.githubusercontent.com/52162386/135728469-81487bb0-bfba-498c-bfa6-fdbf870b8916.png)

## キーマップの書き換え

キーマップの書き換えにはRemapというWebソフトが利用できます。

事前に当リポジトリをクローンするか、Hex/Hypreon_via.jsonを[ダウンロード](Hex/Hypreon_via.json)(Rawボタンを押して右クリックで保存)しておき、Chromeで[Remap](https://remap-keys.app/)にアクセスします。(RemapはChromeのみ対応)

まず、"START REMAP FOR YOUR KEYBOARD"をクリックします。

![Imgur](https://user-images.githubusercontent.com/52162386/137341065-9d0c722c-c16a-44c9-8467-a4234f6c1f7a.png)

次の画面で出てきた"+ KEYBOARD"をクリックします。

![Imgur](https://user-images.githubusercontent.com/52162386/137341075-fe141c2e-0332-4571-93b6-6ceaa1f77770.png)

画面がポップアップするのでHypreonを選択し、"接続"をクリックします。

![Imgur](https://user-images.githubusercontent.com/52162386/137341093-42bfa3a7-0566-4b35-84fc-2f8a550df4d4.png)

RemapにHypreonのキーマップはマージされていないため、先程ダウンロードしたHypreon_via.jsonをドラックして読み込ませます。

![Imgur](https://user-images.githubusercontent.com/52162386/137341098-4e8b92e0-4750-4b50-b65a-475bab70f2b4.png)

キーマップ変更画面になるので好きなようにキーマップを変更します。

![Imgur](https://user-images.githubusercontent.com/52162386/137341109-048773e9-e45e-4236-b8f6-c87cf541b49f.png)

Remapの詳しい使い方については、"Remap 使い方"で検索すると出てくるのでそれを参考にしてください。