# <center>EditSinger: Zero-Shot Text-Based Singing Voice Editing System with Diverse Prosody Modeling</center>

## Abstract

Zero-shot text-based singing voice editing enables users to edit the singing content by just performing text operations on the lyrics, while  without any additional data from the target singer. However, due to the different demands, challenges occur when applying existing speech editing methods to singing voice editing task, mainly including the lack of systematic consideration concerning prosody in insertion and deletion, as well as the trade-off between the naturalness of pronunciation and the preservation of prosody in replacement. In this paper we propose EditSinger, which is a novel singing voice editing model with specially designed diverse prosody modules to overcome the challenges above. Specifically, 1) a general masked variance adaptor is introduced for the comprehensive prosody modeling of the inserted lyrics and the transition of deletion boundary; and 2) we further design a fusion pitch predictor for replacement. By disentangling the reference pitch and fusing the predicted pronunciation, the edited pitch can be reconstructed, which could ensure a natural pronunciation while preserving the prosody of the original audio. In addition, to the best of our knowledge, it is the first zero-shot text-based singing voice editing system. Our experiments conducted on the OpenSinger prove that EditSinger can synthesize high-quality edited singing voices with natural prosody according to the corresponding operations.

<img align="center" src="resources/pipeline.png" style="  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 80%;" />

<img align="center" src="resources/model.png" style="  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 80%;" />

<script type="text/javascript">
        function myFunction() {
            // 这里写入要执行的代码逻辑
            // alert("Hello World!");
            var table = document.getElementById("mytab");
            var td1=table.getElementsByTagName("tr").item(1).getElementsByTagName("td").item(1)
            td1.innerHTML = '运行的结果'
        }
</script>

<form action="http://www.jb51.net/example/html/form_action.asp" method="get">
  <p>输入: <input type="text" name="fname" /></p>
  <!-- <input type="submit" value="Submit" /> -->
</form>
<button type="button" onclick='myFunction()'>运行</button>



**Introduction:**<br> 
<li>In the first two sections (<strong>Audio Samples & Method Analyses</strong>), there are some samples of common performance demonstration and comparison experiments.</li>
<li>In the third section (<strong>More Samples</strong>), we provide more samples of different aspects (e.g., comparisons of different editing positions).</li>
<li>Our research is based on the open-source dataset OpenSinger, and all experiments conducted in the paper have been authorized by the publisher. This project is currently only used for research, and aims to make contributions and provides some ideas for the community. Please do not used for commercial purposes.</li>
## 1 Audio Samples
*Notes:* <br>
<li>GT denotes the original audio(the input audio to be edited).</li>
<li>The <font color="red">red</font> part represents the editing region.</li>
<li>Words —— Phonemes</li>
#### Exp. 1:

original lyrics: 朋友爱得那么苦痛 —— <BOS> p eng | y ou # ai | d e # n a | m e # k u | t ong <EOS> <br>
insertion: 朋友<font color="red">如果</font>爱的那么苦痛 —— <BOS> p eng | y ou # <font color="red">r u | g uo #</font> ai # d e # n a | m e # k u | t ong <EOS> <br>
replacement: 朋友爱的那么<font color="red">认真(<strike>苦痛</strike>)</font> —— <BOS> p eng | y ou # ai # d e # n a | m e # <font color="red">r en | zh en (<strike> k u | t ong</strike>) </font> <EOS> <br>
deletion: 朋友爱的<font color="red">(<strike>那么</strike>)</font>苦痛 —— <BOS> p eng | y ou # ai # d e # <font color="red"> (<strike> n a | m e #</strike>) </font>k u | t ong <EOS> <br>
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

