# memo

__iOS9 まで対応する場合__  

iphone4sまで対応が必要  
iphone4s は armv7。iphone5から armv7s  
armv7, armv7s, arm64 の3つを含むとバイナリサイズが大きい  
armv7sは iphone5, iphone5c のみなので、armv7, arm64 だけにしても影響が少ない  

__xcrun__  

/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin 以下にある（他も？）各種デベロッパーツールを実行するツール。なぜ直接パスを通さないのか？ 多分、複数のxcodeのバージョンを切り替えて作業できるように、である。

__xcrun lipo__

複数のアーキテクチャのライブラリをまとめる、または含まれているアーキテクチャを調べる  
```
xcrun -sdk iphoneos lipo -create build/Release-iphonesimulator/りぶあああ.a build/Release-iphoneos/libsia.a -output build/Release-universallib/りぶあああ.a
```
