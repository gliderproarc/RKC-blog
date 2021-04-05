+++
title = "Hylang"
author = ["Robert Clay"]
date = 2021-03-14
lastmod = 2021-04-05T11:37:11+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-03-21 Sun]</span></span>,#python


## Have you ever heard of Hy? {#have-you-ever-heard-of-hy}

Those of you who have tried a lisp, and gotten used to having things like
multiple arguments for things like addition have probably wondered how you can
write more lisp and less things that aren't lisp. Well as I started poking
around the internet for Lisps that would get me close to Clojure without needing
to deal with the JVM all the time, I came acres this language called Hy.


## Lisp syntax for Python {#lisp-syntax-for-python}

[Hylang](<https://docs.hylang.org/en/stable/>) is mostly just Python, but with a
lisp syntax. It borrows bits and pieces from Clojure's flavor of lisp, and it's
nice to see things like a Loop/recur macro for propper tail-call recursion
despite the fact you are still running on Python. Hy can be installed as a
python package to an existing Python run-time, and it affords some really nice
inter-op with Python.

Just yesterday, I decided to do a little practice and re-implemented a lowest
common denominator function I had written in Python before:

<a id="code-snippet--Hy-euc-lcd-tailcall"></a>
```hy
(require [hy.contrib.loop [loop]])
(defn greatest-common-demoninator [num1 num2] "Algorithm practice. Euclidean greatest common denominator."
    (if (> num2 num1) "The first number must be greater"
        (loop [[n1 num1] [n2 num2]]
          (if (= 0 n2) n1
              (recur n2 (% n1 n2))))))

(print (greatest-common-demoninator 259 37))
```

That is what I ended up with in Hy, vesus a similar implementation in valilla
python

<a id="code-snippet--Euclidean-GCD-Python"></a>
```python
def euclidean_GDC(num1, num2):
    """Euclidean greatest common denominator."""
    if num2 > num1:
        return "The first number must be greater"
    elif num2 == 0:
        return num1
    else:
        return euclidean_GDC(num2, (num1 % num2))


print(euclidean_GDC(270, 195))
```

They don't look that different, and to be fair the Python version is not that
great considering it's recursive without any provision for what happens if you
blow the stack. In a case like this, Hy doesn't provide very much that is
different than vanilla python. It starts to become more apparent when you start
to do more "lispy" things in your code.


## So why use Hy at all? {#so-why-use-hy-at-all}

Well for, I don't write applications. I just write scripts. I need to call out
to Python libraries to do stuff like parse CSV files or print out JSON into a
format I can work within Org-mode. If I don't need to work about a team of
people being able to read my code, Hy makes a lot of sense. I can even call
straight python with in-line if I really need to. Maybe one day I will write
production Python, and if that day comes I won't be able to get away with a
Lowest-common denominator function like the one I have above.

The way I see it, If I had a choice: use vanilla python, put up with some
roughness and use Hy; I would rather use Hy. I don't do a whole lot with code.
But the code I write I would love to be in the idiom that fits how I think the
best. I quite like vanilla Python. But when I thought of how to make a function
that calculates the lowest common denominator, this fairly function and
recursive solution felt right.
