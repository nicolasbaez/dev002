# dev002
Aprendiendo a Programar
```html
<!-- Así hago un comentario en HTML, con la etiqueta <script></script> puedo empezar mi programa -->
<script>
	//Esta es una variable
	var a;
	//Esta es la asignación de un valor a la variable
	var a=12;
	//Así se muestra el valor de la variable
	alert(a);
	//Así se opera una variable (+ suma, + resta, * multiplicación, / división
	var a=3;
	var b=5;
	var c=a+b;
	//Así imprimo el resultado de mi operación
	alert(c);
	//Así condiciono una variable (== igual, > mayor que, < menor que, >= mayor o igual que, <= menor o igual que, != diferente
	if(c==8){
		alert(8);
	}
	//Así incremento una variable (+ para incrementar, - para decrementar)
	c=c+1; //incrementa uno
	c++; //incrementa uno
	c+=1; //incrementa uno
	c+=2; //incrementa dos
	//Así controlo un ciclo (declaro la variable que controlaré y le pongo un valor inicial; declaro en qué valor debe terminar; declaro cada cuanto incrementa)
	for(var i=0;i<=10;i++){
		alert(i);
	}
	//Así creo un array
	var ejemplo = [];
	//Así le asigno los valores a un array
	ejemplo[0]=45;
	ejemplo[1]=2;
	ejemplo[2]=3;
	//Así puedo imprimir los valores de mi array
	for(var i=0;i<=2;i++){
		alert(ejemplo[i]);
	}
	var a=0;
	for(var i=0;i<=12;i+=2){
		a=i;
		switch(a){
			case 0:alert("Hola");
			break;
			case 2:alert("Cómo");
			break;
			case 4:alert("Estás");
			break;
			case 6:alert("Nicolás");
			break;
			case 8:alert("?");
			break;
			case 12:alert("ok, gracias");
			break;
		}
	}    
</script>
```
