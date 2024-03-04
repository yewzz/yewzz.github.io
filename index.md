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

            // XML数据（这里只作为示例）
            var xmlString = "<access-lists><access-list><name>BlockEntertainment</name><aces><ace><name>DenyEntertainmentSite1</name><matches><ipv4><destination-ip-address>220.181.38.148</destination-ip-address></ipv4></matches><actions><forwarding>drop</forwarding></actions></ace><!-- Add more ACEs for other entertainment sites --></aces></access-list></access-lists>";

            xmlString = "&lt;access-lists&gt;\n\t&lt;access-list&gt;\n\t\t&lt;name&gt;BlockEntertainment&lt;/name&gt;\n\t\t&lt;aces&gt;\n\t\t\t&lt;ace&gt;\n\t\t\t\t&lt;name&gt;DenyEntertainmentSite1&lt;/name&gt;\n\t\t\t\t&lt;matches&gt;\n\t\t\t\t\t&lt;ipv4&gt;\n\t\t\t\t\t\t&lt;destination-ip-address&gt;220.181.38.148&lt;/destination-ip-address&gt;\n\t\t\t\t\t&lt;/ipv4&gt;\n\t\t\t\t&lt;/matches&gt;\n\t\t\t\t&lt;actions&gt;\n\t\t\t\t\t&lt;forwarding&gt;drop&lt;/forwarding&gt;\n\t\t\t\t&lt;/actions&gt;\n\t\t\t&lt;/ace&gt;\n\t\t\t&lt;!-- Add more ACEs for other entertainment sites --&gt;\n\t\t&lt;/aces&gt;\n\t&lt;/access-list&gt;\n&lt;/access-lists&gt;";

            <!-- xmlString = "&lt;access-lists&gt;\n&lt;access-list&gt;\n&lt;name&gt;BlockEntertainment&lt;/name&gt;\n&lt;aces&gt;\n&lt;ace&gt;\n&lt;name&gt;DenyEntertainmentSite1&lt;/name&gt;\n&lt;matches&gt;\n&lt;ipv4&gt;\n&lt;destination-ip-address&gt;220.181.38.148&lt;/destination-ip-address&gt;\n&lt;/ipv4&gt;\n&lt;/matches&gt;\n&lt;actions&gt;\n&lt;forwarding&gt;drop&lt;/forwarding&gt;\n&lt;/actions&gt;\n&lt;/ace&gt;\n&lt;!-- Add more ACEs for other entertainment sites --&gt;\n&lt;/aces&gt;\n&lt;/access-list&gt;\n&lt;/access-lists&gt;"; -->
            
           
            
            defined_content = '<pre><code>' + xmlString + '</code></pre>'
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
            <td width="800px" height="400px" style="text-align:left"></td>
            <!-- <td width="400px" height="400px"></td>
            <td width="400px" height="400px"></td> -->

        </tr>
    </tbody>
    </table>
</div>

