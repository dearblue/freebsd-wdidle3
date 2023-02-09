wdidle3 for FreeBSD
=======

camcontrol を用いて Western Digital 製のハードディスクの省電力機能を設定します。

設定できるのは SATA 接続されているディスクのみです。
USB-SATA ブリッジを介したディスクは設定できません。

***だいじなおやくそく***
-------

  - ***このプログラムを理解せずに使うと、パソコンが超新星爆発します。***
  - ***このプログラムはまともなテストを行っていません。***
  - ***他メーカー製品や、Western Digital 製でも未対応の製品に対して行った場合、どうなるか分かりません。***

くみこみかた
-------

システムへ追加する場合は次のようにすると良いでしょう。

```console
% sudo install wdidle3 /usr/local/sbin/
```

自分専用のパスへ追加しても良いでしょう。

```console
% install -d wdidle3 ~/bin/
```

つかいかた
-------

`/dev/ada999` の設定値を確認する:

```console
% wdidle3 ada999
wdidle3: 80 for ada999
```

`/dev/ada999` の設定値を変更する:

```console
% wdidle3 ada999 255
wdidle3: 80 -> 255 for ada999
```

設定値を有効化するために、一度コンピュータの電源を切断、あるいはデバイスの電源を切断して下さい。
コンピュータの再起動では有効化されません。

さんこうしりょう
-------

  - <https://www.truenas.com/community/threads/18171/post-274687>
  - <https://idle3-tools.sourceforge.net/>

諸元
-------

  - Package Name: wdidle3
  - Product Status: CONCEPT
  - Author: [dearblue](https://github.com/dearblue)
  - Project page: <https://github.com/dearblue/freebsd-wdidle3>
  - Licensing: [Creative Commons Zero License (CC0; Public Domain)](LICENSE)
  - Dependency Packages: `sudo`
