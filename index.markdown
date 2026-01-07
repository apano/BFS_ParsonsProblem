---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Algoritmo di ricerca in ampiezza
---
# Parsons 5 Breadth First Algorithm 
## BDF
Ordina i blocchi che compongono l'algoritmo di Ricerca in ampiezza (BFS).
<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "BFS(G, s)\n" +
    "Queue Q\n" +
    "for each vertex v in G:\n" +
    "    mark_unvisited(v)\n" +
    "Q.enqueue(s)          \n" +
    "mark(s)               \n" +
    "while Q is not empty:\n" +
    "    u = Q.front()\n" +
    "    for each vertex w adjacent to u:\n" +
    "        if w is not visited:\n" +
    "            mark(w)\n" +
    "            Q.enqueue(w)\n" +
    "    Q.dequeue()";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
