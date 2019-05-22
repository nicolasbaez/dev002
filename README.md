# videoNico
Creando la interfaz para YouTube, funciona usando F12 y ajustando las preferencias del editor!

![videoNico](https://github.com/nicolasbaez/videoNico/blob/master/portada.png)

1. videoNico.htm
```html
<html>
	<script src="p5.js">
		//Descarga: https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.js
	</script>
	<script src="p5.dom.js">
		//Descarga: https://raw.githubusercontent.com/lmccart/p5.js/master/lib/addons/p5.dom.js
	</script>
	<script>
		let capture;
		var filtro=[];
		var videoY=[];
		var dy=0;
		var cuadros=10;
		function setup(){
			var videoNico=createCanvas(window.innerWidth, window.innerHeight);
			capture = createCapture(VIDEO);
			capture.size(width, width*0.75);
			capture.position(0,0);
			capture.hide();
			for(var i=0;i<cuadros;i++){
				filtro[i]=int(random(3));
				videoY[i]=dy;
				dy+=width*0.75;
			}
		}
		function draw(){
			for(var i=0;i<=cuadros;i++){
				image(capture, 0, videoY[i], width, width*0.75);
				switch(filtro[i]){
					case 0:filter(POSTERIZE, 3);
					break;
					case 1:filter(INVERT);
					break;
					case 2:filter(THRESHOLD);
					break;
					default:
				}
				videoY[i]--;
				if(videoY[i]<-width*0.75){
					videoY[i]=(width*0.75)*(cuadros-1);
					filtro[i]=int(random(3));
				}
			}
		}
	</script>
	<body style="margin:0;">
	</body>
</html>
```
