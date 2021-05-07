## YouTube Subscription Backup

## 何ができるか
* YouTube アカウントに登録されているチャンネル一覧のバックアップを取得する.
* バックアップにあるチャンネル一覧を全て登録する.

## 使い方
* 準備
  ```
  pip3 install google-api-python-client
  pip3 install oauth2client
  pip3 install httplib2
  ```
* YouTube アカウントで登録しているチャンネル一覧からchannel_idを取得します.
  ```
  python get-susc-channel.py
  ```
  channel_id 一覧を バックアップファイル youtube-channel_id-list.txt に書き出します.
* バックアップファイル youtube-channel_id-list.txt にある channel_id を全て目的のアカウントに登録します.
  ```
  python insert-from-channel_id-list.py 
  ```

