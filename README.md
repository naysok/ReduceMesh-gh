# ReduceMesh-via-ghPython  

grasshopper を経由することで、入出力をインタラクティブにできる。  
ReduceMesh で削減して気に入らなくて、 Undo でいちいち戻すのを避けれる（はず）。  

ghPython のコードは冗長に見えるが、フォーラムによると、Rhino の SDK の仕様的に、 Rhino.Doc を噛ませる必要とか書いてあるのでたぶんそういうもの。速度を比べてもそんなに遅くないのでまあ。  

---  


### 使い方  

Toggle を False に。  

target mesh を右クリック。Set mesh を選んで、Rhino上の meshを選択。   

スライダーで削減したい割合を指定。  

Toggle を True にすると削減が始まる。  

良ければ、 Bake  

---  

参考にしたのはこれ→
（[http://www.grasshopper3d.com/forum/topics/how-do-i-reduce-mesh-via-python](http://www.grasshopper3d.com/forum/topics/how-do-i-reduce-mesh-via-python)）  

このままだと、ghPython コンポーネントが常時走り出して、かなり不便なので、BoolToggle を付けた。  

卒制のときにここのサンプル落としてきて使おうとしたときに、そのとき作ってた Mesh が重い + Toggle を自分で付けることを思いつかなくて、ただの自動フリーズスクリプトみたいになってたので改良。（180312）  


---  

僕の手元の実行環境は、  
- windows7 (bootcamp)  
- Rhinoceros5 (Win)  
- Grasshopper (0.9.0076)  
- ghPython (0.6.0.3)  

ghPython はここから→([http://www.food4rhino.com/app/ghpython](http://www.food4rhino.com/app/ghpython))  
