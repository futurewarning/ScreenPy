# ScreenPy
Parse and annotate screenplays with markup language

| File     | info |
|--- | ---|
|screenpile | Main algorithms for compiling screenplay structure|
|screenpy | Parses shot headings with recursive descent |
|screenpy_vars | Defines valid shot heading element patterns |
|screenpy_tests | Extra tests in addition to screenpy |
|moviescript_crawler | crawls through imsdb_raw_nov_2015 folder |


Screenplay Structure
---

See the attached paper for more details (![Paper](https://github.com/drwiner/ScreenPy/blob/master/INT17_screenplays.pdf))


Setup
---
*  Install [poetry](https://python-poetry.org/docs/#installation)  
*  Activate the virtual enviroment
```
source $(poetry env info --path)/bin/activate
```
*  Install the required depencies
```
poetry install
```
* To use sense2vec model, fetch & unzip the pretrained vectors
```
wget https://github.com/explosion/sense2vec/releases/download/v1.0.0/s2v_reddit_2015_md.tar.gz
tar -xvf  s2v_reddit_2015_md.tar.gz
```
* Run the script with  
```
poetry run python <script_name>.py
```


Development
---
Working on verb sense disambiguation to classify clauses in stage direction with FrameNet frames using off-the-shelf frame-semantic parser [Semafor] (https://github.com/Noahs-ARK/semafor).
