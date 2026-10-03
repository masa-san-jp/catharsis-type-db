# 概要
- このプロジェクトでは、OpenAI o1 proが出力した「鑑賞者が体験するカタルシス」のタイプの分類データからデータベースを作り、ランダムに取り出した「鑑賞者が体験するカタルシス」を目的として物語のプロットのアイデアを生成します。
- このプロジェクトは、ChatGPT Proで使用できる、OpenAIのo1 pro modeの検証を兼ねています

# 手順
- ChatGPT Proのo1 pro modeに、「鑑賞者が体験するカタルシス」を分類させます
  - [catharsis-type.md](https://github.com/masa-jp-art/catharsis-type-db/blob/main/catharsis-type.md)
- 出力されたプロットタイプをスプレッドシートに転記してデータベースを作ります
  - [20250103-catharsis-type-snapshot](https://docs.google.com/spreadsheets/d/1xhIcB0q_PTHrhzuIpWXO23FG2zeVEKbYzZtP-7ES7co/edit)
- Google colabでプログラムを動かし、キャラクターとあらすじを生成します
  - [catharsis-type-for-google-colab.py](https://github.com/masa-jp-art/catharsis-type-db/blob/main/catharsis-type-for-google-colab.py)
 
# 関連
- [OpenAI o1 pro mode検証: 鑑賞者にもたらすカタルシスを分類しデータベース化できるか](https://note.com/msfmnkns/n/n34d4b813cefd)

## 用語と創作用の例

この資料での「カタルシス」は、鑑賞者に届けたい感情の解放・変化を表す創作用の分類です。[分類データ](catharsis-type.md)の「融和・和解」なら、長く続く誤解や対立から、相手の本心を知って和解する流れを発想の軸にできます。これは分類の使用例で、鑑賞者が必ず同じ反応をするという予測ではありません。

## 分類の背景と成立

本リポジトリの出発点は、概要にある o1 pro mode による分類の検証です。収録データは感情、前提、トリガー、解放の形、再現のポイントを整理した生成AI由来の創作資料であり、学術的に検証された心理分類や、特定の古典理論の忠実な再現として提示するものではありません。モデルによる分類作成と、Colabスクリプトのプロット生成APIは別工程です。

## 使い方の展開

[Colab用コード](catharsis-type-for-google-colab.py)は、シート `catharsis` の2列目から見出しを除いて1件を無作為に選び、主人公・サブキャラクター・対立者の設定とともにプロット生成へ渡します。同じ人物設定で目的とする感情を替え、異なる展開案を比較する使い方ができます。Sheetsの準備と認証、API設定は利用者側で必要です。生成案は素材として読み直し、物語として採用するかを判断します。

