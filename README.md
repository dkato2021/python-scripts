## search-contamination
**CheckMによってcontaminationと判定された遺伝子が含まれるcontigを探索するためのスクリプト**
![](./tmp/A_3.png)
## search annotation file
**アノテーションファイルから、指定するキーワードを含む行を抽出しします。**

## Usage
```
$ extraction.py [-h] -a ANNOTATION -c COL_NAME [-k KEYWARDS]
```

## optional arguments
```
  -h, --help            show this help message and exit
  -a ANNOTATION         specify the path to your annotation file(ex. ~.xlsx) which number of sheet is 1
  -c COL_NAME           specify the column name you want to search
  -k [KEYWARDS [KEYWARDS ...]]
                        specify the keywords(default:transport facilitator permease antiporter symporter
```
## Accession-number-to-Organism-name
[Batch Entrez](https://www.ncbi.nlm.nih.gov/sites/batchentrez)でダウンロードしたファイル名をAccession numberからOrganism-nameへ一括変更するスクリプト

## Usage
```
$ python3 Accession-number-to-Organism-name.py -in DIR_IN -stats STATS_DIR -ex EXTENSION
```
## optional arguments:
```
  -h, --help        show this help message and exit
  -in DIR_IN        The directory containing the files you want to rename
  -stats STATS_DIR  The directory containing the assembly statistcs reports
  -ex EXTENSION     extension of output file(ex. fna.gz)
```

## tips
- 先頭の'RS_'と'GB_'は削除しないとBatch Entrezは入力として受け付けない。
```
#GTDBに登録されている全細菌のAccession-number一覧の取得。
$ wget https://data.ace.uq.edu.au/public/gtdb/data/releases/release202/202.0/bac120_taxonomy_r202.tsv
```
## edit_features.tsv_from_DFAST
**DFASTが出力するfeatures.tsvファイルのCDS領域の開始点と終了点の表記を下流の解析で扱いやすい表記に変更します**

## Usuge
```
$ python edit_features.py -f features.tsv
```
- new_features.csvが出力されます。
## split_fasta
**multi-fastaファイルを分割します。**

## Usuge
```
$ python split_fasta.py -f multi-fasta.fasta
```
## get basic information of FASTA
**fastaファイルの基礎情報を出力するスクリプト**
## installation
```
$ pip install -r requirements.txt #condaでのinstallも可
```
## Usage
```
$ python basic.py -f fasta_file
```

