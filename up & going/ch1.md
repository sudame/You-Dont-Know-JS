# You Don't Know JS: Up & Going
# チャプター 1: プログラミング入門

*You Don't Know JS* (*YDKJS*)シリーズへようこそ。

*Up & Going* では、JavaScriptを中心としてプログラミングの基本的なコンセプトについて紹介します。JavaScriptはJSと略されることもあるので注意してください。本シリーズの残りのテーマについて、どのようにアプローチし理解していくかも本書で紹介します。特に、プログラミングやJavaScriptを始めたばかりの読者向けに、*up and going*するために何をすれば良いのかを簡潔に説明します。

本書ではまず、プログラミングの基本的な原則を非常に高いレベルで紹介します。これは、プログラミング経験が無かったり、本シリーズをJavaScriptを通したプログラミングの入門書として手に取ったりした方向けの内容です。

チャプター1では、	プログラミングに入門するために読者の皆さんが学ばなければいけないことを簡単に示します。各トピックについて深く知りたい場合は、他にも素晴らしい教材がたくさんあります。しかし、チャプター1を読んでから取り掛かることを強くオススメします。

プログラミングの一般的な部分に納得できたら、チャプター2に進みましょう。チャプター2の目標はJavaScript特有のプログラミングに馴染むことです。チャプター2では、JavaScriptとは一体何なのかを説明します。繰り返しになりますが、チャプター2で触れる内容はJavaScriptの全てではありません。JavaScriptの全ては、残りの*YDJKS*シリーズでじっくりお教えします！

既にJavaScriptに慣れているなら、チャプター3から読み始めてください。チャプター3では、*YDKJS*を通して何を学べるのかを簡単に説明しています。知りたい内容が見つかったら、今すぐ読み始めましょう！

## コード

さっそく取り掛かりましょう。

プログラムは、コンピュータに何をさせるのかを示した命令の集まりです。プログラムは *ソースコード* や単純に *コード* とも呼ばれます。コードは普通、テキストファイルに保存します。ただし、この後すぐ説明しますが、JavaScriptはブラウザの開発者ツールを使って直接コードを書くこともできます。

プログラムの正しい書き方や命令の組み合わせ方の「ルール」のことを *プログラミング言語* 、あるいは *構文* と呼びます。これは、English(英語)という言語が、どのように単語をつづり、どのように意味のある文を作り、どのように句読点を打つかという「ルール」であることと全く同じです。

### 文(Statements)

プログラミング言語では、1つのタスクを行う単語や数字や演算子の集まりのことを *式(ステートメント)* と呼びます。JavaScriptでは、式は次のように書きます。

```js
a = b * 2;
```

`a` や `b` という文字は *変数* と呼ばれます(詳しくは「変数」の項を参照)。変数は、何でも入れられるシンプルな箱のようなものです。プログラムでは、変数はプログラム中で使われる値(例えば数字の `42` )を保持するために使います。変数は値に対するプレースホルダーと考えても構いません。

対象的に、`2` は変数に格納されておらず独立しているため、単なる値だと考えることができます。単なる値は *リテラル* と呼ばれます。

(訳注: 原文では *リテラル* は *literal value* と書かれており、*リテラル値* が直訳ですが、日本人プログラマは単に *リテラル* と呼ぶことが多いため、 *リテラル* を採用しました。)

`=` や `*` といった文字は *演算子* です(詳しくは「演算子」の項を参照)。演算子は代入や乗算といった値や変数に対する操作を行うときに用います。

JavaScriptのほとんどの文は、最後にセミコロン(`;`)を付けて終了します。

おおまかに言えば、`a = b * 2;` という式はコンピュータに対して「現在変数 `b` に格納されている値に `2` を掛け、乗算の結果を( `b` とは別の)変数 `a` に保存しろ」といった命令を出しています。

プログラムはたくさんの文を集めたもので、プログラムの目的をこなすために必要な全てのステップをまとめたものと言えます。

### 式(Expressions)

文(ステートメント)は1つ以上の *式(expressions)* で構成されます。式は、変数や値の参照であったり、変数や値と演算子を組み合わせたものであったりします。

具体的に見てみましょう。

```js
a = b * 2;
```

この文には4つの式が含まれています。

* `2` は *リテラル式* です。
* `b` は *変数式* です。変数に格納されている値を取り出します。
* `b * 2` は *算術式* です。ここでは、乗算を行っています。
* `a = b * 2` は *代入式* です。ここでは、`b * 2` という式の計算結果を変数 `a` に代入(代入については後ほど触れます)しています。

独立している式は *式文(expression statement)* と呼ばれます。

```js
b * 2;
```

この式文はプログラムの実行結果に何の影響も及ぼさないため、あまり一般的ではありませんし、有用でもありません。この式文では、変数 `b` から値を取り出してそれに `2` を掛けますが、乗算の結果は全く使われません。

より一般的で有用な式文としては *呼び出し式* の文(詳しくは「関数」の項を参照)が挙げられます。呼び出し式は文そのものが関数を呼び出します。

```js
alert( a );
```

### プログラムの実行

プログラム言語を使ってコードを書くことはできましたが、それをどのようにコンピュータに理解させるのでしょう？プログラムは *実行* される必要があります。プログラムを実行することは *プログラムを走らせる* と表現されることもあります。

`a = b * 2` といった式は開発者が読み書きするのには便利ですが、実際にはコンピュータは直接この書き方を理解することができません。このため、コンピュータが理解できる命令に変換するためのツール(*インタープリタ* とか *コンパイラ* と呼ばれます)が用いられます。

