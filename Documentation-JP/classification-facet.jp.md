# 分類ファセット

**分類システム**は、要素を分類するための定義された階層です。一般的な**システム**の例として「Uniclass 2015」があります。*
*Uniclass 2015**内には、"EF_25_10" や "EF_25_10_25" など、要素をより具体的なレベルで分類する短い**参照コード**
の階層があります。IFCモデルのどのオブジェクトにも、その**分類参照**が設定され得ます。

**分類ファセット**は、**エンティティファセット**とは異なります。**エンティティファセット**
は、内蔵されたIFCクラスと事前定義タイプに制限されており、これらは**分類**の方法としても機能するかもしれません。対照的に、*
*分類ファセット**で指定される**システム**は、サードパーティーの非IFC**システム**を参照します。

IFCモデルは**分類**の名前、日付、バージョン、その他のデータを追跡して**システム**を一意に識別し、**参照**
の階層さえも格納することができます。このため、**分類**要件は**プロパティファセット**ではなく、**分類ファセット**を使用すべきです。

**分類**は、**適用可能**なエンティティを識別する、またはエンティティが資産管理システム、作業分解構造、または調整要件などのワークフローによって指名された
**分類**システムに従うことを**要求**する素晴らしい方法です。

## パラメータ

| パラメータ    | 必須 | 制約許可 | 許可される値                       | 意味                                                                                                                                                                                                             |
|----------|----|------|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **システム** | ✔️ | ✔️   | **分類システム**の名前                | 要素はこの名前の分類システムの一部である参照で分類されなければなりません                                                                                                                                                                           |
| **値**    | ❌  | ✔️   | **分類システム**内の**参照**コードの値      | 要素はこの値と一致するコードを持つ**参照**で分類されなければなりません。値は通常、分類レベルを示す区切り文字を持つ短いコードです                                                                                                                                             |
| **URI**  | ❌  | ❌    | ISO 23386に準拠した分類の識別に使用されるURI | [buildingSMART Data Dictionary](https://search.bsdd.buildingsmart.org/)で有効なURIを見つけることができます。例えば、[Uniclassベースのアルミニウム窓壁](https://identifier.buildingsmart.org/uri/nbs/uniclass2015-1/class/Pr_30_59_99_02 )の分類です。 |

パラメータが指定されていない場合、**システム**名または**参照**コードにかかわらず、任意の**分類**が存在すれば良いことを意味します。

## 例

 適用範囲                                              | 要件                                                       | ファセット定義                                    
---------------------------------------------------|----------------------------------------------------------|--------------------------------------------
 分類された任意の要素                                        | エンティティは分類されなければならない                                      | なし                                         
 OmniClassを使用して分類された任意のエンティティ                      | エンティティはOmniClassを使用して分類されなければならない                        | System="OmniClass"                         
 OmniClassまたはUniclass 2015のいずれかを使用して分類された任意のエンティティ | エンティティはOmniClassまたはUniclass 2015を使用して分類されなければならない        | System=["OmniClass", "Uniclass 2015"]      
 分類参照が「EF_25_10_25」である任意のエンティティ                    | 要素（例：壁）は参照「EF_25_10_25」を使用して分類されなければならない                 | Value="EF_25_10_25"                        
 Uniclass 2015の分類参照がEF_25_10で始まる任意の要素              | エンティティ（例：壁）はUniclass 2015を使用し、参照がEF_25_10で始まるものでなければならない | System="Uniclass 2015", Value="EF_25_10.*" 
