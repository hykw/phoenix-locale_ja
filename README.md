# phoenix-locale_ja
Phoenix Framework のエラーメッセージを日本語訳した .po ファイルです。
2015/12/31 の master(9765d52)のen/LC_MESSAGES/errors.po を元にしています。

[本家にプルリク](https://github.com/phoenixframework/phoenix/pull/1441) しましたが、 `we don't plan to host different translations.` とのことなので、ここに置いておくことにします。

# 利用方法
・ja/LC_MESSAGES/errors.po ファイルを `priv/gettext/` 以下、つまり `priv/gettext/ja/LC_MESSAGES/errors.po` として設置します

・config/config.exs に下記のような行を追加します。

```elixir
config :my_app, MyApp.Gettext, default_locale: "ja"
```

例えばチュートリアルのように HelloPhoenix というプロジェクトを作成しているのであれば、このようになります。

```elixir
config :hello_phoenix, HelloPhoenix.Gettext, default_locale: "ja"
```

この locale の設定方法は、Stack Overflow で [How to set locale for errors.po?](http://stackoverflow.com/questions/34538502/how-to-set-locale-for-errors-po) という質問をした時に José Valimから直接教えてもらった方法なので、ほぼ公式な設定方法と考えていいのではないかと。
