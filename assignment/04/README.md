# 4章【モデルとデータベースを用意しよう】

## 課題概要
 - 継続課題 : 1問
 - 確認問題 : 2問

---
## 継続課題
教科書を読み進める前に、以下の準備を行ないましょう。

1. ご自身のPC内のローカルリポジトリでの作業
   1. まず、ターミナル（WindowsはGit Bash)上でご自身のPC内のローカルリポジトリに移動して下さい。
   1. `git pull`をして下さい。
   1. `master`Branchに移動して下さい。
      1. `git checkout master`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`master`Branchであれば良い。
   1. `continuous_exercise_04`というBranchを作成して移動して下さい。
      1. `git checkout -b continuous_exercise_04`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`continuous_exercise_04`Branchであれば良い。

**ここまで行ったら教科書に戻り**、読み進みながら、適宜指示のある箇所に関しては、ファイルを編集していきましょう。

教科書を読み終えたら、以下を行ないましょう。
1. ご自身のPC内のローカルリポジトリでの作業
   1. 以下のコマンドを実行し、リモートリポジトリに反映します。
      1. `git add .`
      1. `git commit -m "何かしらのメッセージ"`
         1. 適切なコミットメッセージは学習済みであると思うので、お忘れの方はそちらを復習してみて下さい。
      1. `git push origin continuous_exercise_04`
1. リモートリポジトリ(GitHub)での作業
   1. `continuous_exercise_04`Branchに切り替える。
   1. `master`に向けてPull Requestを作成して下さい。

以上で、継続課題の提出は完了です。

---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。
### 問1
次のうち、間違っているものはどれですか。
```
a. モデルを作るコマンドは「rails g model モデル名」である。
b. データベースは、「テーブル」「カラム」「レコード」の3要素で構成されている。
c. マイグレーションファイルでデータベースへ反映するコマンドは「rails db:migrate」である。
d. データベースとはデータを保存しておくところであり、railsでデータベースとやり取りをするのはcontrollerである。
```

<details>
<summary>解答/解説</summary>
 
```
【解答】
d.データベースとはデータを保存しておくところであり、railsでデータベースとやりとりするところはcontrollerである。

【解説】
コントローラーはモデルとデータをやり取りすることが役割であってデータベースとやりとりすることはありません。

```
</details>


### 問2
次のうち、間違っているものはどれですか。
```
a. テーブルは表のことで、データベース内には複数のテーブル（表）を持つことができる。
b. カラムは、テーブルの列のことである。
c. レコードはテーブルの行のことである。1行に保存されているデータを1レコードと呼ぶ。
d. マイグレーションファイルは、モデルの新規作成、カラムやインデックスの追加といった変更を行えるファイルである。
```

<details>
<summary>解答/解説</summary>
 
```
【解答】
d.マイグレーションとはモデルの新規作成や、カラム・インデックスの追加といった変更を行なうことができる機能である。

【解説】
上の３つの選択肢はどれも正解である。
マイグレーションとはテーブルを新規に作成したりカラムの追加といった変更を行なう機能である。
新規で作成するのはモデルではなくテーブルである。

```
</details>
