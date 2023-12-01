# html-scss-training

## 作業進捗
### NodeJSインストール
- nodenvからinstall
- v21.2.0にした
- あとで14.15.0にした
### scssのビルド
- yarnコマンド叩いた
## 自分用メモ
### yarnとは
- node.jsのパッケージマネージャの1つ
    - npmとyarnがある

### リファクタリング
- HTML,SCSS編集した
- `yarn run build`実行してmain.css作成した
- webページ確認
    - リストの色違う
    - menuの色と位置おかしい
    - 全体的にサイズずれてる

### BEM記法とは
- 参考:https://www.youtube.com/watch?v=QCJ1THnyAec
- Block,Element,Modifierの頭文字
- HTML,CSSのクラス名の命名規則
- block,elementは親子関係のようなもの
- `"block名"__"element名"--"modifier名"`とつける
    - modifierは任意
- 以下、例
    - クラスheroに子body,logo,buttonがあるとすると以下のようにつける
        - `hero__body`
        - `hero__logo`
        - `hero_button`
    - ここで、ボタンに対して色をピンクにして他は全て同じようなクラスを作るときにmodifierを使う
        - `hero__button--pink`
    - CSSでは以下のように記述する
```SCSS
.hero{
    display: flex;
    &__logo{

    }
    &__body{

    }
    &__button{
        padding: 0 16px;
        display: inline-block;
        background: #000;
        coloer: white;
        line-height: 40px;
        border-radius: 20px;
        &--pink{
            background: pink;
        }
    }
}
```