j3.js (jThree非公式フォーク板)
---

![2015-09-30 19 43 39](https://cloud.githubusercontent.com/assets/1548478/10191016/92e2d934-67ab-11e5-8dfa-c09641cf1648.png)

# インストール
```bash
bower install 59naga/j3 --save

open http://localhost:8000/index.html
python -m SimpleHTTPServer 
# Serving HTTP on 0.0.0.0 port 8000 ...
```

`index.html`

```html
<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<script src="bower_components/jquery/dist/jquery.js"></script>
<script src="bower_components/j3/lib/jThree.js"></script>
<script src="bower_components/j3/lib/jThree.Stats.js"></script>
<script src="bower_components/j3/lib/jThree.MMD.js"></script>
<!-- <script src="bower_components/j3/lib/jThree.Trackball.js"></script> -->

<style>
  body{
    background-color:grey;
    /* requiment */
    position:fixed;
    width:100%;
    height:100%;
    margin:0;
  }
</style>
<script>
  jThree(function(j3){
    j3.Stats();
    // j3.Trackball();
  });
</script>

<script type="text/goml">
  <goml>
    <head>
      <rdr frame="body" camera="camera:first" param="antialias: true; clearAlpha:0;" />
    </head>
    <body>
      <scene>

        <camera style="cameraFar: 10000; position: 2 18 30; lookAtY: 10;">
            <light type="Dir" style="position: 1 3 5;" />
        </camera>
        <light type="Amb" style="lightColor: #555;" />
        <mmd model="bower_components/j3/example/miku/index.pmx" motion="bower_components/j3/example/miku/im5066365.vmd" onLoad="parent.jThree.MMD.play( true );"/>
        
      </scene>
    </body>
  </goml>
</script>

</head>
</html>
```

## 使用ポーズ
* [万国博覧会オーストリア館ポスター - ミュシャ再現ポーズ](http://seiga.nicovideo.jp/seiga/im5066365) 作者：闇雨(yamisame) 

> 
禁止事項
---
* 誹謗中傷の目的での使用
* 公序良俗に反する使用
* 関係者に迷惑のかかる使用
* 商用利用

>
免責
---
* 本データの使用による損害に対して当方は一切責任を負いません。自己責任でご使用ください


# 参考
* [有志サイト - jThree備忘録](http://seesaawiki.jp/j3wiki/d/%CD%AD%BB%D6%A5%B5%A5%A4%A5%C8)
* [スクリプト0行で驚くほど描けるWebGL](http://qiita.com/m_mitsuhide/items/827f35dd24d145a2738e)

License
---
MIT
