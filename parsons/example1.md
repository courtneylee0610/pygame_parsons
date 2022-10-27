---
layout: default
title: Page 2 Example (Variable Check Grader)
---

Construct a program that checks to see if the bullet from tank1 has collided with the bullet from tank2. If it has:
1. Move the position of tank2 to a random location on the screen
2. Set the tank1 bullet to be inactive
3. Increase the score of tank1 by 1 point

<div id="CollideRect-sortableTrash" class="sortable-code"></div> 
<div id="CollideRect-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="CollideRect-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="CollideRect-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "if tank1_bullet.colliderect(tank2):\n" +
    "	tank2.pos = (random.randint(50, 250), random.randint(50, HEIGHT - 50))\n" +
    "	tank1_bullet.isActive = False         \n" +
    "	tank1.score += 1\n" +
    "tank1_bullet.isActive = True #distractor\n" +
    "tank2.score += 1 #distractor\n" +
    "tank1.pos = (random.randint(50, 250), random.randint(50, HEIGHT - 50)) #distractor\n" +
    "if tank1_bullet.colliderect(tank1): #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "CollideRect-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "CollideRect-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#CollideRect-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#CollideRect-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

[Next](./example2.html)
