# <center>PitchNet: Pitch Controllable Singing Voice Conversion Network with Non-parallel Data</center>

<center>Chengqi Deng, Chengzhu Yu</center><br>
<center>Zhejiang University, Tencent AI Lab</center>

<br>



## Abstract

<div style="text-align: justify"> Singing voice conversion is to convert one's singing voice to match another one's timbre without modifying the content. Recent work shows that it's feasible to employ an autoencoder network training with non-parallel data to convert one's songs to a specified singer. However, the converted singing voice can be easily off-key, showing that it can't catch the pitch information precisely. In this paper, we propose PitchNet, a novel unsupervised singing voice conversion method based on the autoencoder architecture. We extract pitch information additionally and inject it into the decoder network while a pitch regression network is employed to force the encoder to split pitch information out of the latent space of the autoencoder. Experiments show that our method can greatly improve the quality of the converted singing voice and enable us to control the pitch. </div>

<br>

## The Architecture of Our Model

<table border="0">
  <tbody>
    <tr>
      <td><img src="imgs/model.png" alt="Overall Architecture"></td>
      <td><img src="imgs/submodels-cut.png" alt="Sub-models Architecture"></td>
    </tr>
  </tbody>
</table>

<br>

## Examples

---


Singing voice of VKOW: 

<audio controls="" preload="auto">
            <source src="wavs/Origin/VKOW-11.wav"></audio>

<table align="center">
  <thead>
    <tr>
      <th>Target</th>
      <!-- th>Original voice</th-->
      <th><a href="https://arxiv.org/abs/1904.06590">Nachmani et al.</a></th>
      <th>Ours</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>JLEE</td>
      <!--td><audio controls="" preload="auto">
            <source src="wavs/Origin/JLEE-08.wav"></audio></td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/VKOW-11-JLEE.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/VKOW-11-JLEE.wav"></audio></td>
    </tr>
    <tr>
      <td>JTAN</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/VKOW-11-JTAN.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/VKOW-11-JTAN.wav"></audio></td>
    </tr>
    <tr>
      <td>KENN</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/VKOW-11-KENN.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/VKOW-11-KENN.wav"></audio></td>
    </tr>
    <tr>
      <td>SAMF</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/VKOW-11-SAMF.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/VKOW-11-SAMF.wav"></audio></td>
    </tr>
    <tr>
      <td>ZHIY</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/VKOW-11-ZHIY.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/VKOW-11-ZHIY.wav"></audio></td>
    </tr>
  </tbody>
</table>
----

Singing voice of JLEE: 

<audio controls="" preload="auto">
            <source src="wavs/Origin/JLEE-08.wav"></audio>

<table>
  <thead>
    <tr>
      <th>Target</th>
      <!-- th>Original voice</th-->
      <th><a href="https://arxiv.org/abs/1904.06590">Nachmani et al.</a></th>
      <th>Ours</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>VKOW</td>
      <!--td><audio controls="" preload="auto">
            <source src="wavs/Origin/JLEE-08.wav"></audio></td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/JLEE-08-VKOW.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/JLEE-08-VKOW.wav"></audio></td>
    </tr>
    <tr>
      <td>JTAN</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/JLEE-08-JTAN.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/JLEE-08-JTAN.wav"></audio></td>
    </tr>
    <tr>
      <td>KENN</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/JLEE-08-KENN.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/JLEE-08-KENN.wav"></audio></td>
    </tr>
    <tr>
      <td>SAMF</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/JLEE-08-SAMF.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/JLEE-08-SAMF.wav"></audio></td>
    </tr>
    <tr>
      <td>ZHIY</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/JLEE-08-ZHIY.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/JLEE-08-ZHIY.wav"></audio></td>
    </tr>
  </tbody>
</table>
---

Singing voice of JTAN:

<audio controls="" preload="auto">
            <source src="wavs/Origin/JTAN-16.wav"></audio>

<table>
  <thead>
    <tr>
      <th>Target</th>
      <!-- th>Original voice</th-->
      <th>Nachmani et al.</th>
      <th>Ours</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>JLEE</td>
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/JTAN-16-JLEE.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/JTAN-16-JLEE.wav"></audio></td>
    </tr>
    <tr>
      <td>VKOW</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/JTAN-16-VKOW.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/JTAN-16-VKOW.wav"></audio></td>
    </tr>
    <tr>
      <td>KENN</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/JTAN-16-KENN.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/JTAN-16-KENN.wav"></audio></td>
    </tr>
    <tr>
      <td>SAMF</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/JTAN-16-SAMF.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/JTAN-16-SAMF.wav"></audio></td>
    </tr>
    <tr>
      <td>ZHIY</td>
      <!--td> </td-->
      <td><audio controls="" preload="auto">
            <source src="wavs/USVC/JTAN-16-ZHIY.wav"></audio></td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Ours/JTAN-16-ZHIY.wav"></audio></td>
    </tr>
  </tbody>
</table>

<br>

**Converted results of different pitch as input**

\* *Convert from VKOW to JLEE*

Source:  
<audio controls="" preload="auto">
            <source src="wavs/Origin/VKOW-11.wav"></audio>

<table>
  <thead>
    <tr>
      <th>Input Pitch</th>
      <th>Output</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>pitch x 1.0</td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Pitch/VKOW-11-JLEE-1.0.wav"></audio></td>
    </tr>
    <tr>
      <td>pitch x 0.7</td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Pitch/VKOW-11-JLEE-0.7.wav"></audio></td>
    </tr>
    <tr>
      <td>pitch x 1.2</td>
      <td><audio controls="" preload="auto">
            <source src="wavs/Pitch/VKOW-11-JLEE-1.2.wav"></audio></td>
    </tr>
  </tbody>
</table>