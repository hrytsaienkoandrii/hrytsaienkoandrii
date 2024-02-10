<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Proposal</title>
</head>

<body>
    <div class="container">
        <div class="Mainprompt">
            <img class="image" src="images/cute.gif"></img>
            <div class="text">
              <h1 class="hh" id="name">Привіт, красуне!</h1>
              <p class="pp" id="question">Ти будеш моєю Валентинкою? </p>
            </div>
            <div class="buttons">
                <button class="button no" id="no-button" onclick="showMessage('No')">Ні</button>
                <button class="button yes"  onclick="showMessage('Yes')" id="yesButton">Так</button>
            </div>
        </div>
    </div>
    <script>

      const button = document.getElementById('no-button');

      // Add event listener for mouseenter event
      button.addEventListener('mouseenter', function() {
          showMessage('No')
      });

      function showMessage(response) {
  if (response === "No") {
    const noButton = document.getElementById("no-button");
    const container = document.querySelector(".container");
    const maxWidth = window.innerWidth - noButton.offsetWidth;
    const maxHeight = window.innerHeight - noButton.offsetHeight;

    noButton.style.position = "absolute";

    document.getElementsByClassName("image")[0].src = "images/gun.gif";

    const randomX = Math.max(0, Math.floor(Math.random() * maxWidth));
    const randomY = Math.max(0, Math.floor(Math.random() * maxHeight));

    noButton.style.left = randomX + "px";
    noButton.style.top = randomY + "px";

    document.getElementById("question").textContent =
      "Альо, ти що там задумала?";
    document.getElementById("name").style.display = "none";

  }

  if (response === "Yes") {
    document.getElementById("name").remove();
    document.getElementById("no-button").remove();

    const yesMessage = document.getElementById("question");
    yesMessage.textContent = "Ти моя бусінка 😘";
    yesMessage.style.display = "block";
    yesMessage.style.fontStyle = "normal";
    document.getElementsByClassName("image")[0].src = "images/kiss.gif";

    document.getElementById("yesButton").remove();
  }
}
    </script>
</body>

</html>



body {
  margin-top: 100px;
  background-color: #ffdde1;
  display: flex;
  justify-content: space-evenly;
  height: 100vh;
  margin: 0;
  background: url("images/image.jpg") repeat;
  font-size: 35px;
  color: rgb(255, 0, 174);
  height: 100vh;
  position: fixed;
  width: 100%;
}
.hh {
  -webkit-text-stroke: 2px #71004f;
  font-weight: 900;
  font-size: 50px;
}
.pp {
  -webkit-text-stroke: 2px #71004f;
  font-size: 30px;
  font-style: oblique;
  font-weight: 800;
}

body .container {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: transparent;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
}

.image {
  height: calc(100vh - 600px);
}

.text {
  height: 220px;
}

.buttons button {
  background-color: #ff4d79;
  color: #fff;
  padding: 10px 30px;
  border: none;
  border-radius: 10px;
  margin: 10px;
  font-size: 26px;
  cursor: pointer;
  position: relative;
  font-family: serif; /* Change to a romantic cursive font */
}

.buttons button:hover {
  background-color: #7c1f37;
}

.buttons {
  display: flex;
  justify-content: center;
  flex-direction: row;
}

#no-button {
}

.hidden-message {
  display: none;
  margin-top: 20px;
}

.button {
  font-family: "Courier New", Courier, monospace;
}

@media (min-width: 576px) {
  .pp {
    font-size: 40px;
  }

  .hh {
    font-size: 60px;
  }
}

// Medium devices (tablets, 768px and up)
@media (min-width: 768px) {
  .pp {
    font-size: 40px;
  }

  .hh {
    font-size: 60px;
  }
}

// Large devices (desktops, 992px and up)
@media (min-width: 992px) {
  .pp {
    font-size: 40px;
  }

  .hh {
    font-size: 60px;
  }
}

// X-Large devices (large desktops, 1200px and up)
@media (min-width: 1200px) {
  .pp {
    font-size: 40px;
  }

  .hh {
    font-size: 60px;
  }
}
