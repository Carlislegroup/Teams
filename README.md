<style>
  body {
  background-color: #232323;
}

#team {
  box-shadow: 0px 0px 50px rgba(255,255,255,.25);
}

#team td {
  height: 75px;
  width: 300px;
  text-align: center;
  font-family: Helvetica, Arial, san-serif;
  text-transform: uppercase;
  font-weight: bold;
  background-color: #000000;
  color: #ffffff;
  font-size: 24px;
  padding: 0px;
}

#team .title {
  height: 30px;
  font-size: 16px;
}

#team .blue {
  background-color: dodgerblue;
}

#team .red {
  background-color: tomato;
}

#team .green {
  background-color: olive;
}

#team .orange {
  background-color: orange;
}

#team .grey {
  background-color: #686868;
}

.fade {
   opacity: 1;
   transition: opacity .1s ease-in-out;
   -moz-transition: opacity .1s ease-in-out;
   -webkit-transition: opacity .1s ease-in-out;
   }
</style>
<script>
var team = [
  "Sandra Tom*",
  "Jerry Lin*",
  "Josh Renaud*",
  "Katie Bostian",
  "Sammy Singh",
  "Nader Shehayed*",
  "Joseph Tu*",
  "Jazmarie Opinia",
  "James Kim"
];
var text = "";

function shuffle(array) {
  var currentIndex = array.length, temporaryValue, randomIndex;

  // While there remain elements to shuffle...
  while (0 !== currentIndex) {

    // Pick a remaining element...
    var randomIndex = Math.floor(Math.random() * currentIndex);
    currentIndex -= 1;

    // And swap it with the current element.
    var temporaryValue = array[currentIndex];
    array[currentIndex] = array[randomIndex];
    array[randomIndex] = temporaryValue;
  }

  return array;
}


function shuffler() {
  shuffle(team);
  document.getElementById("player-0").innerHTML = team[0];
  document.getElementById("player-1").innerHTML = team[1];
  document.getElementById("player-2").innerHTML = team[2];
  document.getElementById("player-3").innerHTML = team[3];
  document.getElementById("player-4").innerHTML = team[4];
  document.getElementById("player-5").innerHTML = team[5];
  document.getElementById("player-6").innerHTML = team[6];
  document.getElementById("player-7").innerHTML = team[7];
  document.getElementById("player-8").innerHTML = team[8];
}

// var myInterval = setInterval(shuffler, 50);
// clearInterval(myInterval);

document.getElementById("random").addEventListener("click", shuffler);

window.addEventListener("keypress", checkKeyPressed, false);
 
function checkKeyPressed(e) {
    if (e.charCode == "32") {
      document.getElementById("random").addEventListener("click", shuffler);    
    }
}

</script>
<body>
  <table align="center" id="team" cellpadding="0" cellspacing="0">
    <tr>
      <td colspan="2" class="title">
        Team 1
      </td>
    </tr>
    <tr>
      <td id="player-0" class="blue"></td>
      <td id="player-1" class="blue"></td>
    </tr>
    <tr>
      <td colspan="2" class="title">
        Team 2
      </td>
    </tr>
    <tr>
      <td id="player-2" class="red"></td>
      <td id="player-3" class="red"></td>
    </tr>
    <tr>
      <td colspan="2" class="title">
        Team 3
      </td>
    </tr>
    <tr>
      <td id="player-4" class="green"></td>
      <td id="player-5" class="green"></td>
    </tr>
    <tr>
      <td colspan="2" class="title">
        Team 4
      </td>
    </tr>
    <tr>
      <td id="player-6" class="orange"></td>
      <td id="player-7" class="orange"></td>
    </tr>
    <tr>
      <td colspan="2" class="title">
        Team 5
      </td>
    </tr>
    <tr>
      <td colspan="2" id="player-8" class="grey"></td>
    </tr>
  </table>
  <table width="600" align="center">
    <tr>
      <td colspan="2" align="right">
        <button id="random">RANDOM</button>
      </td>
    </tr>
  </table>
</body>
