# 情報提供仕様

![IDSロゴ](../Documentation/ids-logo.png)

**情報提供仕様（IDS：Information Delivery Specification）** は、IFCモデルからの単純な情報要件を指定および確認するためのbuildingSMARTの標準です。これは、モデルチェックのための無料で軽量な標準化されたアプローチとして設計されています。

## 導入

IDSは`.ids`で終わるファイル形式で、情報**仕様**のリストを含んでいます。例えば、単一の**仕様**では「_すべての壁には耐火性能のプロパティが必要です_」と言うかもしれません。IDSファイルを受け取ったモデルの著者は、各**仕様**に必要な情報が提供されていることを確認するためにそれを使用できます。モデルの受取人は、IFCモデルがすべての**仕様**を満たしているかどうかをチェックするためにIDSファイルを使用できます。また、**仕様**の遵守チェックの結果をリストするレポートも生成できます。

![IDS図](../Documentation/ids-diagram.png)

IDSファイル作成ツールとモデルチェックツールは、多くの[ソフトウェアベンダー](https://technical.buildingsmart.org/resources/software-implementations/)によって提供されています。独自のカスタマイズされたIDS**仕様**を一から作成するか、[公開IDSテンプレート](todo)から開始することができます。任意のソフトウェアから生成された任意のIFCモデルは、IDSファイルによってチェックすることができます。

## 初心者チュートリアル

1. IDSをサポートしているソフトウェアベンダーディレクトリから、お気に入りのソフトウェアを[ダウンロードしてインストール](https://technical.buildingsmart.org/resources/software-implementations/)してください。Windows、Mac、Linux用のソフトウェアが利用可能です。
2. [サンプルIDSファイルをダウンロード](library/sample.ids)します。このIDSファイルには2つの**仕様**があります。最初の仕様では_プロジェクト名はTESTであるべき_と指定されています。2つ目の仕様では_すべての壁に耐火性能のプロパティが必要_と指定されています。
3. [チェックするサンプルIFCモデルをダウンロード](library/sample.ifc)します。このIFCモデルにはプロジェクト名に"TEST"があり、最初の**仕様**を満たしています。しかし、いくつかの壁には耐火性能のプロパティがあり、他にはありません。
4. ソフトウェアでIDSとIFCの両方をロードし、チェックプロセスを開始します。

それだけです！[buildingSMART IDSテンプレートディレクトリ](https://github.com/buildingSMART/IDS/tree/master/Development)でさらに多くのサンプルIDSテンプレートや、[buildingSMART IFCモデルディレクトリ](https://github.com/buildingSMART/Sample-Test-Files)でさらに多くのサンプルIFCモデルを見つけることもできます。

助けが必要な場合は、[buildingSMARTフォーラム](https://forums.buildingsmart.org/)で遠慮なく質問してください。

## IDSについて学び始める

1. [**仕様**はどのように機能するのか？](specifications.jp.md)
1. [良い**仕様**メタデータの指定に関するガイドライン](ids-metadata.jp.md)
1. [**複雑な制約**の指定方法を学ぶ](restrictions.jp.md)
1. [**エンティティファセット**の使用方法を学ぶ](entity-facet.jp.md)
1. [**属性ファセット**の使用方法を学ぶ](attribute-facet.jp.md)
1. [**分類ファセット**の使用方法を学ぶ](classification-facet.jp.md)
1. [**プロパティファセット**の使用方法を学ぶ](property-facet.jp.md)
1. [**材料ファセット**の使用方法を学ぶ](material-facet.jp.md)
1. [**PartOfファセット**の使用方法を学ぶ](partof-facet.jp.md)
1. [ソフトウェア開発者ですか？開発者ガイドを読む！](developer-guide.jp.md)
