---
layout: post
title:  "First problems with the Wikipedia viewer project"
date:   2017-05-02
---
<ul>
	<li><a href="#prob0">Problem 0</a></li>
	<li><a href="#prob1">Problem 1</a></li>
</ul>


<h4 id="prob0">Problem 0</h4>

**What I wanted**: you can type a word in the text box and then click the magnifier icon or press the enter key and get the same result.

**What I wrote**: 

'''javascript
//manejador del evento del click sobre el ícono de la lupa
$('#lupa').on('click', function buscar(){
	var aBuscar = $('#buscadorInput').val();
	console.log("Quiere buscar: " + aBuscar);

	$.getJSON("wikisearchperro.json", function(data){
		//mostrar los resultados
		console.log(data);
		$('#resultados').html("<p> Resultados obtenidos: " + aBuscar + "</p>");
		$('#resultados').append("<br/>");
		$('#resultados').append("<p>"+ data.query.search[0].title + "</p>");
		$('#resultados').append("<p>"+ data.query.search[0].snippet + "</p>");
		//	$('#resultados').append("<p></p>");
		$('#resultados').css("background-color", "#2E2D88");
		$('#resultados').css("color", "white");
	});
});
//manejador del evento de la tecla enter
$('#buscadorInput').on('keyup', function buscar(event){
		var aBuscar = $('#buscadorInput').val();
		console.log("Quiere buscar: " + aBuscar);
		$(this).css("background-color", event.which === 13 ? "#2E2D88" : '#fff');
		$(this).css("color", event.which === 13 ? '#fff': "#2E2D88");
		if (event.which === 13){
			console.log("apretó enter");
			$('#resultados').html("<p> Resultados obtenidos: " + aBuscar + "</p>");
			//$('#resultados').css("background-color", "#2E2D88");
			//$('#resultados').css("color", "white");
			//alert("enter");
		} else {
			console.log("no apretó enter");
		}
});
'''

**What I got**: if you type something in the text box and press enter (the first time, before you try clicking the icon once) it's as if you reset the page, the text you just typed disapears, it is as if you reload the page. But if you write something in the box and then click, it works, and then you write something elsee and press enter, that also works. So, it works but not if what you do first is press the enter key after typing in the box.

**What I changed**: I put the code for the key event handler before the click event handler.
**Results**: Apparently, now it works. But I think it needs further testing.

**Observation**: If I make a search, then I reload the page, the text I wrote in the box is still there. Why is that? How do you clear it?

<h4 id="prob1">Problem 1</h4>

In my first attempt to use the api I got the following error:
"XMLHttpRequest cannot load" ...
"No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin 'null' is therefore not allowed access."

Then I search in the freecodecamp forum and found that if you use _&origin=*_ at the end of the query it works.
Also I found that to get a list of 10 results for your search use: _https://es.wikipedia.org/w/api.php?action=query&format=json&list=search&srsearch=whatYouWantToSearch&origin=*_
You'll get data in jason format.