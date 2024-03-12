# IDS内の単位

数値測定値は、IDSファイル内でSI単位を使用して表されます。

IFCモデルが検証される際、その値は比較前にデフォルト単位へ変換される必要があります。

以下の表は、変換が必要な測定値と、変換プロセスをサポートするためのメタデータをリストしています。
IFC定義タイプの完全なリストは、IFCドキュメントで見ることができます。

次元指数単位の順序は`(m, Kg, s, A, K, mol, cd)`です。

| IFC定義タイプ名                                     | 物理量の説明                 | 単位         | 単位記号     | 次元指数               | 単位列挙型                                       |
|-----------------------------------------------| -------------------------- | ------------ | ------------ | --------------------- | ------------------------------------------------ |
| IFCABSORBEDDOSEMEASURE                        | 吸収放射線量                | gray         | J / Kg       | (2, 0, -2, 0, 0, 0, 0) | IfcUnitEnum.ABSORBEDDOSEUNIT                     |
| IFCACCELERATIONMEASURE                        | 加速度                      |              | m / s2       | (1, 0, -2, 0, 0, 0, 0) | IfcDerivedUnitEnum.ACCELERATIONUNIT              |
| IFCAMOUNTOFSUBSTANCEMEASURE                   | 物質量                      | mole         | mol          | (0, 0, 0, 0, 0, 1, 0)  | IfcUnitEnum.AMOUNTOFSUBSTANCEUNIT                |
| IFCANGULARVELOCITYMEASURE                     | 角速度                      |              | rad / s      | (0, 0, -1, 0, 0, 0, 0) | IfcDerivedUnitEnum.ANGULARVELOCITYUNIT           |
| IFCAREADENSITYMEASURE                         | 面密度                      |              | Kg / m2      | (-2, 1, 0, 0, 0, 0, 0) | IfcDerivedUnitEnum.AREADENSITYUNIT               |
| IFCAREAMEASURE                                | 面積                        | square meter | m2           | (2, 0, 0, 0, 0, 0, 0)  | IfcUnitEnum.AREAUNIT                             |
| IFCCURVATUREMEASURE                           | 曲率                        |              | rad / m      | (-1, 0, 0, 0, 0, 0, 0) | IfcDerivedUnitEnum.CURVATUREUNIT                 |
| IFCDOSEEQUIVALENTMEASURE                      | 等価線量                    | sievert      | J / Kg       | (2, 0, -2, 0, 0, 0, 0) | IfcUnitEnum.DOSEEQUIVALENTUNIT                   |
| IFCDYNAMICVISCOSITYMEASURE                    | 動粘度                      |              | Pa s         | (-1, 1, -1, 0, 0, 0, 0)| IfcDerivedUnitEnum.DYNAMICVISCOSITYUNIT          |
| IFCELECTRICCAPACITANCEMEASURE                 | 電気容量                    | farad        | F            | (-2, 1, 4, 1, 0, 0, 0) | IfcUnitEnum.ELECTRICCAPACITANCEUNIT              |
| IFCELECTRICCHARGEMEASURE                      | 電荷                        | coulomb      | C            | (0, 0, 1, 1, 0, 0, 0)  | IfcUnitEnum.ELECTRICCHARGEUNIT                   |
| IFCELECTRICCONDUCTANCEMEASURE                 | 電気伝導度                  | siemens      | S            | (-2, -1, 3, 2, 0, 0, 0)| IfcUnitEnum.ELECTRICCONDUCTANCEUNIT              |
| IFCELECTRICCURRENTMEASURE                     | 電流                        | ampere       | A            | (0, 0, 0, 1, 0, 0, 0)  | IfcUnitEnum.ELECTRICCURRENTUNIT                  |
| IFCELECTRICRESISTANCEMEASURE                  | 電気抵抗                    | ohm          | Ω            | (2, 1, -3, -2, 0, 0, 0)| IfcUnitEnum.ELECTRICRESISTANCEUNIT               |
| IFCELECTRICVOLTAGEMEASURE                     | 電圧                        | volt         | V            | (2, 1, -3, -1, 0, 0, 0)| IfcUnitEnum.ELECTRICVOLTAGEUNIT                  |
| IFCENERGYMEASURE                              | エネルギー                  | joule        | J            | (2, 1, -2, 0, 0, 0, 0) | IfcUnitEnum.ENERGYUNIT                           |
| IFCFORCEMEASURE                               | 力                          | newton       | N            | (1, 1, -2, 0, 0, 0, 0) | IfcUnitEnum.FORCEUNIT                            |
| IFCFREQUENCYMEASURE                           | 周波数                      | hertz        | Hz           | (0, 0, -1, 0, 0, 0, 0) | IfcUnitEnum.FREQUENCYUNIT                        |
| IFCHEATFLUXDENSITYMEASURE                     | 熱流束密度                  |              | W / m2       | (0, 1, -3, 0, 0, 0, 0)  | IfcDerivedUnitEnum.HEATFLUXDENSITYUNIT           |
| IFCHEATINGVALUEMEASURE                        | 加熱                        |              | J / K        | (2, 1, -2, 0, -1, 0, 0) | IfcDerivedUnitEnum.HEATINGVALUEUNIT              |
| IFCILLUMINANCEMEASURE                         | 照度                        | lux          | lx           | (-2, 0, 0, 0, 0, 0, 1)  | IfcUnitEnum.ILLUMINANCEUNIT                      |
| IFCINDUCTANCEMEASURE                          | インダクタンス              | henry        | Wb / A       | (2, 1, -2, -2, 0, 0, 0) | IfcUnitEnum.INDUCTANCEUNIT                       |
| IFCINTEGERCOUNTRATEMEASURE                    | カウント率                  |              | 1 / s        | (0, 0, -1, 0, 0, 0, 0)  | IfcDerivedUnitEnum.INTEGERCOUNTRATEUNIT          |
| IFCIONCONCENTRATIONMEASURE                    | イオン濃度                  |              | mol / m3     | (-3, 1, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.IONCONCENTRATIONUNIT          |
| IFCISOTHERMALMOISTURECAPACITYMEASURE          | 等温湿度容量                |              | m3 / Kg      | (3, -1, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.ISOTHERMALMOISTURECAPACITYUNIT|
| IFCKINEMATICVISCOSITYMEASURE                  | 動粘度                      |              | m2 / s       | (2, 0, -1, 0, 0, 0, 0)  | IfcDerivedUnitEnum.KINEMATICVISCOSITYUNIT        |
| IFCLENGTHMEASURE                              | 長さ                        | meter        | m            | (1, 0, 0, 0, 0, 0, 0)  | IfcUnitEnum.LENGTHUNIT                           |
| IFCLINEARFORCEMEASURE                         | 線形力                      |              | N / m        | (0, 1, -2, 0, 0, 0, 0)  | IfcDerivedUnitEnum.LINEARFORCEUNIT               |
| IFCLINEARMOMENTMEASURE                        | 線形モーメント              |              | N m / m      | (1, 1, -2, 0, 0, 0, 0)  | IfcDerivedUnitEnum.LINEARMOMENTUNIT              |
| IFCLINEARSTIFFNESSMEASURE                     | 線形剛性                    |              | N / m        | (0, 1, -2, 0, 0, 0, 0)  | IfcDerivedUnitEnum.LINEARSTIFFNESSUNIT           |
| IFCLINEARVELOCITYMEASURE                      | 速度                        |              | m / s        | (1, 0, -1, 0, 0, 0, 0)  | IfcDerivedUnitEnum.LINEARVELOCITYUNIT            |
| IFCLUMINOUSFLUXMEASURE                        | 光束                        | lumen        | lm           | (0, 0, 0, 0, 0, 0, 1)  | IfcUnitEnum.LUMINOUSFLUXUNIT                     |
| IFCLUMINOUSINTENSITYDISTRIBUTIONMEASURE       | 光強度分布                  |              | cd / lm      | (0, 0, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.LUMINOUSINTENSITYDISTRIBUTIONUNIT |
| IFCLUMINOUSINTENSITYMEASURE                   | 光強度                      | candela      | cd           | (0, 0, 0, 0, 0, 0, 1)  | IfcUnitEnum.LUMINOUSINTENSITYUNIT                |
| IFCMAGNETICFLUXDENSITYMEASURE                 | 磁束密度                    | tesla        | Wb / m2      | (0, 1, -2, -1, 0, 0, 0)| IfcUnitEnum.MAGNETICFLUXDENSITYUNIT              |
| IFCMAGNETICFLUXMEASURE                        | 磁束                        | weber        | Wb           | (2, 1, -2, -1, 0, 0, 0)| IfcDerivedUnitEnum.MAGNETICFLUXUNIT              |
| IFCMASSDENSITYMEASURE                         | 質量密度                    |              | Kg / m3      | (-3, 1, 0, 0, 0, 0, 0) | IfcDerivedUnitEnum.MASSDENSITYUNIT               |
| IFCMASSFLOWRATEMEASURE                        | 質量流量                    |              | Kg / s       | (0, 1, -1, 0, 0, 0, 0) | IfcDerivedUnitEnum.MASSFLOWRATEUNIT              |
| IFCMASSMEASURE                                | 質量                        | kilogram     | Kg           | (0, 1, 0, 0, 0, 0, 0)  | IfcUnitEnum.MASSUNIT                             |
| IFCMASSPERLENGTHMEASURE                       | 長さ当たりの質量            |              | Kg / m       | (-1, 1, 0, 0, 0, 0, 0) | IfcDerivedUnitEnum.MASSPERLENGTHUNIT             |
| IFCMODULUSOFELASTICITYMEASURE                 | 弾性率                      |              | N / m2       | (-1, 1, -2, 0, 0, 0, 0)| IfcDerivedUnitEnum.MODULUSOFELASTICITYUNIT       |
| IFCMODULUSOFLINEARSUBGRADEREACTIONMEASURE     | 線形基盤反応の弾性率        |              | N / m2       | (-1, 1, -2, 0, 0, 0, 0)| IfcDerivedUnitEnum.MODULUSOFLINEARSUBGRADEREACTIONUNIT |
| IFCMODULUSOFROTATIONALSUBGRADEREACTIONMEASURE | 回転基盤反応の弾性率        |              | N m / m rad  | (1, 1, -2, 0, 0, 0, 0) | IfcDerivedUnitEnum.MODULUSOFROTATIONALSUBGRADEREACTIONUNIT |
| IFCMODULUSOFSUBGRADEREACTIONMEASURE           | 基盤反応の弾性率            |              | N / m3       | (-2, 1, -2, 0, 0, 0, 0)| IfcDerivedUnitEnum.MODULUSOFSUBGRADEREACTIONUNIT |
| IFCMOISTUREDIFFUSIVITYMEASURE                 | 湿度拡散率                  |              | m3 / s       | (3, 0, -1, 0, 0, 0, 0) | IfcDerivedUnitEnum.MOISTUREDIFFUSIVITYUNIT       |
| IFCMOLECULARWEIGHTMEASURE                     | 分子量                      |              | Kg / mol     | (0, 1, 0, 0, 0, -1, 0) | IfcDerivedUnitEnum.MOLECULARWEIGHTUNIT           |
| IFCMOMENTOFINERTIAMEASURE                     | 慣性モーメント              |              | m4           | (4, 0, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.MOMENTOFINERTIAUNIT           |
| IFCNONNEGATIVELENGTHMEASURE                   | 非負の長さ                  | meter        | m            | (1, 0, 0, 0, 0, 0, 0)  | IfcUnitEnum.LENGTHUNIT                           |
| IFCPHMEASURE                                  | PH値                        |              | PH           | (0, 0, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.PHUNIT                        |
| IFCPLANARFORCEMEASURE                         | 平面力                      |              | Pa           | (-1, 1, -2, 0, 0, 0, 0)| IfcDerivedUnitEnum.PLANARFORCEUNIT               |
| IFCPLANEANGLEMEASURE                          | 角度                        | radian       | rad          | (0, 0, 0, 0, 0, 0, 0)  | IfcUnitEnum.PLANEANGLEUNIT                       |
| IFCPOSITIVELENGTHMEASURE                      | 正の長さ                    | meter        | m            | (1, 0, 0, 0, 0, 0, 0)  | IfcUnitEnum.LENGTHUNIT                           |
| IFCPOSITIVEPLANEANGLEMEASURE                  | 正の平面角                  | radian       | rad          | (0, 0, 0, 0, 0, 0, 0)  | IfcUnitEnum.PLANEANGLEUNIT                       |
| IFCPOWERMEASURE                               | 力率                        | watt         | W            | (2, 1, -3, 0, 0, 0, 0) | IfcUnitEnum.POWERUNIT                            |
| IFCPRESSUREMEASURE                            | 圧力                        | pascal       | Pa           | (-1, 1, -2, 0, 0, 0, 0)| IfcUnitEnum.PRESSUREUNIT                         |
| IFCRADIOACTIVITYMEASURE                       | 放射能                      | becquerel    | Bq           | (0, 0, -1, 0, 0, 0, 0) | IfcUnitEnum.RADIOACTIVITYUNIT                    |
| IFCROTATIONALFREQUENCYMEASURE                 | 回転周波数                  | hertz        | Hz           | (0, 0, -1, 0, 0, 0, 0) | IfcDerivedUnitEnum.ROTATIONALFREQUENCYUNIT       |
| IFCROTATIONALMASSMEASURE                      | 回転質量                    |              | Kg m2        | (2, 1, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.ROTATIONALMASSUNIT            |
| IFCROTATIONALSTIFFNESSMEASURE                 | 回転剛性                    |              | N m / rad    | (2, 1, -2, 0, 0, 0, 0) | IfcDerivedUnitEnum.ROTATIONALSTIFFNESSUNIT       |
| IFCSECTIONALAREAINTEGRALMEASURE               | 断面積積分                  |              | m5           | (5, 0, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.SECTIONALAREAINTEGRALUNIT     |
| IFCSECTIONMODULUSMEASURE                      | 断面係数                    |              | m3           | (3, 0, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.SECTIONMODULUSUNIT            |
| IFCSHEARMODULUSMEASURE                        | せん断率                    |              | N / m2       | (-1, 1, -2, 0, 0, 0, 0)| IfcDerivedUnitEnum.SHEARMODULUSUNIT              |
| IFCSOLIDANGLEMEASURE                          | 立体角                      | steradian    | sr           | (0, 0, 0, 0, 0, 0, 0)  | IfcUnitEnum.SOLIDANGLEUNIT                       |
| IFCSOUNDPOWERLEVELMEASURE                     | 音響パワーレベル            | decibel      | db           | (0, 0, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.SOUNDPOWERLEVELUNIT           |
| IFCSOUNDPOWERMEASURE                          | 音響パワー                  | decibel      | db           | (0, 0, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.SOUNDPOWERUNIT                |
| IFCSOUNDPRESSURELEVELMEASURE                  | 音圧レベル                  | decibel      | db           | (0, 0, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.SOUNDPRESSURELEVELUNIT        |
| IFCSOUNDPRESSUREMEASURE                       | 音圧                        | decibel      | db           | (0, 0, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.SOUNDPRESSUREUNIT             |
| IFCSPECIFICHEATCAPACITYMEASURE                | 比熱                        |              | J / Kg K     | (2, 0, -2, 0, -1, 0, 0)| IfcDerivedUnitEnum.SPECIFICHEATCAPACITYUNIT      |
| IFCTEMPERATUREGRADIENTMEASURE                 | 温度勾配                    |              | K / m        | (-1, 0, 0, 0, 1, 0, 0) | IfcDerivedUnitEnum.TEMPERATUREGRADIENTUNIT       |
| IFCTEMPERATURERATEOFCHANGEMEASURE             | 温度変化率                  |              | K / s        | (0, 0, -1, 0, 1, 0, 0) | IfcDerivedUnitEnum.TEMPERATURERATEOFCHANGEUNIT   |
| IFCTHERMALADMITTANCEMEASURE                   | 熱透過率                    |              | W / m2 K     | (0, 1, -3, 0, -1, 0, 0)| IfcDerivedUnitEnum.THERMALADMITTANCEUNIT         |
| IFCTHERMALCONDUCTIVITYMEASURE                 | 熱伝導率                    |              | W / m K      | (1, 1, -3, 0, -1, 0, 0)| IfcDerivedUnitEnum.THERMALCONDUCTANCEUNIT        |
| IFCTHERMALEXPANSIONCOEFFICIENTMEASURE         | 熱膨張係数                  |              | 1 / K        | (0, 0, 0, 0, -1, 0, 0) | IfcDerivedUnitEnum.THERMALEXPANSIONCOEFFICIENTUNIT |
| IFCTHERMALRESISTANCEMEASURE                   | 熱抵抗                      |              | m2 K / W     | (0, -1, 3, 0, 1, 0, 0) | IfcDerivedUnitEnum.THERMALRESISTANCEUNIT         |
| IFCTHERMALTRANSMITTANCEMEASURE                | 熱伝達率                    |              | W / m2 K     | (0, 1, -3, 0, -1, 0, 0)| IfcDerivedUnitEnum.THERMALTRANSMITTANCEUNIT      |
| IFCTHERMODYNAMICTEMPERATUREMEASURE            | 温度                        | kelvin       | K            | (0, 0, 0, 0, 1, 0, 0)  | IfcUnitEnum.THERMODYNAMICTEMPERATUREUNIT         |
| IFCTIMEMEASURE                                | 時間                        | second       | s            | (0, 0, 1, 0, 0, 0, 0)  | IfcUnitEnum.TIMEUNIT                             |
| IFCTORQUEMEASURE                              | トルク                      |              | N m          | (2, 1, -2, 0, 0, 0, 0) | IfcDerivedUnitEnum.TORQUEUNIT                    |
| IFCVAPORPERMEABILITYMEASURE                   | 蒸気透過性                  |              | Kg / s m Pa  | (0, 0, 1, 0, 0, 0, 0)  | IfcDerivedUnitEnum.VAPORPERMEABILITYUNIT         |
| IFCVOLUMEMEASURE                              | 体積                        | cubic meter  | m3           | (3, 0, 0, 0, 0, 0, 0)  | IfcUnitEnum.VOLUMEUNIT                           |
| IFCVOLUMETRICFLOWRATEMEASURE                  | 体積流量                    |              | m3 / s       | (3, 0, -1, 0, 0, 0, 0) | IfcDerivedUnitEnum.VOLUMETRICFLOWRATEUNIT        |
| IFCWARPINGCONSTANTMEASURE                     | ねじれ定数                  |              | m6           | (6, 0, 0, 0, 0, 0, 0)  | IfcDerivedUnitEnum.WARPINGCONSTANTUNIT           |
| IFCWARPINGMOMENTMEASURE                       | ねじれモーメント            |              | N m2         | (3, 1, -2, 0, 0, 0, 0) | IfcDerivedUnitEnum.WARPINGMOMENTUNIT             |

## 次元単位

各次元指数はデフォルトのSI単位を参照します

| 次元指数リスト内の位置 | 物理量           | SI単位                   |
| --------------------- | --------------- | ------------------------ |
| 1                     | 長さ            | メートル                 |
| 2                     | 質量            | キログラム               |
| 3                     | 時間            | 秒                       |
| 4                     | 電流            | アンペア                 |
| 5                     | 熱力学的温度    | ケルビン                 |
| 6                     | 物質量          | モル                     |
| 7                     | 光度            | カンデラ                 |

## 例

ソフトウェアでは、値は通常ローカル単位で表示されます。以下の表は、ユーザーにどのように表示されるか、そしてIDSでどのように表されるかの例をいくつかリストしています。

| ユーザー視点   | IDS値       | 物理量       |
| -------------- | ----------- | ------------ |
| 10 mm          | 0.01        | 長さ         |
| 1"             | 0.0254      | 長さ         |
| 1 kW           | 1000        | 力率         |
| 1 lbs          | 0.45359237  | 質量         |
| 20 C           | 293.15      | 温度         |
