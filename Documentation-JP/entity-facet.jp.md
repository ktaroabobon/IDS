# エンティティファセット

IFCモデルのすべてのエンティティには「IFCクラス」という**名前**があります。たとえば、壁エンティティにはIfcWallのIFCクラスがあり、ドアエンティティにはIfcDoorのIFCクラスがあります。個々の建築要素を表さないエンティティもクラスを持ちます。たとえば、プロジェクトにはIfcProjectのクラスがあり、窓タイプにはIfcWindowTypeのクラスがあり、コストアイテムにはIfcCostItemのクラスがあります。

クラスはエンティティを分類するだけでなく、どの種類のプロパティや関係が許可されているかも示します。たとえば、IfcWallクラスは火災評価プロパティを持つことができますが、IfcGridクラスは持つことができません。

異なるIFCスキーマには異なるIFCクラスがあります。より最近のIFCスキーマには、より豊かで多様なIFCクラスが含まれています。ここで比較できます：

- [IFC4X3のIFCクラス名のリスト](http://ifc43-docs.standards.buildingsmart.org/IFC/RELEASE/IFC4x3/HTML/annex-b1.html)
- [IFC4のIFCクラス名のリスト](https://standards.buildingsmart.org/IFC/RELEASE/IFC4/ADD2_TC1/HTML/link/alphabeticalorder-entities.htm)
- [IFC2X3のIFCクラス名のリスト](https://standards.buildingsmart.org/IFC/RELEASE/IFC2x3/TC1/HTML/alphabeticalorder_entities.htm)

一部のエンティティは、オプションで**事前定義タイプ**も持つことがあります。これは、**IFCクラス名**に加えてエンティティの分類をさらに行うレベルです。たとえば、IfcWallにはSHEARまたはPARTITIONINGの**事前定義タイプ**があるかもしれません。**IFCクラス名**はIFC標準によって指定されますが、**事前定義タイプ**にはユーザーによるカスタム値も含まれる場合があります。

IFCスキーマのドキュメントには、標準の事前定義タイプのリストが含まれています。ここでは、IFC4X3スキーマの有効な**事前定義タイプ**のリストを見つける方法を示します。すべてのIFCバージョンで指示は似ています。

1. 指定しているIFCクラスのドキュメントページに移動します。上記のIFCクラス名のリストからそこにたどり着くことができます。たとえば、[これがIfcWallのドキュメントページです](http://ifc43-docs.standards.buildingsmart.org/IFC/RELEASE/IFC4x3/HTML/lexical/IfcWall.htm)。
2. ドキュメントの**属性**セクションまでスクロールし、**PredefinedType**属性を見つけます。
3. **PredefinedType**属性の横の列挙リンクをクリックして、有効な値のリストを表示します。たとえば、IfcWallの場合、[IfcWallTypeEnumのドキュメント](http://ifc43-docs.standards.buildingsmart.org/IFC/RELEASE/IFC4x3/HTML/lexical/IfcWallTypeEnum.htm)に移動するリンクをクリックします。
4. 有効な**事前定義タイプ**のリストが表に表示されます。

標準化された**事前定義タイプ**のリストから選択することを強くお勧めします。ただし、プロジェクトに適用されない場合は、任意のカスタム値を指定できます。たとえば、**IfcWall**のカスタム**事前定義タイプ**として「RADIATIONBARRIER」を指定することができます。

仕様書を作成する際の最も重要な側面の1つは、それが適切なIFCクラスに適用されることを確認することです。通常、すべての単一の**仕様書**には、その**適用範囲**セクションで使用される**エンティティファセット**があります。

## パラメータ

| パラメータ            | 必須 | 制約許可 | 許可される値                                                         | 意味                                    |
| ------------------- | ---- | -------- | ---------------------------------------------------------------------- | ------------------------------------------ |
| **名前**            | ✔️   | ✔️      | IFCスキーマからの有効なIFCクラス。                                  | IFCクラスは正確に一致しなければなりません |
| **事前定義タイプ**   | ❌    | ✔️      | IFCスキーマからの有効な事前定義タイプ、または任意のカスタムテキスト値。 | IFC事前定義タイプは正確に一致しなければなりません |

## 例

| 適用範囲                           | 要件                 | ファセット定義                                                |
|--------------------------------|--------------------|--------------------------------------------------------|
| すべての区画壁                        | 区画壁でなければならない       | Name="IFCWALL", PredefinedType="PARTITIONING"                   |
| すべての床スラブ                       | 床スラブでなければならない      | Name="IFCSLAB", PredefinedType="FLOOR"                          |
| ドアタイプ一覧表で文書化される可能性があるすべてのドアタイプ | ドアタイプでなければならない     | Name="IFCDOORTYPE"                                       |
| すべての建物の階層                      | 建物の階層でなければならない     | Name="IFCBUILDINGSTOREY"                                |
| 図面、一覧表、マニュアル、仕様書などのすべての関連文書    | 文書でなければならない        | Name="IFCDOCUMENTINFORMATION"                            |
| 温水システム、電気回路などのすべての配管・配線システム    | 配管・配線システムでなければならない | Name=["IFCDISTRIBUTIONSYSTEM", "IFCDISTRIBUTIONCIRCUIT"] |
| 工事進行スケジュールの作業分解構造におけるすべての建設タスク | 建設タスクでなければならない     | Name="IFCTASK", PredefinedType="CONSTRUCTION"                   |
