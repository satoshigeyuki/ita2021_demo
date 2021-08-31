# 「アルゴリズム入門」(2021A) の課題作成デモ

## 準備

1. このレポジトリをcloneする．

2. [plags_scripts](https://github.com/satoshigeyuki/plags_scripts)レポジトリをcloneする．

3. `pip install astunparse`（`plags_scripts/template_autograde.py`を使う場合）

## as-is課題の作成

1. `exercises/empty_as_is.ipynb` を適当にコピー（例えば `exercises/demo1.ipynb`）

2. 最初の見出しにタイトルを記述し，解答欄を明示する．

3. `release_as_is.py` を実行する．

```sh
python3 plags_scripts/release_as_is.py -s exercises/demo1.ipynb
```

4. `demo1.ipynb` をPLAGS UTに登録する．

5. `form_demo1.ipynb` をGoogle Driveにアップロードする．ファイル名は変えてよい．

6. `form_demo1.ipynb` のURLをPLAGS UTに登録する．

## autograde課題の作成

1. `exercises/empty_autograde.ipynb` を適当にコピー（例えば `exercises/demo2.ipynb`）

2. `demo2.ipynb`において，DESCRIPTION，ANSWER_CELL_CONTENT，EXAMPLE_ANSWERS，INSTRUCTIVE_TESTを埋める．

3. `template_autograde.py` を実行する．

```sh
python3 plags_scripts/template_autograde.py -s exercises/demo2.ipynb
```

4. `cp template_demo2.ipynb demo2.ipynb`

5. `judge_util.py` をインストールする．

```sh
python3 plags_scripts/template_autograde.py -lp -s exercises/demo2.ipynb
```

6. `demo2.ipynb` の hidden モジュールにおいて，テストメソッドを追加する．

7. `build_autograde.py` を実行する．

```sh
python3 plags_scripts/template_autograde.py -c judge_env.json -lp -s exercises/demo2.ipynb
```

8. `autograde.zip` をPLAGS UTに登録する．

9. `form_demo2.ipynb` をGoogle Driveにアップロードする．ファイル名は変えてよい．

10. `form_demo2.ipynb` のURLをPLAGS UTに登録する．

