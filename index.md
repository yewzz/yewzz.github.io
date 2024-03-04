# <center>论文名/模型名</center>

## 摘要/功能介绍

 absxacsa

<img align="center" src="resources/pipeline.png" style="  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 80%;" />


<script type="text/javascript">
        function myFunction() {
            // 这里写入要执行的代码逻辑
            // alert("Hello World!");
            var table = document.getElementById("mytab1");
            var td1=table.getElementsByTagName("tr").item(1).getElementsByTagName("td").item(0)

            code1 = 'print("hello world1")'
            code2 =  'print("hello world2")'
            defined_content = '<pre>' + code1 + '\n' + code2 + '</pre>'
            td1.innerHTML = defined_content
        }

        function myFunction2() {
            var table = document.getElementById("mytab2");
            var td1=table.getElementsByTagName("tr").item(1).getElementsByTagName("td").item(0)

            code1 = '&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot; ?&gt;&lt;root&gt;&lt;element attribute=&quot;value&quot;&gt;Content&lt;/element&gt;&lt;/root&gt;'

            code2 = '&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot; ?&gt;&lt;root&gt;&lt;element attribute=&quot;value&quot;&gt;Content&lt;/element&gt;&lt;/root&gt;'
            
            defined_content = '<pre><code>' + code1 + '\n' + code2 + '</pre></code>'
            td1.innerHTML = defined_content
        }
        
        function progress() {
            var bar = document.getElementById("progress1");
            var width = 0;
            var id = setInterval(frame, 10);
            function frame() {
                if (width >= 100) {
                    clearInterval(id);
                    myFunction();
                }
                else {
                    width++;
                    bar.style.width = width + '%';
                }
            }
        }

        function progress2() {
            var bar = document.getElementById("progress2");
            var width = 0;
            var id = setInterval(frame, 10);
            function frame() {
                if (width >= 100) {
                    clearInterval(id);
                    myFunction2();
                }
                else {
                    width++;
                    bar.style.width = width + '%';
                }
            }
        }
        
  
</script>


## 模型演示 
<form  method="get">
  <p><input type="text" name="fname" value="请输入..." style="width: 600px;height:200px; margin-left:100px" />   <button style="width:200px; height:200px; border: none; border-radius: 10px; font-family: sans-serif;" type="button" onclick='progress()' >1. 运行</button></p>
 
  <!-- <input type="submit" value="Submit" /> -->
</form>


<div class="progress-bar" style="margin-top:10px; margin-bottom:20px; margin-left:100px">
  <div class="progress" id="progress1"></div>
</div>

<div style="margin-left:100px">
    <table style='width: 100%;' id='mytab1'>
        <thead>
        <tr>
            <th width="800px">模型输出-1 </th>
            <!-- <th width="400px">模型输出-2</th>
            <th width="400px">实际答案</th> -->
        </tr>
        </thead>
        <tbody>
        <tr>
            <td width="800px" height="400px"></td>
            <!-- <td width="400px" height="400px"></td>
            <td width="400px" height="400px"></td> -->

        </tr>
    </tbody>
    </table>
</div>



 <button style="width:800px; height:50px; border: none; border-radius: 10px; font-family: sans-serif;margin-left:100px" type="button" onclick='progress2()' >2. 转化</button>

 <div class="progress-bar" style="margin-top:10px; margin-bottom:20px; margin-left:100px">
  <div class="progress" id="progress2"></div>
</div>

<div style="margin-left:100px;margin-bottom:100px">
    <table style='width: 100%;' id='mytab2'>
        <thead>
        <tr>
            <th width="800px">模型输出-2</th>
            <!-- <th width="400px">模型输出-2</th>
            <th width="400px">实际答案</th> -->
        </tr>
        </thead>
        <tbody>
        <tr>
            <td width="800px" height="400px"></td>
            <!-- <td width="400px" height="400px"></td>
            <td width="400px" height="400px"></td> -->

        </tr>
    </tbody>
    </table>
</div>

