## dependencies
- hugo

## how to build
```
> hugo
```

## develop
```
> hugo server --bind=0.0.0.0
```
をして、http://localhost:1313 にアクセス
ファイルを変更すると自動リロードされるが、そのときにスクロールバーの位置が変わってしまう。
それを避ける場合は http://localhost:1313/ja/beginning のように
パスを指定してアクセスするとよい。ただしこの場合はサイドバーが機能しない。
