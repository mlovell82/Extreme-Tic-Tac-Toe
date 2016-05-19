
<html>
  <head>
    <style>
    
    </style>
<script type="text/javascript">
var gameOver = false;
  function toggleLike(score,btId){ // This function calls play(), winnerYet(), and celebration() upon each click of the game board
    play(btId);
    //winnerYet();
	//celebration();
  }
  function play(btId){ // This function decides if 'O' or 'X' is to be played
  var space = [];
  var i, count;
  count = 0;
  space[0] = document.getElementById("a1").value;
  space[1] = document.getElementById("a2").value;
  space[2] = document.getElementById("a3").value;
  space[3] = document.getElementById("a4").value;
  space[4] = document.getElementById("a5").value;
  space[5] = document.getElementById("a6").value;
  space[6] = document.getElementById("a7").value;
  space[7] = document.getElementById("a8").value;
  space[8] = document.getElementById("a9").value;
  space[9] = document.getElementById("b1").value;
  space[10] = document.getElementById("b2").value;
  space[11] = document.getElementById("b3").value;
  space[12] = document.getElementById("b4").value;
  space[13] = document.getElementById("b5").value;
  space[14] = document.getElementById("b6").value;
  space[15] = document.getElementById("b7").value;
  space[16] = document.getElementById("b8").value;
  space[17] = document.getElementById("b9").value;
  space[18] = document.getElementById("c1").value;
  space[19] = document.getElementById("c2").value;
  space[20] = document.getElementById("c3").value;
  space[21] = document.getElementById("c4").value;
  space[22] = document.getElementById("c5").value;
  space[23] = document.getElementById("c6").value;
  space[24] = document.getElementById("c7").value;
  space[25] = document.getElementById("c8").value;
  space[26] = document.getElementById("c9").value;
  
  
  for(i = 0; i < space.length; i++){
	if(space[i] == " ")
		count++;
	}
	
 if(((count == 27) || (count == 25)|| (count == 23) || (count == 21) || (count == 19) || (count == 17) || (count == 15) || (count == 13) || (count == 11) || (count == 9) || (count == 7) || (count == 5) || (count == 3) || (count == 1)) && (document.getElementById(btId).value == " ")) 
	document.getElementById(btId).value = "X";
if(((count == 26) || (count == 24) || (count == 22) || (count == 20) || (count == 18) || (count == 16) || (count == 14) || (count == 12) || (count == 10) || (count == 8) || (count == 6) || (count == 4) || (count == 2)) && (document.getElementById(btId).value == " "))
	document.getElementById(btId).value = "O";
  }
  function winnerYet(){ // This function decides if the 'O's or the 'X's won the game
  var one = document.getElementById("a1").value;
  var two = document.getElementById("a2").value;
  var three = document.getElementById("a3").value;
  var four = document.getElementById("a4").value;
  var five = document.getElementById("a5").value;
  var six = document.getElementById("a6").value;
  var seven = document.getElementById("a7").value;
  var eight = document.getElementById("a8").value;
  var nine = document.getElementById("a9").value;
  var ten = document.getElementById("b1").value;
  var eleven = document.getElementById("b2").value;
  var twelve = document.getElementById("b3").value;
  var thirteen = document.getElementById("b4").value;
  var fourteen = document.getElementById("b5").value;
  var fifteen = document.getElementById("b6").value;
  var sixteen = document.getElementById("b7").value;
  var seventeen = document.getElementById("b8").value;
  var eighteen = document.getElementById("b9").value;
  var nineteen = document.getElementById("c1").value;
  var twenty = document.getElementById("c2").value;
  var twentyone = document.getElementById("c3").value;
  var twentytwo = document.getElementById("c4").value;
  var twentythree = document.getElementById("c5").value;
  var twentyfour = document.getElementById("c6").value;
  var twentyfive = document.getElementById("c7").value;
  var twentysix = document.getElementById("c8").value;
  var twentyseven = document.getElementById("c9").value;
  
  if(((one =='X') && (two == 'X') && (three == 'X')) || ((four == 'X') && (five == 'X') && (six == 'X')) || ((seven == 'X') && (eight == 'X') && (nine == 'X')) || ((one == 'X') && (five == 'X') && (nine == 'X')) || ((three == 'X') && (five == 'X') && (seven == 'X')) || ((one == 'X') && (four == 'X') && (seven == 'X')) || ((two == 'X') && (five == 'X') && (eight == 'X')) || ((three == 'X') && (six == 'X') && (nine == 'X'))){
	window.alert("X is winner!");
	gameOver = true;
	}
  if(((one =='O') && (two == 'O') && (three == 'O')) || ((four == 'O') && (five == 'O') && (six == 'O')) || ((seven == 'O') && (eight == 'O') && (nine == 'O')) || ((one == 'O') && (five == 'O') && (nine == 'O')) || ((three == 'O') && (five == 'O') && (seven == 'O')) || ((one == 'O') && (four == 'O') && (seven == 'O')) || ((two == 'O') && (five == 'O') && (eight == 'O')) || ((three == 'O') && (six == 'O') && (nine == 'O'))){
	window.alert("O is winner!")
	gameOver = true;
	}
  }
  function celebration(){ // This function restarts game
  if(gameOver){
	document.getElementById("a1").value = " ";
    document.getElementById("a2").value = " ";
    document.getElementById("a3").value = " ";
    document.getElementById("b1").value = " ";
    document.getElementById("b2").value = " ";
    document.getElementById("b3").value = " ";
    document.getElementById("c1").value = " ";
    document.getElementById("c2").value = " ";
    document.getElementById("c3").value = " ";
	gameOver = false;
	}
  }
  </script>
  </head>
  <body>
    <table>
      <tr>
        <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="a1" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="a2" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="a3" style="width:100%; height:100%;"></td>
  </tr>
  <tr>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="a4" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="a5" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="a6" style="width:100%; height:100%;"></td>
  </tr>
  <tr>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="a7" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="a8" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="a9" style="width:100%; height:100%;"></td>
  </tr>
</table>
<table align="center">
      <tr>
        <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="b1" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="b2" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="b3" style="width:100%; height:100%;"></td>
  </tr>
  <tr>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="b4" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="b5" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="b6" style="width:100%; height:100%;"></td>
  </tr>
  <tr>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="b7" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="b8" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="b9" style="width:100%; height:100%;"></td>
  </tr>
</table>
<table align="right">
      <tr>
        <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="c1" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="c2" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="c3" style="width:100%; height:100%;"></td>
  </tr>
  <tr>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="c4" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="c5" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="c6" style="width:100%; height:100%;"></td>
  </tr>
  <tr>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="c7" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="c8" style="width:100%; height:100%;"></td>
    <td><input onclick="toggleLike(this.value,this.id)" type="button" value=" " id="c9" style="width:100%; height:100%;"></td>
  </tr>
</table>
  </body>
</html>
