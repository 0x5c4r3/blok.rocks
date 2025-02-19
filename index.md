---
title: /
layout: default
permalink: /
---
<style>
.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 100%;
}
</style>
<script>
  if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)){
  // MOBILE

document.write('<div style="white-space: pre; text-align: center;"><div class="center" style="color:red;display:inline;text-align: center;"> Nah G you browsing from a mobile??</div>\n<div class="center" style="color:red;display:inline;text-align: center;">Fuck that, grab a laptop...</div></div>\n')
  
}else{
  // DESKTOP

document.write('<p style="display: flex;">') //align-items: center;justify-content: center;">')

document.write('<span style="padding-right: 20px;">This is one line of text with image on the left side</span>')
document.write('<img src="https://raw.githubusercontent.com/0x5c4r3/scare.rocks/refs/heads/master/img/1.gif" alt="Human" style="width:30%;height:30%;">')

document.write('</p>')
}
</script>