いくつかのプログラミング言語では、この変換作業が文字通り上から下に、1行ずつ、プログラムを走らせるたびに行われます。この方式の変換作業のことを *インタープリティング* と呼び、この方式を採用した言語のことを「インタープリタ型言語」と呼びます。

インタープリタ型言語以外のプログラミング言語では、変換作業を事前に行っておきます。プログラムが *走る* 際に実際に実行されるのは、事前に変換作業を行ったコードです。この方式の変換作業のことを *コンパイル* と呼び、この方式を採用した言語のことを「コンパイラ型言語」と呼びます。

通常、JavaScriptは実行時にソースコードを変換するため *インタープリタ型言語* であると言われています。しかしそれは完全に正確ではありません。正確に言えば、JavaScriptエンジンは実行時にプログラムを *コンパイル* し、それを即座に実行しているからです。

**注釈:** JavaScriptのコンパイルについてより詳しく知りたい場合は、本シリーズの *Scope & Closures* の最初の2チャプターを読んでみてください。

## 実践してみよう

この章では、それぞれのプログラミングの概念について簡単なコードを交えつつ紹介していきます。コードは全てJavaScriptで書かれています(もちろん！)。

ここで、とても重要なことをアドバイスしておきます。この章を学習している間(全てを理解するには数回読み直す必要があるかもしれません)は、それぞれの概念について、実際に自分でコードを手書きして実践するようにしてください。最も簡単な方法は、普段使っているブラウザ(Firefox, Chrome, IEなど)の開発者ツールのコンソールを使うことです。

