sphinx-rst2pdf-plantuml-japanese-example
========================================

An example to create PDF files containing Japanese with Sphinx, rst2pdf and PlantUML.

## Setup for OSX

### Install VLGothic font

Download [VLGothic-20130607.tar.bz2](https://sourceforge.jp/projects/vlgothic/downloads/58961/VLGothic-20130607.tar.bz2)
from [VL Gothic Font Family](http://vlgothic.dicey.org/download.html)

Extract and put files to ~/Library/Fonts

### Install Python

I use anyenv to install Python.

```
git clone https://github.com/riywo/anyenv ~/.anyenv
cat <<'EOF' >> ~/.bash_profile

# anyenv
export PATH="$HOME/.anyenv/bin:$PATH"
eval "$(anyenv init -)"
EOF
exec $SHELL -l
```

### Install plantuml

```
brew install plantuml
```


### Set up this example

```
git clone https://github.com/hnakamur/sphinx-rst2pdf-plantuml-japanese-example
cd sphinx-rst2pdf-plantuml-japanese-example
virtualenv env
source env/bin/activate
pip install -r pip_requirements.txt
```

### Modify conf.py appropriately

project = u'sphinx rst2pdf example'
copyright = u'2014, Hiroaki Nakamura'

plantuml = ['java', '-jar', '/usr/local/Cellar/plantuml/7994/plantuml.7994.jar']


## Build the pdf file.

```
make pdf
```

## Open the created pdf file

```
open _build/pdf/MyProject.pdf
```

## Thanks to

* [rst2pdf拡張を使ったPDFファイル作成 — Python製ドキュメンテーションビルダー、Sphinxの日本ユーザ会](http://sphinx-users.jp/cookbook/pdf/rst2pdf.html)
* [(6日目) Sphinx 拡張の紹介 - Hack like a rolling stone](http://tk0miya.hatenablog.com/entry/20111206/p1)
* [p.26](http://www.slideshare.net/TakeshiKomiya/sphinx-2013/26) in [Sphinx ではじめるドキュメント生活 2013 #sphinxconjp](http://www.slideshare.net/TakeshiKomiya/sphinx-2013)
