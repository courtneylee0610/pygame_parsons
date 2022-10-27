---
layout: default
title: Move the bullet
---

Create a program that checks if the bullet for tank1 is active. If it is:
1. Move the bullet along the x axis at the correct speed (velocity)
2. Move the bullet along the y axis at the correct speed (velocity)

<div id="MoveBullet-sortableTrash" class="sortable-code"></div> 
<div id="MoveBullet-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="MoveBullet-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="MoveBullet-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "if tank1_bullet.isActive:\n" +
    "	tank1_bullet.x += tank1_bullet.dx\n" +
    "	tank1_bullet.y += tank1_bullet.dy\n" +
    "tank1_bullet.x += tank1_bullet.x #distractor\n" +
    "tank1_bullet.y += tank1_bullet.y #distractor\n" +
    "tank1_bullet.dx += tank1_bullet.x #distractor\n" +
    "tank1_bullet.dy += tank1_bullet.y #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "MoveBullet-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "MoveBullet-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#MoveBullet-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#MoveBullet-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
[Previous](./example1.html)
