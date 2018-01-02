<!DOCTYPE html>
<html>
<head>
<style>
	body {
		font-family: "Times New Roman", Times, serif;
	}
	
	.tab {
		overflow: hidden;
	}
	.tab button {
		background-color: inherit;
		float: left;
		border: none;
		outline: none;
		cursor: pointer;
		padding: 14px 16px;
		transition: 0.1s;
		font-size: 17px;
		font-family: "Times New Roman", Times, serif;
		text-decoration: underline;
	}
	.tab button.active {
		background-color: #fbfbfb;
	}
	.tabcontent {
		display: none;
		padding: 6px 12px;
		border-top: none;
	}
</style>
</head>
<body>

<div class="tab">
  <button class="tablinks" onclick="openCity(event, 'General')">General</button>
  <button class="tablinks" onclick="openCity(event, 'Paris')">Paris</button>
  <button class="tablinks" onclick="openCity(event, 'Tokyo')">Tokyo</button>
</div>

<div id="General" class="tabcontent">
	Fuel: <span id="fuel">0</span> Fuel
	
	
</div>

<div id="Paris" class="tabcontent">
  <h3>Paris</h3>
  <p>Paris is the capital of France.</p> 
</div>

<div id="Tokyo" class="tabcontent">
  <h3>Tokyo</h3>
  <p>Tokyo is the capital of Japan.</p>
</div>

<script>
function openCity(evt, cityName) {
    var i, tabcontent, tablinks;
    tabcontent = document.getElementsByClassName("tabcontent");
    for (i = 0; i < tabcontent.length; i++) {
        tabcontent[i].style.display = "none";
    }
    tablinks = document.getElementsByClassName("tablinks");
    for (i = 0; i < tablinks.length; i++) {
        tablinks[i].className = tablinks[i].className.replace(" active", "");
    }
    document.getElementById(cityName).style.display = "block";
    evt.currentTarget.className += " active";
}
</script>
     
</body>
</html>
