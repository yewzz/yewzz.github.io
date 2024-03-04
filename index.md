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
            var table = document.getElementById("mytab");
            var td1=table.getElementsByTagName("tr").item(1).getElementsByTagName("td").item(0)

            code1 = 'print("hello world1")'
            code2 =  'print("hello world2")'
            defined_content = '<pre>' + code1 + '\n' + code2 + '</pre>'
            td1.innerHTML = defined_content
        }

        function myFunction2() {
            var table = document.getElementById("mytab");
            var td1=table.getElementsByTagName("tr").item(1).getElementsByTagName("td").item(1)

            code1 = 'print("hello world3")'
            code2 =  'print("hello world4")'
            defined_content = '<pre>' + code1 + '\n' + code2 + '</pre>'
            td1.innerHTML = defined_content
        }
        
        function progress() {
            var bar = document.querySelector('.progress');
            var width = 0;
            var id = setInterval(frame, 10);
            function frame() {
                if (width >= 50) {
                   
                    myFunction();
                } 
                else if (width >= 100) {
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


**模型演示:**<br> 
<form  method="get">
  <p>输入: <input type="text" name="fname" style="width: 550px;height:200px" /> <button type="button" onclick='progress()'>运行</button></p>
  <!-- <input type="submit" value="Submit" /> -->
</form>


<div class="progress-bar">
  <div class="progress"></div>
</div>

<div>
    <table style='width: 100%;' id='mytab'>
        <thead>
        <tr>
            <th>模型输出-1</th>
            <th>模型输出-2</th>
            <th>实际答案</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td width="400px" height="400px"></td>
            <td width="400px" height="400px"></td>
            <td width="400px" height="400px"></td>

        </tr>
    </tbody>
    </table>
</div>