**Tip:** 通常、開発者ツールはキーボードショートカットかメニューから開くことができます。より詳細な開き方やお気に入りのブラウザでのコンソールの使い方については、"Mastering The Developer Tools Console" (http://blog.teamtreehouse.com/mastering-developer-tools-console)をご覧ください。コンソールで一度に複数行を入力するときは、`<shift> + <enter>` で改行してください。単純に `<enter>` と打って改行しようとすると、コンソールは今までに書き込んだコードを全て実行してしまいます。

さて、コンソールでの実行に少しずつ慣れていきましょう。はじめに、ブラウザで新規タブを開いてください。アドレスバーに `about:blank` と入力するのがオススメの方法です。新規タブが開いたら、先ほど紹介した方法でコンソールを開いてください。

それでは、このコードを打ち込んで何が起こるのか見てみましょう

```js
a = 21;

b = a * 2;

console.log( b );
```

上記のコードをChromeのコンソールに入力すると、このような結果が出るはずです。

<img src="fig1.png" width="500">

では、読者の皆さんも試してみてください。プログラミングを習得する第一歩は、とにかくコーディングを始めてしまうことです！

### 出力

先ほど示したコード例では、`console.log(..)` を使いました。この文が何を意味しているのかを見ていきましょう。

おそらくあなたの想像通り、このコードはコンソールに文字列をプリントする(あるいは *出力* する)ことを意味します。さて、文中には2つ、説明しなければならない部分があります。

まず一つ目は `log( b )` の部分です。この部分は関数呼び出し(詳しくは「関数」の項を参照)を行っています。変数 `b` を関数に渡し、その関数が変数 `b` の値を読み取ってコンソールに出力しています。

二つ目は `console.` の部分です。この部分は、関数 `log(..)` を持っているオブジェクトへの参照です。オブジェクトやそのプロパティについては、チャプター2でより詳細に解説します。

他の出力方法として、`alert(..)` 文を実行する方法があります。例えば、次のように書きます。

```js
alert( b );
```

この文を実行すると、コンソールに文字が出力される代わりに、「OK」というボタンに併せて変数 `b` の内容が表示されるポップアップが現れるはずです。ただ、コーディングを習得したりプログラムをコンソール上で実行したりする上では、`alert(..)` を使うより `console.log(..)` を使うほうがより便利です。`console.log(..)` を使えば、ブラウザをいちいち操作することなく複数の値を出力することができるからです。

本書では、出力の方法として `console.log(..)` を使うことにします。

### 入力

ここまでは出力について扱ってきましたが、読者の皆さんは *入力* (例えば、ユーザから情報を受け取ること)も気になっているかもしれません。

最も一般的な場面としては、HTMLページに(テキストボックスのような)フォームを設置し、ユーザに入力してもらって、JSでユーザからの入力を受け取って変数に保存するというような場面が考えられます。

しかし、デモンストレーションや単純な学習目的としては、より簡単な方法があり、本書ではこの方法を採用します。`prompt(..)` 関数を使います。

```js
age = prompt( "Please tell me your age:" );

console.log( age );
```

皆さんのご想像通り、`prompt(..)` に渡したメッセージ(この場合は `"Please tell me your age:"`)がポップアップの中に表示されます。

実行結果は次のようになるはずです。

<img src="fig2.png" width="500">

テキストを入力して「OK」をクリックすれば、入力した値が変数 `age` に保存され、`console.log(..)` 関数によってコンソールに *出力* されることを確認できるはずです。

<img src="fig3.png" width="500">

プログラミングの基礎的な概念を学んでいく中で見通しを良くするため、本書のコード例ではユーザからの入力を扱いませんが、読者の皆さんは既に `prompt(..)` の使い方を習得していますから、もし余力があれば、ユーザの入力を受け付けるようコード例を改造してみるのも良いでしょう。

## 演算子

演算子は、変数や値に対するアクションを指定するものです。これまでに本書では `=` と `*` という2つのJavaScript演算子を紹介しました。

`*` 演算子は算術乗算を行います。とても直感的ですね。

`=` イコール演算子は代入のために用いられます。JavaScriptはまず *右辺* (元の値)の式を計算し、それを *左辺* (ターゲット変数)に指定した変数に保存するという動作をします。

**注意:** プログラミングの代入の書き方は、想像と逆の順序で書いているようで奇妙に見えるかもしれません。読者の皆さんのうち何人かは、`a = 42` と書くのではなく、元の値を左に、ターゲット変数を右に書いて `42 -> a` というように(これは正しいJavaScriptの書き方ではありません！)書きたいと思っていることでしょう。 ただ残念ながら、`a = 42` やそれに類する書き方は、最近のプログラミング言語では共通の書き方です。不自然な書き方だと感じても、時間をかけて慣れていくしかありません。

次のコード例を考えてみましょう。

```js
a = 2;
b = a + 1;
```

コード例ではまず、値 `2` を変数 `a` に代入しています。次に、`a` の値を読み取って(先ほど指定した `2` が読まれます)それに `1` を足します。最後に、計算結果である `3` を変数 `b` に保存しています。

これは演算子の話ではありませんが、`var` というキーワードをプログラムの随所に使っています。`var` は *var*iable(変数)を *定義* (あるいは *生成*)する基本的なキーワードです。

私たちは、変数を使う前にその変数を変数名とともに定義する必要があります。1つの *スコープ* (詳しくは「スコープ」の項を参照)に対して、同じ名前の変数は一度だけ定義できます。定義してしまえば、その後は必要に応じて何度でも変数を使うことができます。コード例を見てみましょう。

```js
var a = 20;

a = a + 1;
a = a * 2;

console.log( a );	// 42
```

次に示すのは、JavaScriptでも最も一般的な演算子です。

* 代入演算子: `=` | `a = 2` のように使います。
* 算術演算子: `+` (加算), `-` (減算), `*` (乗算), and `/` (除算) | `a * 3` のように使います。
* 複合演算子: `+=`, `-=`, `*=`, `/=` は複合演算子で、算術演算子と代入演算子を組み合わせたものです。| `a += 2` (`a = a + 2` と同じ意味)のように使います。
* インクリメント/デクリメント: `++` (インクリメント), `--` (デクリメント) | `a++` のように使います。(`a = a + 1` と同じ意味です)。
* プロパティアクセス演算子: `.` | `console.log()` のように使います。

	オブジェクトは他の値をプロパティーと呼ばれる場所に名前を付けて保存できるような値です。`obj.a` は `obj` という名前のオブジェクトの、 `a` という名前のプロパティを指します。プロパティには `obj["a"]` という書き方でもアクセスできます。チャプター2をご覧ください。
* 等値演算子: `==` (弱等値), `===` (強等値), `!=` (弱不等値), `!==` (強不等値) | `a == b` のように使います。

	"Values & Types" やチャプター2をご覧ください。
* 比較演算子: `<` (小なり), `>` (大なり), `<=` (以下), `>=` (以上) |  `a <= b` のように使います。

	"Values & Types" やチャプター2をご覧ください。
* 論理演算子: `&&` (かつ), `||` (または) | `a || b` のように使います。これは `a` *または* `b` を表します。

	これらの演算子は、「`a` または `b` が true」といったように、複数の条件(詳しくは「条件」を参照)を表現するときに用います。

**注意:** より詳しく知りたい場合やここで紹介していない演算子について知りたい場合はMozila Developer Network (MDN)の「式と演算子」(https://developer.mozilla.org/ja/docs/Web/JavaScript/Guide/Expressions_and_Operators)をご覧ください。

## 値と型

携帯電話ショップで、ある携帯電話の価格を店員に聞いたとしましょう。店員は「98,000」($98,000)と答えました。ここでは、店員はあなたが携帯電話を買うために必要な金額を数値で答えました。もしあなたが2つ携帯電話を必要であれば、暗算で金額を2倍するでしょう。$196,000が支払うべき金額です。

同じ店員が似たような携帯電話を持ってきて、「無料」と言ったとしましょう。今回は店員は数値で金額を教えるのではなく、「無料」という文字列で金額($0)を伝えてくれました。

次に、携帯電話に充電器が付いてくるのか聞いてみましょう。店員の回答は「はい」か「いいえ」であるはずです。

プログラムの中で値を扱う場合も携帯ショップでのやりとりと同じように、どんな値を扱うのかに応じて値の表し方を選ぶ必要があります。

この値の異なる表し方のことを、プログラミングでは *型* と言います。JavaScriptは *プリミティブ型* と呼ばれる、次のようなビルトインの型を持っています。

* 数値計算をするならば、`number` 型を使います。
* 画面上に値を出力するのであれば、`string` 型を使います。これは1つ以上の文字や単語や文を表します。
* プログラム中で判断をするのであれば `boolean` 型 (`true` または `false`)を使います。

ソースコード中に直接記してある値のことを *リテラル* と言います。`string` 型のリテラルはダブルクオーテーション( `"..."` )かシングルクオーテーション('...')で囲みます。ダブルクオーテーションとシングルクオーテーションの違いは見た目の違いのみです。`number` 型や `boolean` 型のリテラルはそのまま書けば良いです(例えば、`42` や `true` など)。

次のコード例を見てみましょう。

```js
"これはstring型です";
'これもまたstring型です';

42;

true;
false;
```

`string`/`number`/`boolean` という型に加えて、プログラミング言語では *配列*, *オブジェクト*, *関数* などという機能が提供されるのが一般的です。このチャプターと次のチャプターで、値と型についてはさらに詳しく説明します。

### 型の変換

`number` 型の変数があり、それを画面上に出力したい場合、`string` 型に変換する必要があります。JavaScriptでは、この変換のことを「型強制(coercing)」と言います。同じように、ネットショッピングのwebページのフォームから数字が入力された場合、数字は `string` 型として取得されますが、数値計算をしたい場合は `number` 型として扱うよう *強制* する必要があります。

JavaScriptは *型* 強制を行うためにいくつかの方法を提供しています。その内の一つの方法は次のようなものです。

```js
var a = "42";
var b = Number( a );

console.log( a );	// "42"
console.log( b );	// 42
```

`Number(..)` (ビルトイン関数)を用いることで、他のどのような型も *明示的に* `number` 型へと強制できます。非常に分かりやすいですね。

しかし、同じ型ではない2つの値を比較しようとするときは、論争を生むようなことが起こります。*暗黙的な* 型強制が行われるのです。

文字列型の `"99.99"` と数値型の `99.99` を比較するとき、ほとんどの人はこれらは等しいと考えるでしょう。しかし、これらの値は厳密には等しくありませんね。これらは異なる種類の同じ値ですが、*型* が異なります。これは「弱い等値」であると言えると思いませんか？

このような良くあるシチュエーションに対処するため、JavaScriptは *暗黙的に* 型強制を行い、マッチする型ととして値を格納する機能を持っています。

`==` 弱等値演算子を用いて `"99.99" == 99.99` という比較演算を行うと、JavaScriptは左辺の `"99.99"` を同じ値の `number` 型である `99.99` へと変換します。これにより、比較演算は `99.99 == 99.99` となり、結果はもちろん `true` となります。

暗黙的な型強制は開発を簡単にするために設計されたものですが、開発者が挙動のルールを十分に習得していない場合、かえって混乱を巻き起こすことになります。ほとんどのJS開発者は暗黙的な型強制について学ぶための時間を十分確保できていないため、暗黙的な型強制は予期せぬバグを引き起こす可能性があり避けるべきだと思われています。暗黙的な型強制はJavaScriptの設計上の弱点だとさえも言われる始末です。

しかし、暗黙的な型強制は *習得可能な* メカニズムであり、JavaScriptできちんとプログラミングをしたい人は *習得すべき* ものです。一度ルールを習得してしまえば、暗黙的な型強制で混乱しないようになるだけでなく、プログラムをより良いものにすることさえできます。暗黙的な型強制は習得するに値するものです。

**注意:** 型強制についてより詳しく知りたい場合は、チャプター2か、*Types & Grammar* のチャプター4をご覧ください。

## コードコメント

携帯電話ショップの店員は、新製品の特徴や本社の方針をメモに書いておくかもしれません。このメモは店員向けのものであり、来店客にが読むものではありません。にも関わらず、メモは店員が来店客に何をどのように伝えれば良いのかが書かれていますから、仕事をより良いものにしてくれます。

コードを書く中で最も重要なことの一つは、コードはコンピュータが読むだけのものではないということです。コードはコンパイラが解読するためにあるのと同様、開発者自身が解読するものでもあります。

コンピュータは *コンパイル* によって生成される0と1が連なる機械語のみを解釈します。コンパイルしてしまえば同じ0と1の羅列になるようなプログラムでも、その書き方は無限に存在します。無限にある書き方の中であなたがなぜその書き方を選択したのかは大変重要です。これはもちろんあなた自身にとっても重要なのですが、開発チームの他のメンバーにとっても重要ですし、将来コードを読み直した自分にとっても重要です。

正しく動作するプログラムを書くことは大切ですが、コードを読んだときに意味が分かるプログラムを書くことも大切です。読者の皆さんは今後、変数(詳細は「変数」の項を参照)や関数(詳細は「関数」の項を参照)により分かりやすい名前を付けることに頭を悩ませ続けることになるでしょう。

分かりやすいコードを書くにあたってもう一つ大切なものは、コードコメントです。コードコメントとは、人間にコードの説明をするためにコード中に挿入するテキストのことです。インタープリタやコンパイラはこれらのコメントを無視します。

良いコメントとは何かという議論には様々な意見があり、完全に絶対的かつ網羅的なルールを定義することは不可能です。しかし、次のようないくつかの意見やガイドラインは非常に有用です。

* コメントの無いコードは最適ではありません。
* 過剰なコメント(例えば1行に1つコメントを入れるなど)は下手なコーディングのサインかもしれません。
* コメントは *なぜ* を説明すべきで、*何を* したのかを説明するべきではありません。特に分かりづらいコードには *どのように* を説明しても良いでしょう。

JavaScriptでは、1行コメントと複数行コメントという2種類のコメント形式があります。

次のコード例を見てみましょう。

```js
// これは1行のコメントです。

/* これは
       複数行の
             コメントです。
                            */
```

`//` は1行のコメントを表し、文の右側や行末にコメントを付けたいときに向いています。`//` の後に書かれたものは行が終わるまでがコメントとして扱われます(つまり、コンパイラに無視されます)。1行のコメントの中には何を書いても構いません。

次にように使うのが一般的です。

```js
var a = 42;		// 42 は残りライフを表す
```

`/* .. */` は複数行のコメントを表し、コードの説明をするにあたって複数行が必要な場合に向いています。


次のコード例は複数行のコメントの一般的な使い方です。

```js
/* 次の変数は、生命、宇宙、そし
   て万物についての究極の疑問の
   答えを表すために使用 */
var a = 42;
```

この形式のコメントは、行のどこにでも書くことができ、行の真ん中に書くこともできます。これは `*/` がコメントの終端であることを表しているためです。例えば、

```js
var a = /* 任意の値 */ 42;

console.log( a );	// 42
```

というコメントも書くことができます。

複数行のコメントの中に唯一書いてはいけないものは `*/` です。`*/` を書くとコメントが終了してしまいます。

読者の皆さんはコメントを書く習慣を付けつつプログラミングの学習を始めたいと思っていることでしょう。このチャプターの残りの部分では、コード例にコメントを入れていきます。皆さんも練習として、同じようにコメントを書くようにしてください。筆者を信じてください。皆さんのコードを読んだ人はあなたに感謝してくれるはずです！

## 変数

有用なプログラムのほとんどは、プログラム中の他の部分が変化している間にも値を保持し続ける必要があります。

そのようなことを実現する最も簡単な方法は、値に何らかの印の付いた箱のようなものを割り当てることです。「何らかの印の付いた箱のようなもの」は *変数* と呼ばれています。*変* 数の名前の由来は、箱が保持する値は状況によって *変* 化させることができることによります。

いくつかのプログラミング言語では、変数を定義するときに `number` や `string` といった型を指定して定義しなければなりません。こういったプログラミング言語は `静的型付け` や `型強制` と呼ばれます。静的型付けは特に、意図しない値の変化を防止することでプログラムを正確にするのに役立ちます。

(訳注: ここで言う *型強制* は *type enforcement* です。型の変換で触れた *型強制* は *type coercion* で、全く別の概念です。良い訳語をお待ちしております。)

静的型付け言語以外の言語では、変数に対する型よりも値に対する型を重視します。これは *弱い型付け* や *動的型付け* と呼ばれ、変数にはいつでもいかなる型の値も格納できます。動的型付け言語ではプログラムの論理的な流れの中で、どのような状態においても値を一つの変数で表すことができるため、特にプログラムの柔軟性を向上するのに役立ちます。

JavaScriptは後者の方式、すなわち *動的型付け* を採用していて、変数が格納する値の *型* を強制することはなく、どのような *型* でも格納できます。

既に触れているように、変数を定義するときは `var` 式を用います。変数を定義するときには *型* の情報を一切書いていないことに注意してください。次の簡単なコード例をご覧ください。

```js
var amount = 99.99;

amount = amount * 2;

console.log( amount );		// 199.98

// `amount`をstring型に変換し、
// "$"を頭に付ける
amount = "$" + String( amount );

console.log( amount );		// "$199.98"
```

変数 `amount` は始め `99.99` という数字を持っていて、`number` 型です。従って、`amount * 2` の演算結果は `199.98` になります。

一つ目の `console.log(..)` コマンドは *暗黙的に* `number` 型の値を `string` 型の値に変換して出力します。 

式 `amount = "$" + String(amount)` では *明示的に* `199.98` という値を `string` 型に変換し、頭に `"$"` を加えています。この時点で `amount` は `string` 型の値 `"$199.98"` を保持しているため、二つ目の `console.log(..)` は値を出力するために型の変換をする必要がありません。

JavaScript開発者は変数 `amount` で `99.99`、`199.98`、`"$199.98"` を扱うとき、柔軟性を利用して変数の定義は1つのみとするでしょう。一方、静的型付け言語が好きな人は、最後の `"$199.98"` は型が他と異なるため、`amountStr` といった別の変数を用意することを好むはずです。

何にせよ、`amount` はプログラムを通して変化する値を保持しており、変数を用いる本来の目的であるプログラムの *状態* を表すという役割を果たしていることが分かるはずです。

言い換えれば、*状態* というのはプログラムが進むにつれて値が変化していく様を捉えることだと言うこともできます。

変数の他の一般的な変数の使い方としては、値の設定を分かりやすくまとめるというものがあります。このことは特に `定数` と呼ばれ、変数でありながらプログラムを通して `変化しない` ものを定義することを意味します。

`定数` は多くの場合プログラムの一番最初に定義します。これは必要なときに定数を別の値で書き換えるのに便利だからです。JavaScriptでは普通、定数の変数名を全て大文字にし、単語の区切りは `_` で表します。

例を見てみましょう。

```js
var TAX_RATE = 0.08;	// 8% の消費税

var amount = 99.99;

amount = amount * 2;

amount = amount + (amount * TAX_RATE);

console.log( amount );				// 215.9784
console.log( amount.toFixed( 2 ) );	// "215.98"
```

**注意:** `console.log(..)` が `console` のオブジェクトプロパティとして `log(..)` 関数にアクセスしているのと似たように、コード例にある `toFixed(..)` は `number` 型の値からアクセスできる関数です。JavaScriptの `number` 型は当然、自動的にドル表記にはしてくれません。JavaScriptエンジンはプログラマの意図を汲みませんし、JavaScriptには通貨を扱う型は存在しません。`toFixed(..)` は小数点第何位まで四捨五入を行うのかを設定し、四捨五入結果を `string` 型で返してくれる関数です。

`TAX_RATE` 変数は *定数* として定義していますが、これはただ慣例によるものです。というのも、プログラム中で `TAX_RATE` が書き換わることを防止するような特別なことは一切していないためです。国が消費税を10%に引き上げるときには、`TAX_RATE` を `0.10` に書き換えれば良いだけで、プログラムの更新は簡単に済みます。もし定数を使わ無かった場合、プログラム中に多数あるであろう `0.08` を全て `0.10` に書き換えなければいけません。

本書を執筆している時点で最新バージョンのJavaScript(一般的に「ES6」と呼ばれています)は *定数* を定義するときに `var` の代わりに `const` を用いるという新しい方法を採用しています。

```js
// ES6にて:
const TAX_RATE = 0.08;

var amount = 99.99;

// ..
```

`const` キーワードを使って定義した定数は(`var` キーワードを用いて定義した)値が変更されない変数と同じように有用です。異なるのは定数の初期設定が誤って他の箇所で書き換えられてしまうことを防止するということです。`TAX_VALUE` を最初に定義した後に他の値を代入しようとしても、プログラムは値の変更を拒絶します。(厳密モードではエラーが発生します。詳しくは「厳密モード」を参照。)

ところで、`const` キーワードで定義する定数のような「保護」機能でミスを防止することは静的型付け言語を使うことに似ています。なぜ静的型付け言語が魅力的なのかを垣間見ることができますね！

**注意:** プログラム内で変数のさまざまな値がどのように使われるのかについての詳細は *Types & Grammar* をご覧ください。

## ブロック

携帯電話ショップの店員は、あなたが携帯電話を購入するためにいくつかのステップを踏まなければなりません。

同じように、プログラムのコードでも一連の文をまとめる必要が出てくる場面は多くあります。このような文のまとまりのことを *ブロック* と言います。JavaScriptでは、ブロックは1行以上の文を中括弧 `{ .. }` で囲むことで定義できます。コード例を見てみましょう。

```js
var amount = 99.99;

// 一般的なブロック
{
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

このような独立した `{ .. }` というブロックは文法上間違いはありませんが、JSプログラムではあまり見かけません。一般的には、ブロックは `if` 文(詳しくは「条件」の項を参照)やループ(詳しくは「ループ」の項を参照)といった他の制御文とともに使います。例えば、次のようなコードがあります。

```js
var amount = 99.99;

// amountは十分大きいか？
if (amount > 10) {		// <-- `if` とともにブロックが使われている
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

`if` 文については次のセクションで解説しますが、2つの文を持った `{ .. }` ブロックが `if(amount > 10);` にくっついているのが見て取れると思います。ブロック内の文は条件に合致したときのみ実行されます。

**注意:** `console.log(amount);` などの他の文と違い、ブロック文は文末にセミコロン(`;`)を付ける必要はありません。

## Conditionals

"Do you want to add on the extra screen protectors to your purchase, for $9.99?" The helpful phone store employee has asked you to make a decision. And you may need to first consult the current *state* of your wallet or bank account to answer that question. But obviously, this is just a simple "yes or no" question.

There are quite a few ways we can express *conditionals* (aka decisions) in our programs.

The most common one is the `if` statement. Essentially, you're saying, "*If* this condition is true, do the following...". For example:

```js
var bank_balance = 302.13;
var amount = 99.99;

if (amount < bank_balance) {
	console.log( "I want to buy this phone!" );
}
```

The `if` statement requires an expression in between the parentheses `( )` that can be treated as either `true` or `false`. In this program, we provided the expression `amount < bank_balance`, which indeed will either evaluate to `true` or `false` depending on the amount in the `bank_balance` variable.

You can even provide an alternative if the condition isn't true, called an `else` clause. Consider:

```js
const ACCESSORY_PRICE = 9.99;

var bank_balance = 302.13;
var amount = 99.99;

amount = amount * 2;

// can we afford the extra purchase?
if ( amount < bank_balance ) {
	console.log( "I'll take the accessory!" );
	amount = amount + ACCESSORY_PRICE;
}
// otherwise:
else {
	console.log( "No, thanks." );
}
```

Here, if `amount < bank_balance` is `true`, we'll print out `"I'll take the accessory!"` and add the `9.99` to our `amount` variable. Otherwise, the `else` clause says we'll just politely respond with `"No, thanks."` and leave `amount` unchanged.

As we discussed in "Values & Types" earlier, values that aren't already of an expected type are often coerced to that type. The `if` statement expects a `boolean`, but if you pass it something that's not already `boolean`, coercion will occur.

JavaScript defines a list of specific values that are considered "falsy" because when coerced to a `boolean`, they become `false` -- these include values like `0` and `""`. Any other value not on the "falsy" list is automatically "truthy" -- when coerced to a `boolean` they become `true`. Truthy values include things like `99.99` and `"free"`. See "Truthy & Falsy" in Chapter 2 for more information.

*Conditionals* exist in other forms besides the `if`. For example, the `switch` statement can be used as a shorthand for a series of `if..else` statements (see Chapter 2). Loops (see "Loops") use a *conditional* to determine if the loop should keep going or stop.

**Note:** For deeper information about the coercions that can occur implicitly in the test expressions of *conditionals*, see Chapter 4 of the *Types & Grammar* title of this series.

## Loops

During busy times, there's a waiting list for customers who need to speak to the phone store employee. While there's still people on that list, she just needs to keep serving the next customer.

Repeating a set of actions until a certain condition fails -- in other words, repeating only while the condition holds -- is the job of programming loops; loops can take different forms, but they all satisfy this basic behavior.

A loop includes the test condition as well as a block (typically as `{ .. }`). Each time the loop block executes, that's called an *iteration*.

For example, the `while` loop and the `do..while` loop forms illustrate the concept of repeating a block of statements until a condition no longer evaluates to `true`:

```js
while (numOfCustomers > 0) {
	console.log( "How may I help you?" );

	// help the customer...

	numOfCustomers = numOfCustomers - 1;
}

// versus:

do {
	console.log( "How may I help you?" );

	// help the customer...

	numOfCustomers = numOfCustomers - 1;
} while (numOfCustomers > 0);
```

The only practical difference between these loops is whether the conditional is tested before the first iteration (`while`) or after the first iteration (`do..while`).

In either form, if the conditional tests as `false`, the next iteration will not run. That means if the condition is initially `false`, a `while` loop will never run, but a `do..while` loop will run just the first time.

Sometimes you are looping for the intended purpose of counting a certain set of numbers, like from `0` to `9` (ten numbers). You can do that by setting a loop iteration variable like `i` at value `0` and incrementing it by `1` each iteration.

**Warning:** For a variety of historical reasons, programming languages almost always count things in a zero-based fashion, meaning starting with `0` instead of `1`. If you're not familiar with that mode of thinking, it can be quite confusing at first. Take some time to practice counting starting with `0` to become more comfortable with it!

The conditional is tested on each iteration, much as if there is an implied `if` statement inside the loop.

We can use JavaScript's `break` statement to stop a loop. Also, we can observe that it's awfully easy to create a loop that would otherwise run forever without a `break`ing mechanism.

Let's illustrate:

```js
var i = 0;

// a `while..true` loop would run forever, right?
while (true) {
	// stop the loop?
	if ((i <= 9) === false) {
		break;
	}

	console.log( i );
	i = i + 1;
}
// 0 1 2 3 4 5 6 7 8 9
```

**Warning:** This is not necessarily a practical form you'd want to use for your loops. It's presented here for illustration purposes only.

While a `while` (or `do..while`) can accomplish the task manually, there's another syntactic form called a `for` loop for just that purpose:

```js
for (var i = 0; i <= 9; i = i + 1) {
	console.log( i );
}
// 0 1 2 3 4 5 6 7 8 9
```

As you can see, in both cases the conditional `i <= 9` is `true` for the first 10 iterations (`i` of values `0` through `9`) of either loop form, but becomes `false` once `i` is value `10`.

The `for` loop has three clauses: the initialization clause (`var i=0`), the conditional test clause (`i <= 9`), and the update clause (`i = i + 1`). So if you're going to do counting with your loop iterations, `for` is a more compact and often easier form to understand and write.

There are other specialized loop forms that are intended to iterate over specific values, such as the properties of an object (see Chapter 2) where the implied conditional test is just whether all the properties have been processed. The "loop until a condition fails" concept holds no matter what the form of the loop.

## Functions

The phone store employee probably doesn't carry around a calculator to figure out the taxes and final purchase amount. That's a task she needs to define once and reuse over and over again. Odds are, the company has a checkout register (computer, tablet, etc.) with those "functions" built in.

Similarly, your program will almost certainly want to break up the code's tasks into reusable pieces, instead of repeatedly repeating yourself repetitiously (pun intended!). The way to do this is to define a `function`.

A function is generally a named section of code that can be "called" by name, and the code inside it will be run each time. Consider:

```js
function printAmount() {
	console.log( amount.toFixed( 2 ) );
}

var amount = 99.99;

printAmount(); // "99.99"

amount = amount * 2;

printAmount(); // "199.98"
```

Functions can optionally take arguments (aka parameters) -- values you pass in. And they can also optionally return a value back.

```js
function printAmount(amt) {
	console.log( amt.toFixed( 2 ) );
}

function formatAmount() {
	return "$" + amount.toFixed( 2 );
}

var amount = 99.99;

printAmount( amount * 2 );		// "199.98"

amount = formatAmount();
console.log( amount );			// "$99.99"
```

The function `printAmount(..)` takes a parameter that we call `amt`. The function `formatAmount()` returns a value. Of course, you can also combine those two techniques in the same function.

Functions are often used for code that you plan to call multiple times, but they can also be useful just to organize related bits of code into named collections, even if you only plan to call them once.

Consider:

```js
const TAX_RATE = 0.08;

function calculateFinalPurchaseAmount(amt) {
	// calculate the new amount with the tax
	amt = amt + (amt * TAX_RATE);

	// return the new amount
	return amt;
}

var amount = 99.99;

amount = calculateFinalPurchaseAmount( amount );

console.log( amount.toFixed( 2 ) );		// "107.99"
```

Although `calculateFinalPurchaseAmount(..)` is only called once, organizing its behavior into a separate named function makes the code that uses its logic (the `amount = calculateFinal...` statement) cleaner. If the function had more statements in it, the benefits would be even more pronounced.

### Scope

If you ask the phone store employee for a phone model that her store doesn't carry, she will not be able to sell you the phone you want. She only has access to the phones in her store's inventory. You'll have to try another store to see if you can find the phone you're looking for.

Programming has a term for this concept: *scope* (technically called *lexical scope*). In JavaScript, each function gets its own scope. Scope is basically a collection of variables as well as the rules for how those variables are accessed by name. Only code inside that function can access that function's *scoped* variables.

A variable name has to be unique within the same scope -- there can't be two different `a` variables sitting right next to each other. But the same variable name `a` could appear in different scopes.

```js
function one() {
	// this `a` only belongs to the `one()` function
	var a = 1;
	console.log( a );
}

function two() {
	// this `a` only belongs to the `two()` function
	var a = 2;
	console.log( a );
}

one();		// 1
two();		// 2
```

Also, a scope can be nested inside another scope, just like if a clown at a birthday party blows up one balloon inside another balloon. If one scope is nested inside another, code inside the innermost scope can access variables from either scope.

Consider:

```js
function outer() {
	var a = 1;

	function inner() {
		var b = 2;

		// we can access both `a` and `b` here
		console.log( a + b );	// 3
	}

	inner();

	// we can only access `a` here
	console.log( a );			// 1
}

outer();
```

Lexical scope rules say that code in one scope can access variables of either that scope or any scope outside of it.

So, code inside the `inner()` function has access to both variables `a` and `b`, but code in `outer()` has access only to `a` -- it cannot access `b` because that variable is only inside `inner()`.

Recall this code snippet from earlier:

```js
const TAX_RATE = 0.08;

function calculateFinalPurchaseAmount(amt) {
	// calculate the new amount with the tax
	amt = amt + (amt * TAX_RATE);

	// return the new amount
	return amt;
}
```

The `TAX_RATE` constant (variable) is accessible from inside the `calculateFinalPurchaseAmount(..)` function, even though we didn't pass it in, because of lexical scope.

**Note:** For more information about lexical scope, see the first three chapters of the *Scope & Closures* title of this series.

## Practice

There is absolutely no substitute for practice in learning programming. No amount of articulate writing on my part is alone going to make you a programmer.

With that in mind, let's try practicing some of the concepts we learned here in this chapter. I'll give the "requirements," and you try it first. Then consult the code listing below to see how I approached it.

* Write a program to calculate the total price of your phone purchase. You will keep purchasing phones (hint: loop!) until you run out of money in your bank account. You'll also buy accessories for each phone as long as your purchase amount is below your mental spending threshold.
* After you've calculated your purchase amount, add in the tax, then print out the calculated purchase amount, properly formatted.
* Finally, check the amount against your bank account balance to see if you can afford it or not.
* You should set up some constants for the "tax rate," "phone price," "accessory price," and "spending threshold," as well as a variable for your "bank account balance.""
* You should define functions for calculating the tax and for formatting the price with a "$" and rounding to two decimal places.
* **Bonus Challenge:** Try to incorporate input into this program, perhaps with the `prompt(..)` covered in "Input" earlier. You may prompt the user for their bank account balance, for example. Have fun and be creative!

OK, go ahead. Try it. Don't peek at my code listing until you've given it a shot yourself!

**Note:** Because this is a JavaScript book, I'm obviously going to solve the practice exercise in JavaScript. But you can do it in another language for now if you feel more comfortable.

Here's my JavaScript solution for this exercise:

```js
const SPENDING_THRESHOLD = 200;
const TAX_RATE = 0.08;
const PHONE_PRICE = 99.99;
const ACCESSORY_PRICE = 9.99;

var bank_balance = 303.91;
var amount = 0;

function calculateTax(amount) {
	return amount * TAX_RATE;
}

function formatAmount(amount) {
	return "$" + amount.toFixed( 2 );
}

// keep buying phones while you still have money
while (amount < bank_balance) {
	// buy a new phone!
	amount = amount + PHONE_PRICE;

	// can we afford the accessory?
	if (amount < SPENDING_THRESHOLD) {
		amount = amount + ACCESSORY_PRICE;
	}
}

// don't forget to pay the government, too
amount = amount + calculateTax( amount );

console.log(
	"Your purchase: " + formatAmount( amount )
);
// Your purchase: $334.76

// can you actually afford this purchase?
if (amount > bank_balance) {
	console.log(
		"You can't afford this purchase. :("
	);
}
// You can't afford this purchase. :(
```

**Note:** The simplest way to run this JavaScript program is to type it into the developer console of your nearest browser.

How did you do? It wouldn't hurt to try it again now that you've seen my code. And play around with changing some of the constants to see how the program runs with different values.

## Review

Learning programming doesn't have to be a complex and overwhelming process. There are just a few basic concepts you need to wrap your head around.

These act like building blocks. To build a tall tower, you start first by putting block on top of block on top of block. The same goes with programming. Here are some of the essential programming building blocks:

* You need *operators* to perform actions on values.
* You need values and *types* to perform different kinds of actions like math on `number`s or output with `string`s.
* You need *variables* to store data (aka *state*) during your program's execution.
* You need *conditionals* like `if` statements to make decisions.
* You need *loops* to repeat tasks until a condition stops being true.
* You need *functions* to organize your code into logical and reusable chunks.

Code comments are one effective way to write more readable code, which makes your program easier to understand, maintain, and fix later if there are problems.

Finally, don't neglect the power of practice. The best way to learn how to write code is to write code.

I'm excited you're well on your way to learning how to code, now! Keep it up. Don't forget to check out other beginner programming resources (books, blogs, online training, etc.). This chapter and this book are a great start, but they're just a brief introduction.

The next chapter will review many of the concepts from this chapter, but from a more JavaScript-specific perspective, which will highlight most of the major topics that are addressed in deeper detail throughout the rest of the series.
