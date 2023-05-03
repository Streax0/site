<!DOCTYPE html>
<html>
<head>
	<title>Minecraft Server</title>
	<style>
		body {
			margin: 0;
			padding: 0;
			font-family: Arial, sans-serif;
			background-color: #333;
			color: #fff;
		}

		header {
			display: flex;
			flex-direction: row;
			justify-content: space-between;
			align-items: center;
			padding: 20px;
			background-color: #1c07a3;
			position: fixed;
			top: 0;
			left: 0;
			width: 100%;
			z-index: 1;
		}

		header h1 {
			font-size: 36px;
			font-weight: bold;
			color: #fff;
			text-shadow: 2px 2px #333;
		}

		nav a {
			font-size: 18px;
			font-weight: bold;
			color: #fff;
			text-decoration: none;
			margin-left: 20px;
			transition: color 0.5s ease;
		}

		nav a:hover {
			color: #00bfff;
		}

		.server-status {
			display: flex;
			justify-content: center;
			align-items: center;
			background-color: #00bfff;
			padding: 10px;
			position: fixed;
			top: 80px;
			left: 0;
			width: 100%;
			z-index: 1;
		}

		.server-status p {
			font-size: 18px;
			font-weight: bold;
			color: #fff;
			margin: 0;
		}

		.gray-label {
			background-color: #1f1c1c03;
			padding: 20px;
			text-align: center;
			margin-top: 50px;
			animation: slide-up 1s ease;
		}

		.home {
			max-width: 1000px;
			margin: auto;
			padding: 50px;
			text-align: center;
			animation: slide-up 1s ease;
		}

		.home h2 {
			font-size: 36px;
			font-weight: bold;
			margin-bottom: 20px;
			color: #fff;
		}

		.home p {
			font-size: 18px;
			line-height: 1.5;
			margin-bottom: 20px;
			color: #fff;
		}

		.server-info {
			max-width: 1000px;
			margin: auto;
			padding: 50px;
			text-align: center;
			animation: slide-up 1s ease;
		}

		.server-info h2 {
			font-size: 36px;
			font-weight: bold;
			margin-bottom: 20px;
			color: #fff;
		}

		.server-info ul {
			list-style: none;
			padding: 0;
			margin: 0;
			flex-direction: column;
			display: flex;
			flex-wrap: wrap;
			justify-content: center;
			align-items: center;
		}

		.server-info li {
			font-size: 18px;
			line-height: 1.5;
			flex-direction: column;
			margin-bottom: 20px;
			color: #fff;
			margin-right: 50px;
		}

		.mods {
			max-width: 1000px;
			margin: auto;
			padding: 50px;
			text-align: center;
			animation: slide-up 1s ease;
		}

		.mods h2 {
			font-size: 36px;
			font-weight: bold;
			margin-bottom: 20px;
			color: #fff;
		}

		.mods p {
			font-size: 18px;
			line-height: 1.5;
			margin-bottom: 20px;
			color: #fff;
		}

		.mods ul {
			list-style: none;
			padding: 0;
			margin: 0;
			flex-direction: column;
			display: flex;
			flex-wrap: wrap;
			justify-content: center;
			align-items: center;
		}

		.mods li {
			font-size: 18px;
			line-height: 1.5;
			flex-direction: column;
			margin-bottom: 20px;
			color: #fff;
			margin-right: 50px;
		}

		.contact {
			max-width: 1000px;
			margin: auto;
			padding: 50px;
			text-align: center;
			animation: slide-up 1s ease;
		}

		.contact h2 {
			font-size: 36px;
			font-weight: bold;
			margin-bottom: 20px;
			color: #fff		}

.contact form {
	display: flex;
	flex-direction: column;
	align-items: center;
	margin-top: 50px;
}

.contact label {
	font-size: 18px;
	font-weight: bold;
	margin-bottom: 10px;
	color: #fff;
}

.contact input[type="text"],
.contact input[type="email"],
.contact textarea {
	width: 100%;
	padding: 10px;
	margin-bottom: 20px;
	border: none;
	border-radius: 5px;
	background-color: #fff;
	color: #333;
	font-size: 18px;
	font-weight: bold;
}

.contact textarea {
	height: 200px;
	resize: none;
}

.contact input[type="submit"] {
	background-color: #00bfff;
	color: #fff;
	font-size: 18px;
	font-weight: bold;
	padding: 10px 20px;
	border: none;
	border-radius: 5px;
	cursor: pointer;
	transition: background-color 0.5s ease;
}

.contact input[type="submit"]:hover {
	background-color: #fff;
	color: #00bfff;
}

.banner {
	background-image: url('https://th.bing.com/th/id/OIP.Meh09pYT0QTqe8JJy1G-MgHaEK?w=313&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7');
	background-size: cover;
	background-position: center;
	height: 500px;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	text-align: center;
	animation: slide-up 1s ease;
}

.banner h2 {
	font-size: 48px;
	font-weight: bold;
	margin-bottom: 20px;
	color: #fff;
	text-shadow: 2px 2px #333;
}

.banner p {
	font-size: 24px;
	margin-bottom: 20px;
	color: #fff;
	text-shadow: 2px 2px #333;
}

.slideshow-container {
	max-width: 1000px;
	margin: auto;
	position: relative;
	animation: slide-up 1s ease;
}

.mySlides {
	display: none;
	max-width: 1000px;
	margin: auto;
}

.mySlides img {
	width: 100%;
	height: 500px;
	object-fit: cover;
}

.prev,
.next {
	position: absolute;
	top: 50%;
	transform: translateY(-50%);
	font-size: 36px;
	font-weight: bold;
	padding: 10px;
	color: #fff;
	background-color: rgba(0, 0, 0, 0.5);
	cursor: pointer;
	transition: background-color 0.5s ease;
}

.next {
	right: 0;
}

.prev:hover,
.next:hover {
	background-color: rgba(0, 0, 0, 0.8);
}

.dot-container {
	text-align: center;
	margin-top: 20px;
}

.dot {
	display: inline-block;
	width: 10px;
	height: 10px;
	border-radius: 50%;
	background-color: #bbb;
	margin: 0 5px;
	cursor: pointer;
	transition: background-color 0.5s ease;
}

.active,
.dot:hover {
	background-color: #00bfff;
}

@keyframes slide-up {
	from {
		transform: translateY(50px);
		opacity: 0;
	}

	to {
		transform: translateY(0);
		opacity: 1;
	}
}
</style>
</head>
<body>
<header>
<h1>Minecraft Server</h1>
<nav>
	<a href="#home">Home</a>
	<a href="#server-info">Server Info</a>
	<a href="#mods">Mods</a>
	<a href="#contact">Contact</a>
</nav>
</header>

<div class="server-status">
<p> Server Status: Offline</p>
</div>

<div class="banner">
	<h2>Welcome to our Minecraft Server</h2>
</div>

<div class="slideshow-container">



	<div class="mySlides fade">
		<img src="https://th.bing.com/th/id/OIP.XQgj5hdHVXctfnNTNSGioQHaD7?w=327&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7">
	</div>

	<div class="mySlides fade">
		<img src="https://th.bing.com/th?id=OIP.gucONe0mb3nU30bHNii1FgHaEK&w=333&h=187&c=8&rs=1&qlt=90&o=6&dpr=1.3&pid=3.1&rm=2">
	</div>

<div class="mySlides fade">
	<img src="https://th.bing.com/th/id/R.d29124461100b9bd175f8209f35c930d?rik=IRmAhNYL3BrHbQ&pid=ImgRaw&r=0">
</div>

	<div class="mySlides fade">
		<img src="https://th.bing.com/th/id/OIP.UYaOC81OHI5P8fFmH6LolAHaEK?w=313&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7">
	</div>

	<a class="prev" onclick="plusSlides(-1)">&#10094;</a>
	<a class="next" onclick="plusSlides(1)">&#10095;</a>
</div>

<div class="dot-container" style="text-align:center">
	<span class="dot" onclick="currentSlide(1)"></span>
	<span class="dot" onclick="currentSlide(2)"></span>
	<span class="dot" onclick="currentSlide(3)"></span>
	<span class="dot" onclick="currentSlide(4)"></span>
</div>

<div class="gray-label" id="home">
	<div class="home">
		<h2>Welcome to our Minecraft Server</h2>
		<p>Our server is a fun and friendly place to play Minecraft with your friends. We have a variety of game modes and features to keep you entertained for hours. Join us today and start your adventure!</p>
	</div>
</div>

<div class="gray-label" id="server-info">
	<div class="server-info">
		<h2>Server Info</h2>
		<ul>
			<li>Server IP: play.minecraftserver.com</li>
			<li>Game Modes: Survival</li>
			<li>Max Players: 20</li>
			<li>Version: 1.19.2 Fabric </li>
		</ul>
	</div>
</div>

<div class="gray-label" id="mods">
	<div class="mods">
		<h2>Mods</h2>
		<p>We have a variety of mods installed on our server to enhance your gameplay experience. Here are just a few of the mods we have:</p>
		<ul>
			<li><a href="https://www.curseforge.com/minecraft/mc-mods/optifabric/files">OptiFine</a>			</li>
			<li><a href="https://www.curseforge.com/minecraft/mc-mods/betterend/files">BetterEnd [Fabric]</a>			</li>
			<li><a href="https://www.curseforge.com/minecraft/mc-mods/capybara-fabric/files">CapyBara [Fabric]</a>			</li>
			<li><a href="https://www.curseforge.com/minecraft/mc-mods/betteranimalsplus/files/3825878">Better Animals Plus [Fabric] </a>			</li>
			<li><a href="https://www.curseforge.com/minecraft/mc-mods/betternether/files/3866286">Better Nether [Fabric]e</a>			</li>
			<li><a href="https://www.curseforge.com/minecraft/mc-mods/create-fabric/files">Create [Fabric]</a>			</li>
			<li><a href="https://fabricmc.net/">Fabric</a>			</li>
			<li><a href="https://www.curseforge.com/minecraft/mc-mods/create-fabric/files">Fabric api</a>			</li>




		</ul>
	</div>
</div>

<div class="gray-label" id="contact">
	<div class="contact">
		<h2>Contact Us</h2>
		<form>
			<label for="name">Name:</label>
			<input type="text" id="name" name="name" required>

			<label for="email">Email:</label>
			<input type="email" id="email" name="email" required>

			<label for="message">Message:</label>
			<textarea id="message" name="message" required></textarea>

			<input type="submit" value="Send">
		</form>
	</div>
</div>

<script>
	var slideIndex = 1;
	showSlides(slideIndex);

	function plusSlides(n) {
		showSlides(slideIndex += n);
	}

	function currentSlide(n) {	showSlides(slideIndex = n);
		}

		function showSlides(n) {
			var i;
			var slides = document.getElementsByClassName("mySlides");
			var dots = document.getElementsByClassName("dot");
			if (n > slides.length) {
				slideIndex = 1
			}
			if (n < 1) {
				slideIndex = slides.length
			}
			for (i = 0; i < slides.length; i++) {
				slides[i].style.display = "none";
			}
			for (i = 0; i < dots.length; i++) {
				dots[i].className = dots[i].className.replace(" active", "");
			}
			slides[slideIndex - 1].style.display = "block";
			dots[slideIndex - 1].className += " active";
		}
	</script>
</body>
</html>
