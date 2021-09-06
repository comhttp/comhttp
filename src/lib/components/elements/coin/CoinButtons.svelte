<a href="https://com-http.download" class="flex flex-col px-4 py-2 huge button rounded-lg blue font-title text-2xl text-invert items-center"><i class="fas fa-cloud-download-alt mr-3 text-9xl"></i>download</a>
<a href="https://com-http.directory" class="flex flex-col px-4 py-2 huge button rounded-lg green font-title text-2xl items-center text-invert"><i class="fas fa-folder mr-2 text-9xl"></i>directory</a>

<a href="https://com-http.download" class="px-4 py-2 med button rounded-lg blue font-title text-xl text-invert items-center "><i class="fas fa-cloud-download-alt mr-3"></i>download</a>
<a href="https://com-http.directory" class="px-4 py-2 med button rounded-lg green font-title text-xl items-center text-invert"><i class="fas fa-ambulance mr-2"></i>directory</a>
<a href="https://com-http.games" class="px-4 py-2 med button rounded-lg orange font-title text-md items-center text-invert "><i class="fas fa-gamepad mr-2"></i>games</a>
<a href="https://com-http.trade" class="px-4 py-2 med button rounded-lg red font-title text-md items-center text-invert"><i class="fas fa-ambulance mr-2"></i>trade</a>
<a href="https://com-http.exchange" class="px-4 py-2 med button rounded-lg purple font-title text-md items-center text-invert"><i class="fas fa-ambulance mr-2"></i>exchange</a>
<a href="https://com-http.tools" class="px-4 py-2 med button rounded-lg purple font-title text-md items-center text-invert"><i class="fas fa-tools mr-2"></i>tools</a>

<a href="https://com-http.help" class="px-4 py-2 button rounded-lg items-center font-title text-md"><i class="fas fa-users-cog-wired mr-2"></i>help</a>
<a href="https://com-http.info" class="px-4 py-2 button rounded-lg items-center font-title text-md"><i class="fas fa-network-wired mr-2"></i>info</a>
<a href="https://com-http.live" class="px-4 py-2 button rounded-lg items-center font-title text-md"><i class="fas fa-server-wired mr-2"></i>live</a>
<a href="https://com-http.network" class="px-4 py-2 button rounded-lg items-center font-title text-md"><i class="fas fa-network-wired mr-2"></i>network</a>
<a href="https://com-http.news" class="px-2 button rounded-lg items-center font-title text-md"><i class="fas fa-network-wired mr-2"></i>news</a>
<a href="https://com-http.social" class="px-2 button rounded-lg items-center font-title text-md"><i class="fas fa-hashtag mr-2"></i>social</a>
<a href="https://com-http.today" class="px-2 button rounded-lg items-center font-title text-md"><i class="fas fa-broadcast-tower mr-2"></i>today</a>


<style>
    :root {
        --blue: #80a8cf;
        --light-blue: #80a8cf;
        --dark-blue: #305880;
        --green-blue: #308080;
        --green-blue-light: #80a8a8;
        --green: #30CF30;
        --orange: #cf8030;
        --yellow: #CFCF30;
        --red: #CF3030;
        --purple: #803080;
        --dark: #303030;
        --light: #cfcfcf;
        --dark-gray:#424242;
        --gray:#888888;
        --light-gray:#bdbdbd;
        --text-invert:#cfcfcf;
        --lighter:#fefefe;

        --border-light: rgba(255,255,255,.62);
        --border-dark: rgba(0,0,0,.38);

        --trans-light: rgba(255,255,255,.64);
        --trans-dark: rgba(0,0,0,.62);
        --trans-dark-gray: rgba(48,48,48,0.62);
        --trans-gray: rgba(48,48,48,.38);

    }
    .button{
        display: flex;
        transition: all 111ms ease-in;
        border: none;

        cursor: pointer;
        font-family: 'splendid';
        color:var(--text-invert);
        text-align:center;
        transition: box-shadow 111ms ease-in;
        letter-spacing:2px;
    }

    .med.button{
        background: var(--trans-dark);
        color:var(--text-invert);
        text-align:center;
        letter-spacing:2px;
    }

    .huge.button{
        color:var(--text-invert);
        text-align:center;
        letter-spacing:2px;
        text-shadow:  0px 0px 0px var(--dark), 0px 0px 0px var(--light);
    }

    .button:hover{
        color: var(--lighter);
        transition: all 99ms ease-in;

    }
    .huge.button:hover{
        color: var(--lighter);
        transition: all 99ms ease-in;
        transition: text-shadow 77ms ease-in;
        text-shadow:  1px 3px 1px var(--dark), 1px 3px 1px var(--light);
    }
    .huge.button.blue{
        color: var(--blue);
        text-shadow:  1px 3px 1px var(--dark), 1px 3px 1px var(--blue);
    }
    .huge.button.blue:hover{
        text-shadow:  0px 0px 0px var(--dark), 0px 0px 0px var(--blue);
    }
    .huge.button.green{
        color: var(--green);
        text-shadow:  1px 3px 1px var(--dark), 1px 3px 1px var(--green);
    }
    .huge.button.green:hover{
        text-shadow:  0px 0px 0px var(--dark), 0px 0px 0px var(--green);
    }
    .med.button:hover{
        transition: box-shadow 77ms ease-in;
        box-shadow:  inset 0 5px 10px  var(--dark),inset 0 99px 0 var(--light);
    }
    .med.button.orange{
        box-shadow:inset 0 0px 0px  var(--dark), inset 0 5px 0 var(--orange);
    }
    .med.button.orange:hover{
        box-shadow:  inset 0 5px 10px  var(--dark),inset 0 99px 0 var(--orange);
    }
    .med.button.red{
        box-shadow: inset 0 0px 0px  var(--dark), inset 0 5px 0 var(--red);
    }
    .med.button.red:hover{
        box-shadow:  inset 0 5px 10px  var(--dark), inset 0 99px 0 var(--red);
    }
    .med.button.green{
        box-shadow:inset 0 0px 0px  var(--dark), inset 0 5px 0 var(--green);
    }
    .med.button.green:hover{
        box-shadow:  inset 0 5px 10px  var(--dark),inset 0 99px 0 var(--green);
    }
    .med.button.blue{
        box-shadow:inset 0 0px 0px  var(--dark), inset 0 5px 0 var(--blue);
    }
    .med.button.blue:hover{
        box-shadow:  inset 0 5px 10px  var(--dark),inset 0 99px 0 var(--blue);
    }
    .med.button.light-blue{
        box-shadow:inset 0 0px 0px  var(--dark), inset 0 5px 0 var(--light-blue);
    }
    .med.button.light-blue:hover{
        box-shadow:  inset 0 5px 10px  var(--dark),inset 0 99px 0 var(--light-blue);
    }

    .med.button.purple{
        box-shadow:inset 0 0px 0px  var(--dark), inset 0 5px 0 var(--purple);
    }
    .med.button.purple:hover{
        box-shadow:  inset 0 5px 10px  var(--dark),inset 0 99px 0 var(--purple);
    }
    .med.button.yellow{
        box-shadow:inset 0 0px 0px  var(--dark), inset 0 5px 0 var(--yellow);
    }
    .med.button.yellowblue:hover{
        box-shadow:  inset 0 5px 10px  var(--dark),inset 0 99px 0 var(--yellow);
    }
</style>
