# deterministic_float
fast soft float for deterministic computing
your can make deterministic physics engine、pathfind、AI by use my GFloat


  <table  >
    <tr>
        <th align="center" >符号位 S（1位）</th>
        <th align="center" colspan = "5" width="400">阶码部分（8位） E</th>
        <th align="center" colspan = "5" width="400">尾数部分（23位） M</th>
    </tr>
    <tr>
        <td >31</td>
        <td >30</td><td>29</td><td>...</td><td>24</td><td>23</td>
        <td >22</td><td>21</td><td>...</td><td>1</td><td>0</td>
    </tr>
    </table>


Call Function Test And BenchMark: 400000Times 
|Function| avg error|max error| time float vs GFloat | float / GFloat |
|--|--|--|--|--|
|Add|0.000071 %|5.882353 %|0.54 - 4.09  (ms) |0.13|
|Sub|0.000058 %|11.111112 %|0.53 - 4.34  (ms) |0.12|
|Mul|0.000011 %|0.000047 %|0.54 - 0.83  (ms) |0.65|
|Div|0.000011 %|0.000048 %|0.69 - 1.23  (ms) |0.56|
|Ceil|0.000008 %|0.040274 %|3.61 - 2.25  (ms) |1.60|
|Floor|0.000000 %|0.000000 %|3.63 - 0.65  (ms) |5.55|
|Whole|0.000004 %|0.000012 %|0.52 - 4.21  (ms) |0.12|
|Sin|146.627853 %|74631.750000 %|5.12 - 12.98  (ms) |0.39|
|Cos|146.200912 %|74857.898438 %|4.92 - 18.19  (ms) |0.27|
|Tan|237.590973 %|236063.468750 %|4.09 - 30.10  (ms) |0.14|
|ASin|1.791232 %|100.000000 %|5.37 - 4.33  (ms) |1.24|
|ACos|4.252209 %|10427.250977 %|5.66 - 9.98  (ms) |0.57|
|ATan|0.000445 %|10.218527 %|4.15 - 21.45  (ms) |0.19|
|ATan(10,x)|0.002552 %|10.290107 %|4.70 - 17.00  (ms) |0.28|
|ATan(x,10)|0.003720 %|10.312443 %|4.73 - 27.50  (ms) |0.17|
|Sqrt|0.063934 %|20.346285 %|0.58 - 12.14  (ms) |0.05|
|Exp|0.010087 %|0.061122 %|1.26 - 41.95  (ms) |0.03|
|Log|0.053551 %|12.293630 %|1.34 - 89.97  (ms) |0.01|
|Pow(2,x)|0.056123 %|0.141206 %|2.82 - 80.17  (ms) |0.04|
|Pow(x,2)|1.647707 %|19.761913 %|3.01 - 80.82  (ms) |0.04|


