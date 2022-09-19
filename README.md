## deterministic_float
 * Cross-platform deterministic float point, fast soft float point.
 * Fast soft float point for deterministic computing, That
you can make **deterministic plugin** by use GFloat to replace float-point. like：
    * Physics Engine (Bullet、PhysX)
    * AI PathFinding (recast navigation)
    * AI Engine
 * Compare the overall performance of float754 and GFloat numbers, They differ by no more than **100%**
    * Is the fastest soft floating point in the world?
## IEEE-754 & My GFloat
* IEEE-754 float
  <table  >
    <tr>
        <th align="center" >sign</th>
        <th align="center" colspan = "5" width="400">exponents（8 bits）</th>
        <th align="center" colspan = "5" width="400">fractions（23 bits）</th>
    </tr>
    <tr>
        <td >31</td>
        <td >30</td><td>29</td><td>...</td><td>24</td><td>23</td>
        <td >22</td><td>21</td><td>...</td><td>1</td><td>0</td>
    </tr>
    </table>
* My GFloat
  <table  >
    <tr>
        <th align="center" >sign</th>
        <th align="center" colspan = "5" width="400">fractions（23 bits）</th>
        <th align="center" colspan = "5" width="400">exponents（8 bits）</th>
    </tr>
    <tr>
        <td >31</td>
        <td >30</td><td>29</td><td>...</td><td>9</td><td>8</td>
        <td >7</td><td>6</td><td>...</td><td>1</td><td>0</td>
    </tr>
    </table>
## Performance float vs GFloat
 * Some main function compare，more information view TestAndBenchMark 
 * Call every function 1000000 Times, get the float vs GFloat time

|Function|Win64 5950X|Win64 12900H | iOS A15 | MacOS M1 Pro | Android |
|:--|:--:|:--: |:--:|:--:|:--:|
|add|1.47 - 4.3 (ms)| | 1.36 - 2.14  (ms)|
|Mul|1.58 - 2.0 (ms)| 1.25 - 1.54 (ms)| 1.42 - 1.38  (ms) |
|Sin|12.08 - 15.25 (ms)|10.57 - 7.68 (ms)| 2.84 - 6.65  (ms)|
|Sqrt|1.54 - 11.46 (ms)|1.03 - 7.73 (ms) |1.14 - 7.75  (ms) |
|Exp| | |7.24 - 19.70  (ms)|
	
	
## How to start
 * Four OS platform projects for fast and easy to start test&benchmark

|Target Platform| Compiler| Project |
|:--|:--|:--|
|Win|Visual Studio 2022| deterministic/deterministic_float.sln|
|MacOS|XCode| deterministic/deterministic_float.xcodeproj |
|iOS|XCode| deterministic/deterministic_float_ios.xcodeproj |
|Android||todo|

## Current Support Platform For Test&Benchmark 
|Operation System|Win64|MacOS| iOS| Android|
|--|--|--|--|--|
|Now| $\checkmark$  |$\checkmark$|$\checkmark$| todo |





