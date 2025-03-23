<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="utf-8" />
    <meta name="description" content="@feelthisray - Script HTML by Feeldream Repl Co">
    <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1, maximum-scale=1" />
    <title>htmlku.com/pesanuntukmu</title>
    <link href="https://fonts.googleapis.com/css2?family=Handlee&display=swap" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Patrick+Hand&family=Sriracha&family=Itim&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Berkshire+Swash&display=swap" rel="stylesheet">
    <script src="https://unpkg.com/typeit@8.7.0/dist/index.umd.js"></script>
    <link rel="stylesheet" href="https://htmlku.com/pesanuntukmu/style.css">
    <style>
        /* General styles for the button container */
        .button-container {
            text-align: center;
            margin-top: 30px;
            margin-bottom: 50px;
        }

        /* Styling for buttons */
        .button-container button {
            font-size: 18px;
            padding: 10px 20px;
            margin: 0 10px;
            cursor: pointer;
            background-color: #ff5e5e;
            color: white;
            border: none;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        /* Hover effect */
        .button-container button:hover {
            background-color: #ff1a1a;
            transform: scale(1.05);
        }

        /* Popup styles with 50% transparency */
        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: rgba(255, 94, 94, 0.5); /* 50% opacity */
            padding: 20px 40px;
            border-radius: 12px;
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.3);
            text-align: center;
            z-index: 1000;
            max-width: 400px;
            width: 100%;
            border: 2px solid white; /* White border */
        }

        /* White text in popup */
        .popup p {
            color: white;
        }

        .popup table {
            width: 100%;
            margin-top: 20px;
        }

        .popup table, .popup th, .popup td {
            border: 1px solid #ddd;
            border-collapse: collapse;
        }

        .popup th, .popup td {
            padding: 10px;
            text-align: center;
        }

        /* Close popup button */
        .popup button {
            background-color: red;
            color: white;
            padding: 12px 20px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        .popup button.clicked {
            background-color: #ff66b3; /* Light pink after click */
        }

        .popup button:hover {
            background-color: #ff1a1a;
        }

        /* Warning popup */
        .warning-popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: rgba(255, 0, 0, 0.7); /* Red background with some transparency */
            padding: 20px 40px;
            border-radius: 12px;
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.3);
            text-align: center;
            z-index: 2000; /* Increased z-index to ensure it's in front of other popups */
            max-width: 400px;
            width: 100%;
            border: 2px solid white;
        }

        .warning-popup p {
            color: white;
            font-size: 20px;
            font-weight: bold;
        }

        .warning-popup button {
            background-color: #ffcc00; /* Yellow background */
            color: black;
            padding: 12px 20px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        .warning-popup button:hover {
            background-color: #ff9900;
        }

        /* Watermark styles */
        .watermark {
            position: fixed;
            bottom: 10px;  /* Position 10px from the bottom */
            right: 10px;   /* Position 10px from the right */
            font-size: 16px; 
            color: rgba(255, 255, 255, 0.5);  /* White color with some transparency */
            font-family: 'Berkshire Swash', cursive; /* Choose a cursive font */
            z-index: 9999; /* Make sure it's above other content */
            pointer-events: none; /* Ensure watermark doesn't interfere with other elements */
        }
    </style>
</head>
<body>
    <div class="overlay">
        <div class="cover">
            <p>Sentuh untuk Mulai</p>
            <div class="awalan">
                <svg class='line' fill='none' xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'>
                    <g transform='translate(2.000000, 2.000000)'>
                        <path d='M9.27542857,0.714285714 C14.0030476,0.714285714 17.836381,4.54666667 17.836381,9.2752381 C17.836381,14.0038095 14.0030476,17.8361905 9.27542857,17.8361905 C4.54685714,17.8361905 0.71447619,14.0038095 0.71447619,9.2752381 C0.71447619,4.54666667 4.54685714,0.714285714 9.27542857,0.714285714 Z'></path>
                        <path d='M17.8989524,16.487619 C18.678,16.487619 19.3094286,17.12 19.3094286,17.8980952 C19.3094286,18.6780952 18.678,19.3095238 17.8989524,19.3095238 C17.1199048,19.3095238 16.4875238,18.6780952 16.4875238,17.8980952 C16.4875238,17.12 17.1199048,16.487619 17.8989524,16.487619 Z'></path>
                    </g>
                </svg>
                <label style="font-size:16px">satrio_adty.com/pesanuntukmu</label>
            </div>
        </div>
    </div>

    <div id="bodyblur">
        <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhqjeQ7NlN92_dwtxYNCtLFpPe9lMt_zffq06EPVGF53aqoeBoy3wNq4j6BSPtc8f_ciXlX07xs1mSjgaSpXZUwpYXg2JJxl4D1iVjpdspfHiScLSgqfKTJIHtH4OmpG8Gk1Br8sByutqxjx-s1H-gY8LQCLjWPWyqQ6SsJFac-IGfZq05gxRp3CemyatUy/s1200/1000322477.jpg" id="wallpaper"/>
        <div id="thisblur"></div>
    </div>

    <!-- Audio element for sound -->
    <audio src="sound1.mp3" id="linkmp3"></audio>

    <div id="envwrap" class="envlope-wrapper">
        <div id="envelope" class="close">
            <div class="wax-seal"></div>
            <div class="front flap"></div>
            <div class="front pocket"></div>
            <div class="letter">
                <div class="letter-corner corner-tl"></div>
                <div class="letter-corner corner-br"></div>
                <div class="message">
                    <p>Alooo Kamuu! 🩷</p>
                    <p>......</p>
                </div>
            </div>
            <div class="hearts">
                <div class="heart a1"></div>
                <div class="heart a2"></div>
                <div class="heart a3"></div>
            </div>
            <div class="sparkles">
                <div class="sparkle s1"></div>
                <div class="sparkle s2"></div>
                <div class="sparkle s3"></div>
            </div>
        </div>
    </div>
    <div class="reset">
        <button id="open">Buka Surat 🫰</button>
    </div>

    <div class="stiker">
        <img id="main-stiker" src="https://htmlku.com/0/panda/pusn.gif" />
        <img id="stikerAlt1" src="https://htmlku.com/0/panda/muah.gif" />
    </div>

    <div class="container" id="container">
        <p class="titleC"><b>Alooo Kamuu! 🫣😇</b></p>
        <script>teksAnimasi = [
            "selamat hari raya idulfitri kawann🥱",
            "<br><i>Every day, I’m so proud of you</i>. di hari yang istimewa ini aku mau minta maaf🙄, selama satu tahun lalu banyak salah, yaa entah itu di sengaja atau tidak. jujur sii aku ga pinter merangkai kata, intinya mulai hari ini kita nol nol yaa😁",
            "<br><b>Terakhir,</b><br>aku beneran minta maaf loh, ini GA BOHONG!<br>maaf yaa 💐",
            "<br><i class='fontAlt'>thankkkkk youuu</i> 😎",
        ];</script>
        <p class="messageC"></p>

        <!-- Add the buttons here directly below the message content -->
        <div class="button-container">
            <button id="maafinBtn">Di Maafin</button>
            <button id="gakDimaafinBtn" id="movingButton">Gak Dimaafin</button>
        </div>
    </div>

    <!-- Popup that will be displayed when 'Di Maafin' is clicked -->
    <div class="popup" id="popup">
        <table>
            <tr>
                <th>Terimakasih!</th>
            </tr>
            <tr>
                <td>Terimakasih telah memaafkan aku!</td>
            </tr>
        </table>
        <button id="closePopup">Tutup</button>
    </div>

    <!-- New popup with "Ngga ada THR yaa lagi ga ada uang nihh" message -->
    <div class="popup" id="noThrPopup">
        <table>
            <tr>
                <th>Maaf!</th>
            </tr>
            <tr>
                <td>Ngga ada THR yaa, lagi ga ada uang nihh!</td>
            </tr>
        </table>
        <button id="closeNoThrPopup">Tutup</button>
    </div>

    <!-- Warning popup for "Gak Dimaafin" -->
    <div class="warning-popup" id="warningPopup">
        <p>Harus Dimaafin! 😓</p>
        <button id="closeWarningPopup">Selesai</button>
    </div>

    <!-- Watermark -->
    <div class="watermark">
        satrio_adty
    </div>

    <script>
        // Handle "Di Maafin" Button click
        document.getElementById('maafinBtn').addEventListener('click', function() {
            // Play the audio when the button is clicked
            var audio = document.getElementById('linkmp3');
            audio.play(); // This will play the audio

            // Hide the container and buttons
            document.getElementById('container').style.display = 'none';
            document.getElementById('popup').style.display = 'block'; // Show popup
        });

        // Handle "Gak Dimaafin" Button click
        document.getElementById('gakDimaafinBtn').addEventListener('click', function() {
            // Hide the container and show the warning popup
            document.getElementById('container').style.display = 'none';
            document.getElementById('warningPopup').style.display = 'block';
        });

        // Close the popup and show "Ngga ada THR" popup
        document.getElementById('closePopup').addEventListener('click', function() {
            document.getElementById('popup').style.display = 'none';
            document.getElementById('noThrPopup').style.display = 'block'; // Show "Ngga ada THR" popup
        });

        // Close the "Ngga ada THR" popup when clicked
        document.getElementById('closeNoThrPopup').addEventListener('click', function() {
            document.getElementById('noThrPopup').style.display = 'none';
        });

        // Close the warning popup and return to container
        document.getElementById('closeWarningPopup').addEventListener('click', function() {
            document.getElementById('warningPopup').style.display = 'none';
            document.getElementById('container').style.display = 'block'; // Show the container again
        });
    </script>

    <script src="https://htmlku.com/pesanuntukmu/script.js"></script>
</body>
</html>
