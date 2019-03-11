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

## Values & Types

If you ask an employee at a phone store how much a certain phone costs, and they say "ninety-nine, ninety-nine" (i.e., $99.99), they're giving you an actual numeric dollar figure that represents what you'll need to pay (plus taxes) to buy it. If you want to buy two of those phones, you can easily do the mental math to double that value to get $199.98 for your base cost.

If that same employee picks up another similar phone but says it's "free" (perhaps with air quotes), they're not giving you a number, but instead another kind of representation of your expected cost ($0.00) -- the word "free."

When you later ask if the phone includes a charger, that answer could only have been either "yes" or "no."

In very similar ways, when you express values in a program, you choose different representations for those values based on what you plan to do with them.

These different representations for values are called *types* in programming terminology. JavaScript has built-in types for each of these so called *primitive* values:

* When you need to do math, you want a `number`.
* When you need to print a value on the screen, you need a `string` (one or more characters, words, sentences).
* When you need to make a decision in your program, you need a `boolean` (`true` or `false`).

Values that are included directly in the source code are called *literals*. `string` literals are surrounded by double quotes `"..."` or single quotes (`'...'`) -- the only difference is stylistic preference. `number` and `boolean` literals are just presented as is (i.e., `42`, `true`, etc.).

Consider:

```js
"I am a string";
'I am also a string';

42;

true;
false;
```

Beyond `string`/`number`/`boolean` value types, it's common for programming languages to provide *arrays*, *objects*, *functions*, and more. We'll cover much more about values and types throughout this chapter and the next.

### Converting Between Types

If you have a `number` but need to print it on the screen, you need to convert the value to a `string`, and in JavaScript this conversion is called "coercion." Similarly, if someone enters a series of numeric characters into a form on an ecommerce page, that's a `string`, but if you need to then use that value to do math operations, you need to *coerce* it to a `number`.

JavaScript provides several different facilities for forcibly coercing between *types*. For example:

```js
var a = "42";
var b = Number( a );

console.log( a );	// "42"
console.log( b );	// 42
```

Using `Number(..)` (a built-in function) as shown is an *explicit* coercion from any other type to the `number` type. That should be pretty straightforward.

But a controversial topic is what happens when you try to compare two values that are not already of the same type, which would require *implicit* coercion.

When comparing the string `"99.99"` to the number `99.99`, most people would agree they are equivalent. But they're not exactly the same, are they? It's the same value in two different representations, two different *types*. You could say they're "loosely equal," couldn't you?

To help you out in these common situations, JavaScript will sometimes kick in and *implicitly* coerce values to the matching types.

So if you use the `==` loose equals operator to make the comparison `"99.99" == 99.99`, JavaScript will convert the left-hand side `"99.99"` to its `number` equivalent `99.99`. The comparison then becomes `99.99 == 99.99`, which is of course `true`.

While designed to help you, implicit coercion can create confusion if you haven't taken the time to learn the rules that govern its behavior. Most JS developers never have, so the common feeling is that implicit coercion is confusing and harms programs with unexpected bugs, and should thus be avoided. It's even sometimes called a flaw in the design of the language.

However, implicit coercion is a mechanism that *can be learned*, and moreover *should be learned* by anyone wishing to take JavaScript programming seriously. Not only is it not confusing once you learn the rules, it can actually make your programs better! The effort is well worth it.

**Note:** For more information on coercion, see Chapter 2 of this title and Chapter 4 of the *Types & Grammar* title of this series.

## Code Comments

The phone store employee might jot down some notes on the features of a newly released phone or on the new plans her company offers. These notes are only for the employee -- they're not for customers to read. Nevertheless, these notes help the employee do her job better by documenting the hows and whys of what she should tell customers.

One of the most important lessons you can learn about writing code is that it's not just for the computer. Code is every bit as much, if not more, for the developer as it is for the compiler.

Your computer only cares about machine code, a series of binary 0s and 1s, that comes from *compilation*. There's a nearly infinite number of programs you could write that yield the same series of 0s and 1s. The choices you make about how to write your program matter -- not only to you, but to your other team members and even to your future self.

You should strive not just to write programs that work correctly, but programs that make sense when examined. You can go a long way in that effort by choosing good names for your variables (see "Variables") and functions (see "Functions").

But another important part is code comments. These are bits of text in your program that are inserted purely to explain things to a human. The interpreter/compiler will always ignore these comments.

There are lots of opinions on what makes well-commented code; we can't really define absolute universal rules. But some observations and guidelines are quite useful:

* Code without comments is suboptimal.
* Too many comments (one per line, for example) is probably a sign of poorly written code.
* Comments should explain *why*, not *what*. They can optionally explain *how* if that's particularly confusing.

In JavaScript, there are two types of comments possible: a single-line comment and a multiline comment.

Consider:

```js
// This is a single-line comment

/* But this is
       a multiline
             comment.
                      */
```

The `//` single-line comment is appropriate if you're going to put a comment right above a single statement, or even at the end of a line. Everything on the line after the `//` is treated as the comment (and thus ignored by the compiler), all the way to the end of the line. There's no restriction to what can appear inside a single-line comment.

Consider:

```js
var a = 42;		// 42 is the meaning of life
```

The `/* .. */` multiline comment is appropriate if you have several lines worth of explanation to make in your comment.

Here's a common usage of multiline comments:

```js
/* The following value is used because
   it has been shown that it answers
   every question in the universe. */
var a = 42;
```

It can also appear anywhere on a line, even in the middle of a line, because the `*/` ends it. For example:

```js
var a = /* arbitrary value */ 42;

console.log( a );	// 42
```

