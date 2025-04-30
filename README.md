✅ HTML (index.html)

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Online Restaurant Menu</title>
  <link rel="stylesheet" href="5.css" />
</head>
<body>
  <header>
    <h1>Welcome to JAAT Restaurant!</h1>
    <p>Explore our desi menu below</p>
  </header>

  <main>
    <ol>
      <li onclick="highlight(this)">Nashta</li>
      <li onclick="highlight(this)">Mukhya Bhojan</li>
      <li onclick="highlight(this)">Misthan Bhandar</li>
    </ol>

    <section class="menu-section" id="Nashta">
      <h2>Nashta</h2>
      <ul>
        <li>
          <img src="https://static.toiimg.com/photo/53109843.cms" alt="Aloo Ke Paranthe" />
          <p><strong>Aloo Paranthe</strong><br> Swadisht Aloo ke paranthe with Dahi.</p>
        </li>
        <li>
          <img src="https://www.eatingwell.com/thmb/BFKxRmk1Julcr1ldWafGvzVChxk=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/chole-bhature-beauty1x1-921-f66fc717da044251be01feb1cd0dba3e.jpg" alt="Chole Puri" />
          <p><strong>Chole Puri</strong><br> Mast Puri with chole.</p>
        </li>
      </ul>
    </section>

    <section class="menu-section" id="Mukhya">
      <h2>Mukhya Bhojan</h2>
      <ul>
        <li>
          <img src="https://www.vanillabeancuisine.com/wp-content/uploads/2024/12/Spaghetti-Alfredo-2nd-Set-7.jpg" alt="Dal Roti and Dal Chawal" />
          <p><strong>Dal Roti and Dal Chawal</strong><br> Proper Desi .</p>
        </li>
        <li>
          <img src="https://www.allrecipes.com/thmb/Bw4L_IuQHhHeqq52cEkWbA5PIGo=/0x512/filters:no_upscale():max_bytes(150000):strip_icc()/16160-juicy-grilled-chicken-breasts-ddmfs-5594-hero-3x4-902673c819994c0191442304b40104af.jpg" alt="Grilled Chicken" />
          <p><strong>Grilled Chicken</strong><br> Juicy grilled chicken served with rice.</p>
        </li>
      </ul>
    </section>

    <section class="menu-section" id="Misthan">
      <h2>Desserts</h2>
      <ul>
        <li>
          <img src="https://www.indianhealthyrecipes.com/wp-content/uploads/2024/06/classic-chocolate-cake-recipe-500x500.jpg" alt="Chocolate Cake" />
          <p><strong>Chocolate Cake</strong><br> Rich and moist chocolate layered cake.</p>
        </li>
        <li>
          <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcToNb4qLVc8li_M2NHBfEl14DaVpUCmplY5lg&s" alt="Ice Cream" />
          <p><strong>Vanilla Ice Cream</strong><br> Classic creamy vanilla flavor.</p>
        </li>
      </ul>
    </section>
  </main>

  <script src="1.js"></script>
</body>
</html>


🎨 CSS (5.css)
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Segoe UI', sans-serif;
  background: url('https://t3.ftcdn.net/jpg/02/05/87/60/360_F_205876015_hYYs7ugqoU8QAobSS3TbnGQ92qyS5gEc.jpg');
  background-color: #fff8e1;
  color: #333;
}

header {
  background-color: #ff7043;
  padding: 20px;
  text-align: center;
  color: white;
}

ol {
  display: flex;
  justify-content: center;
  background-color: #ffe0b2;
  padding: 10px;
  list-style-position: inside;
  font-weight: bold;
  cursor: pointer;
}

ol li {
  margin: 0 15px;
  padding: 10px 20px;
  border: 2px solid transparent;
  border-radius: 10px;
  transition: 0.3s;
}

ol li:hover, ol li.active {
  border-color: #ff5722;
  background-color: #fff3e0;
}

.menu-section {
  padding: 20px;
}

.menu-section h2 {
  margin-bottom: 15px;
  color: #e64a19;
}

.menu-section ul {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  list-style: none;
}

.menu-section ul li {
  background-color: #fff3e0;
  border: 1px solid #ffccbc;
  border-radius: 10px;
  padding: 10px;
  width: 200px;
  text-align: center;
}

.menu-section img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
}

✨ JavaScript (1.js)
function highlight(element) {
  const items = document.querySelectorAll("ol li");
  items.forEach((item) => item.classList.remove("active"));
  element.classList.add("active");
}
