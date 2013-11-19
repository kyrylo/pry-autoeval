**This project is just a rough and raw idea. Currently, it's not possible to
  implement it.**

Pry Autoeval
============

* Repository: [https://github.com/kyrylo/pry-autoeval][pa]

Description
-----------

Pry Autoeval provides a way to evaluate expressions as you type them.

Installation
------------

All you need is to install the gem. The `pry-autoeval` plugin will be detected
and used automatically.

    gem install pry-theme

Synopsis
--------

Let's see what you can do with Pry Autoeval.

```
[1] pry(main)> 1 + 1 #=> 2
[2] pry(main)> ['pry'] + [''] #=> ["pry", ""]
[2] pry(main)> ['pry'] + ['autoeval'] #=> ["pry", "autoeval"]
```

```
[1] pry(main)> 1 + 1
#=> 2
[2] pry(main)> []
```


### Configuration

Pry Autoeval can be configured via `~/.pryrc` file.

```
# The default configuration.
Pry.config.autoeval = {
  # Options:
  #   :compact
  #   :greedy
  :style => :compact,

  # Options:
  #   :same_line
  #   :beneath
  :position => :same_line,

  # Options:
  #   0.1-1.0
  :delay => 0.5
}
```

### Why would I want to use Pry Autoeval?

OK, now that you've seen the features, you may be wondering why this plugin even
exists. First of all, if you test some dirty code in Pry (say, a regular
expression or a complex one-liner), you often press <Return> key in order to
evaluate an expression and see its the result. However, if the result is
unpleasant, you press <Up>, make changes to the code, then press <Enter> and get
the new result. And this continues on and on, and on, and on, until you finally
figure out that doing this sucks monkey balls^W^W^W^W^W^W^W^W pleased
with the final result. You pollute your history with unwanted entries
and waste your screen space. Secondly, you constantly perform repetitive job.
With Pry Autoeval there is no need to press <Enter>+<Up>, because expressions
evaluate on the fly. You are a human, not a robot. You create beautiful things,
while your computer assists you. Not vice versa. Thirdly… hey, isn't that enough
for you already? You've been told. Now, install the gem and enjoy Pry.

Limitations
-----------

* MRI 1.9.3

Licence
-------

The project uses Zlib Licence. See LICENCE file for more information.

[pa]: https://github.com/kyrylo/pry-autoeval "Home page"
