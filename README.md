## YouTube Subscription Backup

## 何ができるか
* YouTube アカウントに登録されているチャンネル一覧のバックアップを取得する.
* バックアップにあるチャンネル一覧を全て登録する.

## 使い方
* 準備
  1. パッケージインストール
  ```
  pip3 install google-api-python-client
  pip3 install oauth2client
  pip3 install httplib2
  ```
  2. [Google Cloud Platform](https://console.cloud.google.com/)でOAuth認証の準備を行い, OAuth クライアントの右端にあるダウンロードアイコンをクリックして、認証情報が含まれる JSON ファイルをダウンロードします.
  3. ダウンロードしたファイルを client_secrets.json として同じディレクトリ内に保存します.


* 登録しているチャンネル一覧からchannel_idを取得します.
  channel_id の一覧がバックアップファイル youtube-channel_id-list.txt に書き出されます.
  ```
  python get-susc-channel.py
  ```
* バックアップファイル youtube-channel_id-list.txt にある channel_id を全て目的のアカウントからチャンネル登録します.
  ```
  python insert-from-channel_id-list.py 
  ```

