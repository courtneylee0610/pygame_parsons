---
layout: default
title: Crystal 1
---

Create a new Pygame Zero game that will:
1. import the pgzrun library
2. Set the WIDTH of the screen to 1200
3. Set the HEIGHT of the screen to 768

<div id="New Pygame-sortableTrash" class="sortable-code"></div> 
<div id="New Pygame-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="New Pygame-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="New Pygame-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "import pgzrun\n" +
    "WIDTH = 1200\n" +
    "HEIGHT = 768\n" +
    "set width = 1200 #distractor\n" +
    "set height = 768 #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "New Pygame-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "New Pygame-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#New Pygame-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#New Pygame-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
[Next](./crystal2.html)
