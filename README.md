<!DOCTYPE html>
<html>
<head>
	<title>Download Image on Click</title>
	<script>
		function downloadImage() {
			var url = document.getElementById("myImage").src;
			var filename = url.substring(url.lastIndexOf('/')+1);
			var element = document.createElement('a');
			element.setAttribute('href', url);
			element.setAttribute('download', filename);
			element.style.display = 'none';
			document.body.appendChild(element);
			element.click();
			document.body.removeChild(element);
		}
	</script>
</head>
<body>
	<img id="myImage" src="https://example.com/image.jpg" alt="Image" onclick="downloadImage()">
</body>
</html>
