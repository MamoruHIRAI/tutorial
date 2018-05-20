{% set warning_icon = '<span class="glyphicon glyphicon-exclamation-sign" style="color: red;" aria-hidden="true" data-toggle="tooltip" title="An error is expected when you run this command!" ></span>' %}

# Introduction to Python

> このチャプターの一部はGeek Girls Carrotsのチュートリアルをもとにしています。(https://github.com/ggcarrots/django-carrots)

さあ、コードを書いてみましょう！

## Python prompt

> For readers at home: this part is covered in the [Python Basics: Integers, Strings, Lists, Variables and Errors](https://www.youtube.com/watch?v=MO63L4s-20U) video.

Pythonであそぶために、*コマンドライン* を開きましょう。 やり方は、チャプター [Intro to Command Line](../intro_to_command_line/README.md) で学びましたね。

準備ができたら、次の指示に従ってやってみましょう。

Pythonコンソールを開きましょう。Windowsなら `python` 、Mac OSやLinuxなら `python3` とタイプして `Enter` キーを押してください。

{% filename %}command-line{% endfilename %}

    $ python3
    Python 3.6.1 (...)
    Type "help", "copyright", "credits" or "license" for more information.
    >>>
    

## Your first Python command!

Pythonのコマンドが走ると、プロンプト記号が `>>>` に変わりました。 これは、今Pythonの言語を実行できますという意味です。 `>>>` はタイプしなくていいですよ。 – Pythonがあなたの代わりにやってくれます。

Pythonコンソールを終わる時は、`exit()` とタイプするか、ショートカット `Ctrl + Z`（Windows）、`Ctrl + D`（Mac/Linux）で終了です。 `>>>` は現れなくなりました。

けど、今はまだコンソールを終了しないで、もっと動かして学びましょう。簡単な計算からはじめましょう。`2 + 3` とタイプして、`Enter` キーを押してください。

{% filename %}command-line{% endfilename %}

```python
>>> 2 + 3
5
```

できました！答えがでてきましたね。Pythonは計算ができます。他にも、次のようなコマンドを試してみましょう。

- `4 * 5`
- `5 - 1`
- `40 / 2`

2の3乗のような指数の計算は、次のようにタイプします。{% filename %}command-line{% endfilename %}

```python
>>> 2 ** 3
8
```

ちょっとの間楽しんであそんでみたら、またココに戻ってきてくださいね。:)

お分かりのとおり、Pythonはステキな計算機ですね. 他になにができるんだろう…と思ったら、次にいってみましょう。

## Strings

あなたのお名前を次のようにクォーテーションをつけてタイプしてください。

{% filename %}command-line{% endfilename %}

```python
>>> "Ola"
'Ola'
```

はじめてのString（文字列）が完成です！ Stringとは、文字の集合のことです。 シングルクォーテーション (`'`) あるいは、ダブルクォーテーション (`"`) で囲います。 最初と最後は同じ記号にしてください。 - クォーテーションの中が文字列であることを意味しています。

複数の文字列を結合することもできます。次のように試してみましょう。

{% filename %}command-line{% endfilename %}

```python
>>> "Hi there " + "Ola"
'Hi there Ola'
```

文字列を繰り返すためには、演算子を使って繰り返し回数を指定することもできます。

{% filename %}command-line{% endfilename %}

```python
>>> "Ola" * 3
'OlaOlaOla'
```

アポストロフィーを文字列の中に含めたい場合は、２通りの方法があります。

まずは、ダブルクォーテーションを使う方法です。

{% filename %}command-line{% endfilename %}

```python
>>> "Runnin' down the hill"
"Runnin' down the hill"
```

あるいは、バックスラッシュ (``) を使う方法もあります。

{% filename %}command-line{% endfilename %}

```python
>>> 'Runnin\' down the hill'
"Runnin' down the hill"
```

できましたか？次に、あなたの名前を大文字に変えてみましょう。次のように記述してください。

{% filename %}command-line{% endfilename %}

```python
>>> "Ola".upper()
'OLA'
```

ここで `upper` **関数 (function)** を使うことができましたね！ 関数 ( `upper()` など) は、呼び出したオブジェクト ( `"Ola"` のことです) に対してどのような手順でどのような処理をするかをひとまとめにしたものです。

あなたの名前の文字数を知りたいときは、その **関数** もあります！

{% filename %}command-line{% endfilename %}

```python
>>> len("Ola")
3
```

どうして、文字列の後に `.` をつけて関数を呼び出したり ( `"Ola".upper()` のように)、あるいは、先に関数を呼び出してかっこの中に文字列をいれているのか、と疑問に思ったかもしれません。 そうですね。時に、オブジェクトに結びついた関数というのがあります。例えば、`upper()` は、文字列にのみ実行される関数です。 私たちはこれを **メソッド (method)** と呼びます。 それとは別に、特定のオブジェクトに関連せず、異なるタイプのオブジェクトに対して実行できる関数があります。例えば `len()` ですね。 `len` 関数の引数として `"Ola"` をかっこの中にいれているのです。

### 概要

文字列はだいじょうぶですね。ここまでに学んだことをまとめましょう。

- **プロンプト** – Pythonプロンプトにコマンド（コード）を入力すると、答えがかえってきます。
- **数値と文字列** – 数値は計算に、文字列はテキストに使われます。
- **演算子** – 例えば `+` や `*` のように、値を計算して新しい値を返します。
- **関数** – `upper()` や `len()` のようにオブジェクトに対して行う機能のことです。

すべてのプログラミング言語に共通する基礎になります。 もう少し難易度の高いものに挑戦してみましょう。準備はいいですか？

## Errors

さて、新しいことをやってみましょう。あなたの名前の文字数を数えたように、数字の文字列は数えられるでしょうか？ `len(304023)` と記述して、`Enter` キーを押してみましょう。

{% filename %}{{ warning_icon }} command-line{% endfilename %}

```python
>>> len(304023)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: object of type 'int' has no len()
```

はじめてのエラーがでました！ {{ warning_icon }} アイコンのついたコードは思ったように動かないコードです。 （今回はチュートリアルで用意されていましたが）思ったように動かないことは学ぶ上で大事な経験です！

オブジェクトタイプ"int" (integers, 数値) は文字数がありませんと言っています。では、どうすればよいでしょうか？この数字を文字列として扱えれば、文字数を数えられるはずですよね？

{% filename %}command-line{% endfilename %}

```python
>>> len(str(304023))
6
```

うまく行きました！ `str` 関数を `len` の中に記述しました。`str()` はその中身を文字列に変換します。

- `str` 関数は、**文字列** に変換します。
- `int` 関数は、文字列や数値を **整数** に変換します。

> 重要！: 数字は文字列にすることはできますが、全ての文字が数字に変換できるわけではありません。 例えば `int('hello')` は数字にはなりませんよね？

## Variables

変数（variables）は、プログラミングの重要なコンセプトです。 後で使うためにつける単なる名札ではありません。 プログラマーは変数を使ってデータを保管したり、 コードを読みやすくして、後でそれが何だったか覚えておかなくてもいいようにします。

変数 `name` を新しくつくってみましょう。

{% filename %}command-line{% endfilename %}

```python
>>> name = "Ola"
```

name イコール（=）Ola とタイプします。

見てのとおり、プログラムは、なにも返してくれませんね。では、変数がきちんとあるか、どうやって確かめたらいいのでしょうか？ `name` とタイプして、`Enter` キーを押してください。

{% filename %}command-line{% endfilename %}

```python
>>> name
'Ola'
```

やりました！あなたのはじめての変数ができましたね！代入する値を変えることもできます。

{% filename %}command-line{% endfilename %}

```python
>>> name = "Sonja"
>>> name
'Sonja'
```

変数には関数も使えます。

{% filename %}command-line{% endfilename %}

```python
>>> len(name)
5
```

素晴らしいですね！変数は、もちろん数値にも使えますよ。

{% filename %}command-line{% endfilename %}

```python
>>> a = 4
>>> b = 6
>>> a * b
24
```

もしも、間違えた変数名を使ってしまったら、どうなるでしょうか？予想できますか？やってみましょう！

{% filename %}{{ warning_icon }} command-line{% endfilename %}

```python
>>> city = "Tokyo"
>>> ctiy
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'ctiy' is not defined
```

エラーになりました！ 前回とは違うエラータイプです。**NameError** という、初めてみるエラータイプですね。 作成されていない変数を使った時は、Pythonがエラーを教えてくれます。 If you encounter this error later, check your code to see if you've mistyped any names.

Play with this for a while and see what you can do!

## The print function

Try this:

{% filename %}command-line{% endfilename %}

```python
>>> name = 'Maria'
>>> name
'Maria'
>>> print(name)
Maria
```

When you just type `name`, the Python interpreter responds with the string *representation* of the variable 'name', which is the letters M-a-r-i-a, surrounded by single quotes, ''. When you say `print(name)`, Python will "print" the contents of the variable to the screen, without the quotes, which is neater.

As we'll see later, `print()` is also useful when we want to print things from inside functions, or when we want to print things on multiple lines.

## Lists

Beside strings and integers, Python has all sorts of different types of objects. Now we're going to introduce one called **list**. Lists are exactly what you think they are: objects which are lists of other objects. :)

Go ahead and create a list:

{% filename %}command-line{% endfilename %}

```python
>>> []
[]
```

Yes, this list is empty. Not very useful, right? Let's create a list of lottery numbers. We don't want to repeat ourselves all the time, so we will put it in a variable, too:

{% filename %}command-line{% endfilename %}

```python
>>> lottery = [3, 42, 12, 19, 30, 59]
```

All right, we have a list! What can we do with it? Let's see how many lottery numbers there are in a list. Do you have any idea which function you should use for that? You know this already!

{% filename %}command-line{% endfilename %}

```python
>>> len(lottery)
6
```

Yes! `len()` can give you a number of objects in a list. Handy, right? Maybe we will sort it now:

{% filename %}command-line{% endfilename %}

```python
>>> lottery.sort()
```

This doesn't return anything, it just changed the order in which the numbers appear in the list. Let's print it out again and see what happened:

{% filename %}command-line{% endfilename %}

```python
>>> print(lottery)
[3, 12, 19, 30, 42, 59]
```

As you can see, the numbers in your list are now sorted from the lowest to highest value. Congrats!

Maybe we want to reverse that order? Let's do that!

{% filename %}command-line{% endfilename %}

```python
>>> lottery.reverse()
>>> print(lottery)
[59, 42, 30, 19, 12, 3]
```

If you want to add something to your list, you can do this by typing this command:

{% filename %}command-line{% endfilename %}

```python
>>> lottery.append(199)
>>> print(lottery)
[59, 42, 30, 19, 12, 3, 199]
```

If you want to show only the first number, you can do this by using **indexes**. An index is the number that says where in a list an item occurs. Programmers prefer to start counting at 0, so the first object in your list is at index 0, the next one is at 1, and so on. Try this:

{% filename %}command-line{% endfilename %}

```python
>>> print(lottery[0])
59
>>> print(lottery[1])
42
```

As you can see, you can access different objects in your list by using the list's name and the object's index inside of square brackets.

To delete something from your list you will need to use **indexes** as we learned above and the `pop()` method. Let's try an example and reinforce what we learned previously; we will be deleting the first number of our list.

{% filename %}command-line{% endfilename %}

```python
>>> print(lottery)
[59, 42, 30, 19, 12, 3, 199]
>>> print(lottery[0])
59
>>> lottery.pop(0)
59
>>> print(lottery)
[42, 30, 19, 12, 3, 199]
```

That worked like a charm!

For extra fun, try some other indexes: 6, 7, 1000, -1, -6 or -1000. See if you can predict the result before trying the command. Do the results make sense?

You can find a list of all available list methods in this chapter of the Python documentation: https://docs.python.org/3/tutorial/datastructures.html

## Dictionaries

> For readers at home: this part is covered in the [Python Basics: Dictionaries](https://www.youtube.com/watch?v=ZX1CVvZLE6c) video.

A dictionary is similar to a list, but you access values by looking up a key instead of a numeric index. A key can be any string or number. The syntax to define an empty dictionary is:

{% filename %}command-line{% endfilename %}

```python
>>> {}
{}
```

This shows that you just created an empty dictionary. Hurray!

Now, try writing the following command (try substituting your own information, too):

{% filename %}command-line{% endfilename %}

```python
>>> participant = {'name': 'Ola', 'country': 'Poland', 'favorite_numbers': [7, 42, 92]}
```

With this command, you just created a variable named `participant` with three key–value pairs:

- キー `name` が指す値 `'オーラ'` (`string` オブジェクト)
- キー `country` が指す値 `'Poland'` (`string` オブジェクト),
- キー `favorite_numbers/0> は リスト <code>[7, 42, 92]/0>。 (数字を3つ持つlist).</li>
</ul>

<p>You can check the content of individual keys with this syntax:</p>

<p>{% filename %}command-line{% endfilename %}</p>

<pre><code class="python">>>> print(participant['name'])
Ola
`</pre> 
    See, it's similar to a list. But you don't need to remember the index – just the name.
    
    What happens if we ask Python the value of a key that doesn't exist? Can you guess? Let's try it and see!
    
    {% filename %}{{ warning_icon }} command-line{% endfilename %}
    
    ```python
    >>> participant['age']
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    KeyError: 'age'
    ```
    
    Look, another error! This one is a **KeyError**. Python is helpful and tells you that the key `'age'` doesn't exist in this dictionary.
    
    When should you use a dictionary or a list? Well, that's a good point to ponder. Just have a solution in mind before looking at the answer in the next line.
    
    - 必要なのは、順序付けられた一連のアイテムですか？　リストを使いましょう。
    - キーに対応する値が必要？キーから値を参照する？　ディクショナリを使いましょう。
    
    Dictionaries, like lists, are *mutable*, meaning that they can be changed after they are created. You can add new key–value pairs to a dictionary after it is created, like this:
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    >>> participant['favorite_language'] = 'Python'
    ```
    
    Like lists, using the `len()` method on the dictionaries returns the number of key–value pairs in the dictionary. Go ahead and type in this command:
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    >>> len(participant)
    4
    ```
    
    I hope it makes sense up to now. :) Ready for some more fun with dictionaries? Read on for some amazing things.
    
    You can use the `pop()` method to delete an item in the dictionary. Say, if you want to delete the entry corresponding to the key `'favorite_numbers'`, just type in the following command:
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    >>> participant.pop('favorite_numbers')
    [7, 42, 92]
    >>> participant
    {'country': 'Poland', 'favorite_language': 'Python', 'name': 'Ola'}
    ```
    
    As you can see from the output, the key–value pair corresponding to the 'favorite_numbers' key has been deleted.
    
    As well as this, you can also change a value associated with an already-created key in the dictionary. Type this:
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    >>> participant['country'] = 'Germany'
    >>> participant
    {'country': 'Germany', 'favorite_language': 'Python', 'name': 'Ola'}
    ```
    
    As you can see, the value of the key `'country'` has been altered from `'Poland'` to `'Germany'`. :) Exciting? Hurrah! You just learned another amazing thing.
    
    ### 概要
    
    Awesome! You know a lot about programming now. In this last part you learned about:
    
    - **errors** – you now know how to read and understand errors that show up if Python doesn't understand a command you've given it
    - **variables** – names for objects that allow you to code more easily and to make your code more readable
    - **lists** – lists of objects stored in a particular order
    - **dictionaries** – objects stored as key–value pairs
    
    Excited for the next part? :)
    
    ## Compare things
    
    > For readers at home: this part is covered in the [Python Basics: Comparisons](https://www.youtube.com/watch?v=7bzxqIKYgf4) video.
    
    A big part of programming involves comparing things. What's the easiest thing to compare? Numbers, of course. Let's see how that works:
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    >>> 5 > 2
    True
    >>> 3 < 1
    False
    >>> 5 > 2 * 2
    True
    >>> 1 == 1
    True
    >>> 5 != 2
    True
    ```
    
    We gave Python some numbers to compare. As you can see, not only can Python compare numbers, but it can also compare method results. Nice, huh?
    
    Do you wonder why we put two equal signs `==` next to each other to compare if numbers are equal? We use a single `=` for assigning values to variables. You always, **always** need to put two of them – `==` – if you want to check if things are equal to each other. We can also state that things are unequal to each other. For that, we use the symbol `!=`, as shown in the example above.
    
    Give Python two more tasks:
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    >>> 6 >= 12 / 2
    True
    >>> 3 <= 2
    False
    ```
    
    We've seen `>` and `<`, but what do `>=` and `<=` mean? Read them like this:
    
    - x > y : x は y　より大きい
    - x < y : x は y　より小さい
    - x <= y : x は y　以下
    - x >= y : x は y　以上
    
    Awesome! Wanna do one more? Try this:
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    >>> 6 > 2 and 2 < 3
    True
    >>> 3 > 2 and 2 < 1
    False
    >>> 3 > 2 or 2 < 1
    True
    ```
    
    You can give Python as many numbers to compare as you want, and it will give you an answer! Pretty smart, right?
    
    - **and** – if you use the `and` operator, both comparisons have to be True in order for the whole command to be True
    - **or** – if you use the `or` operator, only one of the comparisons has to be True in order for the whole command to be True
    
    Have you heard of the expression "comparing apples to oranges"? Let's try the Python equivalent:
    
    {% filename %}{{ warning_icon }} command-line{% endfilename %}
    
    ```python
    >>> 1 > 'django'
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    TypeError: '>' not supported between instances of 'int' and 'str'
    ```
    
    Here you see that just like in the expression, Python is not able to compare a number (`int`) and a string (`str`). Instead, it shows a **TypeError** and tells us the two types can't be compared together.
    
    ## Boolean
    
    Incidentally, you just learned about a new type of object in Python. It's called **Boolean**.
    
    There are only two Boolean objects:
    
    - True
    - False
    
    But for Python to understand this, you need to always write it as 'True' (first letter uppercase, with the rest of the letters lowercased). **true, TRUE, and tRUE won't work – only True is correct.** (The same applies to 'False' as well, of course.)
    
    Booleans can be variables, too! See here:
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    >>> a = True
    >>> a
    True
    ```
    
    You can also do it this way:
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    >>> a = 2 > 5
    >>> a
    False
    ```
    
    Practice and have fun with Booleans by trying to run the following commands:
    
    - `True and True`
    - `False and True`
    - `True or 1 == 1`
    - `1 != 2`
    
    Congrats! Booleans are one of the coolest features in programming, and you just learned how to use them!
    
    # Save it!
    
    > For readers at home: this part is covered in the [Python Basics: Saving files and "If" statement](https://www.youtube.com/watch?v=dOAg6QVAxyk) video.
    
    So far we've been writing all our python code in the interpreter, which limits us to entering one line of code at a time. Normal programs are saved in files and executed by our programming language **interpreter** or **compiler**. So far we've been running our programs one line at a time in the Python **interpreter**. We're going to need more than one line of code for the next few tasks, so we'll quickly need to:
    
    - Pythonインタプリタを終了します。
    - お好きなエディタを起動します。
    - Pythonファイルとしてコードを保存します。
    - 実行します！
    
    To exit from the Python interpreter that we've been using, simply type the `exit()` function
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    >>> exit()
    $
    ```
    
    This will put you back into the command prompt.
    
    Earlier, we picked out a code editor from the [code editor](../code_editor/README.md) section. We'll need to open the editor now and write some code into a new file:
    
    {% filename %}editor{% endfilename %}
    
    ```python
    print('Hello, Django girls!')
    ```
    
    Obviously, you're a pretty seasoned Python developer now, so feel free to write some code that you've learned today.
    
    Now we need to save the file and give it a descriptive name. Let's call the file **python_intro.py** and save it to your desktop. We can name the file anything we want, but the important part here is to make sure the file ends in **.py**. The **.py** extension tells our operating system that this is a **Python executable file** and Python can run it.
    
    > **Note** You should notice one of the coolest thing about code editors: colors! In the Python console, everything was the same color; now you should see that the `print` function is a different color from the string. これは「構文」と呼ばれています「ハイライトする」こと、そして、コーディングとき、それは本当に役に立つ特徴です。 The color of things will give you hints, such as unclosed strings or a typo in a keyword name (like the `def` in a function, which we'll see below). これが私たちがコードエディタを使う理由の１つです. :)
    
    With the file saved, it's time to run it! Using the skills you've learned in the command line section, use the terminal to **change directories** to the desktop.
    
    <!--sec data-title="Change directory: OS X" data-id="python_OSX"
data-collapse=true ces-->
    
    On a Mac, the command will look something like this:
    
    {% filename %}command-line{% endfilename %}
    
        $ cd ~/Desktop
        
    
    <!--endsec-->
    
    <!--sec data-title="Change directory: Linux" data-id="python_linux"
data-collapse=true ces-->
    
    On Linux, it will be like this (the word "Desktop" might be translated to your local language):
    
    {% filename %}command-line{% endfilename %}
    
        $ cd ~/Desktop
        
    
    <!--endsec-->
    
    <!--sec data-title="Change directory: Windows Command Prompt" data-id="python_windows" data-collapse=true ces-->
    
    On Windows Command Prompt, it will be like this:
    
    {% filename %}command-line{% endfilename %}
    
        > cd %HomePath%\Desktop
        
    
    <!--endsec-->
    
    <!--sec data-title="Change directory: Windows Powershell" data-id="python_windowsPSH" data-collapse=true ces-->
    
    And on Windows Powershell, it will be like this:
    
    {% filename %}command-line{% endfilename %}
    
        > cd $Home\Desktop
        
    
    <!--endsec-->
    
    If you get stuck, just ask for help.
    
    Now use Python to execute the code in the file like this:
    
    {% filename %}command-line{% endfilename %}
    
        $ python3 python_intro.py
        Hello, Django girls!
        
    
    Note: on Windows 'python3' is not recognized as a command. Instead, use 'python' to execute the file:
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    > python python_intro.py
    ```
    
    Alright! You just ran your first Python program that was saved to a file. Feel awesome?
    
    You can now move on to an essential tool in programming:
    
    ## If … elif … else
    
    Lots of things in code should be executed only when given conditions are met. That's why Python has something called **if statements**.
    
    Replace the code in your **python_intro.py** file with this:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    if 3 > 2:
    ```
    
    If we were to save and run this, we'd see an error like this:
    
    {% filename %}{{ warning_icon }} command-line{% endfilename %}
    
        $ python3 python_intro.py
        File "python_intro.py", line 2
                 ^
        SyntaxError: unexpected EOF while parsing
        
    
    Python expects us to give further instructions to it which are executed if the condition `3 > 2` turns out to be true (or `True` for that matter). Let’s try to make Python print “It works!”. Change your code in your **python_intro.py** file to this:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    if 3 > 2:
        print('It works!')
    ```
    
    Notice how we've indented the next line of code by 4 spaces? We need to do this so Python knows what code to run if the result is true. You can do one space, but nearly all Python programmers do 4 to make things look neat. A single `tab` will also count as 4 spaces.
    
    Save it and give it another run:
    
    {% filename %}command-line{% endfilename %}
    
    ```python
    $ python3 python_intro.py
    It works!
    ```
    
    Note: Remember that on Windows, 'python3' is not recognized as a command. From now on, replace 'python3' with 'python' to execute the file.
    
    ### What if a condition isn't True?
    
    In previous examples, code was executed only when the conditions were True. But Python also has `elif` and `else` statements:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    if 5 > 2:
        print('5 is indeed greater than 2')
    else:
        print('5 is not greater than 2')
    ```
    
    When this is run it will print out:
    
    {% filename %}command-line{% endfilename %}
    
        $ python3 python_intro.py
        5 is indeed greater than 2
        
    
    If 2 were a greater number than 5, then the second command would be executed. Let's see how `elif` works:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    name = 'Sonja'
    if name == 'Ola':
        print('Hey Ola!')
    elif name == 'Sonja':
        print('Hey Sonja!')
    else:
        print('Hey anonymous!')
    ```
    
    and executed:
    
    {% filename %}command-line{% endfilename %}
    
        $ python3 python_intro.py
        Hey Sonja!
        
    
    See what happened there? `elif` lets you add extra conditions that run if the previous conditions fail.
    
    You can add as many `elif` statements as you like after your initial `if` statement. For example:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    volume = 57
    if volume < 20:
        print("It's kinda quiet.")
    elif 20 <= volume < 40:
        print("It's nice for background music")
    elif 40 <= volume < 60:
        print("Perfect, I can hear all the details")
    elif 60 <= volume < 80:
        print("Nice for parties")
    elif 80 <= volume < 100:
        print("A bit loud!")
    else:
        print("My ears are hurting! :(")
    ```
    
    Python runs through each test in sequence and prints:
    
    {% filename %}command-line{% endfilename %}
    
        $ python3 python_intro.py
        Perfect, I can hear all the details
        
    
    ## Comments
    
    Comments are lines beginning with `#`. You can write whatever you want after the `#` and Python will ignore it. Comments can make your code easier for other people to understand.
    
    Let's see how that looks:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    # Change the volume if it's too loud or too quiet
    if volume < 20 or volume > 80:
        volume = 50
        print("That's better!")
    ```
    
    You don't need to write a comment for every line of code, but they are useful for explaining why your code is doing something, or providing a summary when it's doing something complex.
    
    ### 概要
    
    In the last few exercises you learned about:
    
    - **comparing things** – in Python you can compare things by using `>`, `>=`, `==`, `<=`, `<` and the `and`, `or` operators
    - **Boolean** – a type of object that can only have one of two values: `True` or `False`
    - **Saving files** – storing code in files so you can execute larger programs.
    - **if … elif … else** – statements that allow you to execute code only when certain conditions are met.
    - **comments** - lines that Python won't run which let you document your code
    
    Time for the last part of this chapter!
    
    ## Your own functions!
    
    > For readers at home: this part is covered in the [Python Basics: Functions](https://www.youtube.com/watch?v=5owr-6suOl0) video.
    
    Remember functions like `len()` that you can execute in Python? Well, good news – you will learn how to write your own functions now!
    
    A function is a sequence of instructions that Python should execute. Each function in Python starts with the keyword `def`, is given a name, and can have some parameters. Let's give it a go. Replace the code in **python_intro.py** with the following:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    def hi():
        print('Hi there!')
        print('How are you?')
    
    hi()
    ```
    
    Okay, our first function is ready!
    
    You may wonder why we've written the name of the function at the bottom of the file. This is because Python reads the file and executes it from top to bottom. So in order to use our function, we have to re-write it at the bottom.
    
    Let's run this now and see what happens:
    
    {% filename %}command-line{% endfilename %}
    
        $ python3 python_intro.py
        Hi there!
        How are you?
        
    
    Note: if it didn't work, don't panic! The output will help you to figure why:
    
    - If you get a `NameError`, that probably means you typed something wrong, so you should check that you used the same name when creating the function with `def hi():` and when calling it with `hi()`.
    - If you get an `IndentationError`, check that both of the `print` lines have the same whitespace at the start of a line: python wants all the code inside the function to be neatly aligned.
    - If there's no output at all, check that the last `hi()` *isn't* indented - if it is, that line will become part of the function too, and it will never get run.
    
    Let's build our first function with parameters. We will use the previous example – a function that says 'hi' to the person running it – with a name:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    def hi(name):
    ```
    
    As you can see, we now gave our function a parameter that we called `name`:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    def hi(name):
        if name == 'Ola':
            print('Hi Ola!')
        elif name == 'Sonja':
            print('Hi Sonja!')
        else:
            print('Hi anonymous!')
    
    hi()
    ```
    
    Remember: The `print` function is indented four spaces within the `if` statement. This is because the function runs when the condition is met. Let's see how it works now:
    
    {% filename %}{{ warning_icon }} command-line{% endfilename %}
    
        $ python3 python_intro.py
        Traceback (most recent call last):
        File "python_intro.py", line 10, in <module>
          hi()
        TypeError: hi() missing 1 required positional argument: 'name'
        
    
    Oops, an error. Luckily, Python gives us a pretty useful error message. It tells us that the function `hi()` (the one we defined) has one required argument (called `name`) and that we forgot to pass it when calling the function. Let's fix it at the bottom of the file:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    hi("Ola")
    ```
    
    And run it again:
    
    {% filename %}command-line{% endfilename %}
    
        $ python3 python_intro.py
        Hi Ola!
        
    
    And if we change the name?
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    hi("Sonja")
    ```
    
    And run it:
    
    {% filename %}command-line{% endfilename %}
    
        $ python3 python_intro.py
        Hi Sonja!
        
    
    Now, what do you think will happen if you write another name in there? (Not Ola or Sonja.) Give it a try and see if you're right. It should print out this:
    
    {% filename %}command-line{% endfilename %}
    
        Hi anonymous!
        
    
    This is awesome, right? This way you don't have to repeat yourself every time you want to change the name of the person the function is supposed to greet. And that's exactly why we need functions – you never want to repeat your code!
    
    Let's do something smarter – there are more names than two, and writing a condition for each would be hard, right?
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    def hi(name):
        print('Hi ' + name + '!')
    
    hi("Rachel")
    ```
    
    Let's call the code now:
    
    {% filename %}command-line{% endfilename %}
    
        $ python3 python_intro.py
        Hi Rachel!
        
    
    Congratulations! You just learned how to write functions! :)
    
    ## Loops
    
    > For readers at home: this part is covered in the [Python Basics: For Loop](https://www.youtube.com/watch?v=aEA6Rc86HF0) video.
    
    This is the last part already. That was quick, right? :)
    
    Programmers don't like to repeat themselves. Programming is all about automating things, so we don't want to greet every person by their name manually, right? That's where loops come in handy.
    
    Still remember lists? Let's do a list of girls:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    girls = ['Rachel', 'Monica', 'Phoebe', 'Ola', 'You']
    ```
    
    We want to greet all of them by their name. We have the `hi` function to do that, so let's use it in a loop:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    for name in girls:
    ```
    
    The `for` statement behaves similarly to the `if` statement; code below both of these need to be indented four spaces.
    
    Here is the full code that will be in the file:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    def hi(name):
        print('Hi ' + name + '!')
    
    girls = ['Rachel', 'Monica', 'Phoebe', 'Ola', 'You']
    for name in girls:
        hi(name)
        print('Next girl')
    ```
    
    And when we run it:
    
    {% filename %}command-line{% endfilename %}
    
        $ python3 python_intro.py
        Hi Rachel!
        Next girl
        Hi Monica!
        Next girl
        Hi Phoebe!
        Next girl
        Hi Ola!
        Next girl
        Hi You!
        Next girl
        
    
    As you can see, everything you put inside a `for` statement with an indent will be repeated for every element of the list `girls`.
    
    You can also use `for` on numbers using the `range` function:
    
    {% filename %}python_intro.py{% endfilename %}
    
    ```python
    for i in range(1, 6):
        print(i)
    ```
    
    Which would print:
    
    {% filename %}command-line{% endfilename %}
    
        1
        2
        3
        4
        5
        
    
    `range` is a function that creates a list of numbers following one after the other (these numbers are provided by you as parameters).
    
    Note that the second of these two numbers is not included in the list that is output by Python (meaning `range(1, 6)` counts from 1 to 5, but does not include the number 6). That is because "range" is half-open, and by that we mean it includes the first value, but not the last.
    
    ## 概要
    
    That's it. **You totally rock!** This was a tricky chapter, so you should feel proud of yourself. We're definitely proud of you for making it this far!
    
    For official and full python tutorial visit https://docs.python.org/3/tutorial/. This will give you a more thorough and complete study of the language. Cheers :)
    
    You might want to briefly do something else – stretch, walk around for a bit, rest your eyes – before going on to the next chapter. :)
    
    ![Cupcake](images/cupcake.png)