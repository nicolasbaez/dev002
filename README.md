# videoNico
Creando la interfaz para YouTube
Funciona usando F12 y ajustando las preferencias del editor!

![videoNico](https://github.com/nicolasbaez/videoNico/blob/master/portada.png)

1. gameDev.htm
```html
<html>
	<script src="p5.js">//carga processing para javascript</script>
	<script src="p5.dom.js">//carga processing para las características del navegador</script>
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
