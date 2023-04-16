# Spider

---

## What is it ?

Spider is a web fuzzer, fully writen in [Python](https://www.python.org/).

A web fuzzer is a [fuzzer](https://owasp.org/www-community/Fuzzing) implemented to find informations (such as vulnerable pages, credentials...) on a web server.

Spider only focus on web pages finding. To do so, and unlike other fuzzers, spider only aim to request known pages :

Instead of getting a wordlist and only trying these pages (like [ffuf](https://github.com/ffuf/ffuf) would do (this is a really good fuzzer you should definitly try out !)), Spider will get a small list of targets, and read the target pages to find other pages on the same server.

---

## Why using Spider ?

### Pros :

- Using that method, your scan will send less out-of-scope requests. It will be quieter, and faster.

### Cons :

- While you don't try a list of pages (you can, but it's not the goal of this tool), if a page is not "called" in any of the pages, you won't find it !

---

## Installation

To use Spider, you will need 2 packages :

    python3
    python3-pip

Install them using your default package manager (`apt-get`, `dnf`...)

Once you installed these, run

    python3 -m pip install -r requirements.txt

To install python packages.

Now, you are ready to run

    ./spider.py

To start the fuzzer !

---

## To do

- [ ] Make the basic app, that will fuzz a simple page (use )
- [ ] Add manual recursion limit
- [ ] Configure to take more arguments (like exclude some file types...)