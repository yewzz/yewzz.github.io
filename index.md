# <center>论文名/模型名</center>

## 摘要/功能介绍

 absxacsa

<img align="center" src="resources/pipeline.png" style="  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 80%;" />

<!-- <img align="center" src="resources/model.png" style="  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 80%;" /> -->

<script type="text/javascript">
        function myFunction() {
            // 这里写入要执行的代码逻辑
            // alert("Hello World!");
            var table = document.getElementById("mytab");
            var td1=table.getElementsByTagName("tr").item(1).getElementsByTagName("td").item(1)
            td1.innerHTML = '运行的结果'
        }
</script>





**Introduction:**<br> 
<li><form action="http://www.jb51.net/example/html/form_action.asp" method="get">
  <p>输入: <input type="text" name="fname" /></p>
  <!-- <input type="submit" value="Submit" /> -->
</form>
<button type="button" onclick='myFunction()'>运行</button></li>
<!-- <li>In the third section (<strong>More Samples</strong>), we provide more samples of different aspects (e.g., comparisons of different editing positions).</li>
<li>Our research is based on the open-source dataset OpenSinger, and all experiments conducted in the paper have been authorized by the publisher. This project is currently only used for research, and aims to make contributions and provides some ideas for the community. Please do not used for commercial purposes.</li> -->
<!-- ## 1 Audio Samples
*Notes:* <br>
<li>GT denotes the original audio(the input audio to be edited).</li>
<li>The <font color="red">red</font> part represents the editing region.</li>
<li>Words —— Phonemes</li>
#### Exp. 1:

original lyrics: 朋友爱得那么苦痛 —— <BOS> p eng | y ou # ai | d e # n a | m e # k u | t ong <EOS> <br>
insertion: 朋友<font color="red">如果</font>爱的那么苦痛 —— <BOS> p eng | y ou # <font color="red">r u | g uo #</font> ai # d e # n a | m e # k u | t ong <EOS> <br>
replacement: 朋友爱的那么<font color="red">认真(<strike>苦痛</strike>)</font> —— <BOS> p eng | y ou # ai # d e # n a | m e # <font color="red">r en | zh en (<strike> k u | t ong</strike>) </font> <EOS> <br>
deletion: 朋友爱的<font color="red">(<strike>那么</strike>)</font>苦痛 —— <BOS> p eng | y ou # ai # d e # <font color="red"> (<strike> n a | m e #</strike>) </font>k u | t ong <EOS> <br> -->
<div>
    <table style='width: 100%;' id='mytab'>
        <thead>
        <tr>
            <th>GT</th>
            <th>GT(Mel+PWG)</th>
            <th>EditSinger(insertion)</th>
            <th>EditSinger(replacement)</th>
            <th>EditSinger(deletion)</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT/0000000001.mp3" type="audio/mp3"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/GT(mel+pwg)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(insertion)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(replacement)/0000000001.wav" type="audio/wav"></audio></td>
            <td><audio style="width: 150px;" controls="" ><source src="resources/MOS1/editsinger(deletion)/0000000001.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    </table>
</div>