The only thing that cannot appear inside a multiline comment is a `*/`, because that would be interpreted to end the comment.

You will definitely want to begin your learning of programming by starting off with the habit of commenting code. Throughout the rest of this chapter, you'll see I use comments to explain things, so do the same in your own practice. Trust me, everyone who reads your code will thank you!

## Variables

Most useful programs need to track a value as it changes over the course of the program, undergoing different operations as called for by your program's intended tasks.

The easiest way to go about that in your program is to assign a value to a symbolic container, called a *variable* -- so called because the value in this container can *vary* over time as needed.

In some programming languages, you declare a variable (container) to hold a specific type of value, such as `number` or `string`. *Static typing*, otherwise known as *type enforcement*, is typically cited as a benefit for program correctness by preventing unintended value conversions.

Other languages emphasize types for values instead of variables. *Weak typing*, otherwise known as *dynamic typing*, allows a variable to hold any type of value at any time. It's typically cited as a benefit for program flexibility by allowing a single variable to represent a value no matter what type form that value may take at any given moment in the program's logic flow.

JavaScript uses the latter approach, *dynamic typing*, meaning variables can hold values of any *type* without any *type* enforcement.

As mentioned earlier, we declare a variable using the `var` statement -- notice there's no other *type* information in the declaration. Consider this simple program:

```js
var amount = 99.99;

amount = amount * 2;

console.log( amount );		// 199.98

// convert `amount` to a string, and
// add "$" on the beginning
amount = "$" + String( amount );

console.log( amount );		// "$199.98"
```

The `amount` variable starts out holding the number `99.99`, and then holds the `number` result of `amount * 2`, which is `199.98`.

The first `console.log(..)` command has to *implicitly* coerce that `number` value to a `string` to print it out.

Then the statement `amount = "$" + String(amount)` *explicitly* coerces the `199.98` value to a `string` and adds a `"$"` character to the beginning. At this point, `amount` now holds the `string` value `"$199.98"`, so the second `console.log(..)` statement doesn't need to do any coercion to print it out.

JavaScript developers will note the flexibility of using the `amount` variable for each of the `99.99`, `199.98`, and the `"$199.98"` values. Static-typing enthusiasts would prefer a separate variable like `amountStr` to hold the final `"$199.98"` representation of the value, because it's a different type.

Either way, you'll note that `amount` holds a running value that changes over the course of the program, illustrating the primary purpose of variables: managing program *state*.

In other words, *state* is tracking the changes to values as your program runs.

Another common usage of variables is for centralizing value setting. This is more typically called *constants*, when you declare a variable with a value and intend for that value to *not change* throughout the program.

You declare these *constants*, often at the top of a program, so that it's convenient for you to have one place to go to alter a value if you need to. By convention, JavaScript variables as constants are usually capitalized, with underscores `_` between multiple words.

Here's a silly example:

```js
var TAX_RATE = 0.08;	// 8% sales tax

var amount = 99.99;

amount = amount * 2;

amount = amount + (amount * TAX_RATE);

console.log( amount );				// 215.9784
console.log( amount.toFixed( 2 ) );	// "215.98"
```

**Note:** Similar to how `console.log(..)` is a function `log(..)` accessed as an object property on the `console` value, `toFixed(..)` here is a function that can be accessed on `number` values. JavaScript `number`s aren't automatically formatted for dollars -- the engine doesn't know what your intent is and there's no type for currency. `toFixed(..)` lets us specify how many decimal places we'd like the `number` rounded to, and it produces the `string` as necessary.

The `TAX_RATE` variable is only *constant* by convention -- there's nothing special in this program that prevents it from being changed. But if the city raises the sales tax rate to 9%, we can still easily update our program by setting the `TAX_RATE` assigned value to `0.09` in one place, instead of finding many occurrences of the value `0.08` strewn throughout the program and updating all of them.

The newest version of JavaScript at the time of this writing (commonly called "ES6") includes a new way to declare *constants*, by using `const` instead of `var`:

```js
// as of ES6:
const TAX_RATE = 0.08;

var amount = 99.99;

// ..
```

Constants are useful just like variables with unchanged values, except that constants also prevent accidentally changing value somewhere else after the initial setting. If you tried to assign any different value to `TAX_RATE` after that first declaration, your program would reject the change (and in strict mode, fail with an error -- see "Strict Mode" in Chapter 2).

By the way, that kind of "protection" against mistakes is similar to the static-typing type enforcement, so you can see why static types in other languages can be attractive!

**Note:** For more information about how different values in variables can be used in your programs, see the *Types & Grammar* title of this series.

## Blocks

The phone store employee must go through a series of steps to complete the checkout as you buy your new phone.

Similarly, in code we often need to group a series of statements together, which we often call a *block*. In JavaScript, a block is defined by wrapping one or more statements inside a curly-brace pair `{ .. }`. Consider:

```js
var amount = 99.99;

// a general block
{
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

This kind of standalone `{ .. }` general block is valid, but isn't as commonly seen in JS programs. Typically, blocks are attached to some other control statement, such as an `if` statement (see "Conditionals") or a loop (see "Loops"). For example:

```js
var amount = 99.99;

// is amount big enough?
if (amount > 10) {			// <-- block attached to `if`
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

We'll explain `if` statements in the next section, but as you can see, the `{ .. }` block with its two statements is attached to `if (amount > 10)`; the statements inside the block will only be processed if the conditional passes.

**Note:** Unlike most other statements like `console.log(amount);`, a block statement does not need a semicolon (`;`) to conclude it.

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
