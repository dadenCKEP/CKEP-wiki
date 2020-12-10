---
title: "Plugin"
date: 2020-02-27T02:17:55+09:00
draft: false
---

Blenderで使っているプラグインメモ。バックアップ代わりに。

## Cats関連
* [cats-blender-plugin](https://github.com/michaeldegroot/cats-blender-plugin/)  
    アバター最適化等
  * [mmd_tools](https://github.com/sugiany/blender_mmd_tools)  
    MMD関連ファイルの扱いに必要
    * https://github.com/powroupi/blender_mmd_tools こっちのほうがよい？
  * [material-combiner-addon](https://github.com/Grim-es/material-combiner-addon)  
    マテリアル統合に必要
  * [VRM_IMPORTER_for_Blender](https://github.com/saturday06/VRM_IMPORTER_for_Blender)  
    VRMインポートに必要(catsの対応は0.17.0の1つ後から)

## ウェイト関連
* [Blenderでウェイトのない頂点グループをすべて削除する](https://scrapbox.io/keroxp/Blender%E3%81%A7%E3%82%A6%E3%82%A7%E3%82%A4%E3%83%88%E3%81%AE%E3%81%AA%E3%81%84%E9%A0%82%E7%82%B9%E3%82%B0%E3%83%AB%E3%83%BC%E3%83%97%E3%82%92%E3%81%99%E3%81%B9%E3%81%A6%E5%89%8A%E9%99%A4%E3%81%99%E3%82%8B)
  * (自分で2.8対応)
  * 同等の機能は後述の`Blender-CM3D2-Converter`にもある。

## テクスチャ関連
* [TexTools](http://renderhjs.net/textools/blender/)
  * 非公式2.8対応版: https://github.com/SavMartin/TexTools-Blender (OSSだし非公式とは…)
* [AutoReloadImage](https://yukimi-blend.blogspot.com/2019/12/blog-post.html)
  * 外部ツールでテクスチャを更新するとBlender側でリロードするアドオン

## 追加メッシュ関連
* [ハートのメッシュを作成するスクリプト(Add on)](https://blender.jp/modules/newbb/index.php?topic_id=1341)
  * (自分で2.8対応)

## 法線関連
* Yet Another Vertex Normal Editor (Y.A.V.N.E.)
  * https://github.com/fedackb/yavne
  * 頂点法線をいい感じにする

## 総合系
* https://github.com/mifth/mifthtools  
  * MiraTools - https://blenderartists.org/t/miratools/637385
  * MifthTools - https://blenderartists.org/t/mifthtools-addon/619227
* Blender-CM3D2-Converter
  * https://github.com/trzr/Blender-CM3D2-Converter
  * おまけ機能が非常に便利

## 有料プラグイン
* [Auto-Rig Pro](https://blendermarket.com/products/auto-rig-pro)
  * http://www.lucky3d.fr/auto-rig-pro/doc/
* [Better Fbx Importer & Exporter](https://blendermarket.com/products/better-fbx-importer--exporter)
  * http://www.mesh-online.net/fbx.html
  * 主にインポート用。Maya等で作成したFBXファイルを正しく読むことができる。
* [Pro Align Tools](https://blendermarket.com/products/pro-align-tools)
* [Simply Cloth](https://gumroad.com/l/vpzMx)
  * https://modelinghappy.com/archives/25222
* [Voxel Heat Diffuse Skinning](https://blendermarket.com/products/voxel-heat-diffuse-skinning)
  * http://www.mesh-online.net/voxel.html
* [Uvpackmaster 2](https://blendermarket.com/products/uvpackmaster2)
  * https://uvpackmaster.com/uvpackmaster-for-blender/

## リトポ関連
* [EdgeFlow](https://github.com/BenjaminSauder/EdgeFlow)
* [Poly Source](https://gumroad.com/derksen#mNvmS)

## 標準プラグイン
* Archipack
* Archimesh
* Auto Mirror
  * [Blender Addon : Auto Mirror [Blender2.8ver]](https://gumroad.com/l/vgRSB)  
    有志2.8対応版
* Cell Fracture
* Extra Objects
  * CurveとMeshの2つがある
* F2
* LoopTools
