# To-do-list
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    /* #363532, rgb(88, 111, 112) */
    align-items: center;
    display: flex;
    flex-direction: column;
    font-family: 'Work Sans', sans-serif;
    min-height: 100vh;
    padding-top: 3%;
}

/* Body light or darker themes */
.standard {
    background-image: linear-gradient(100deg, #575656, #062e3f);
    color: #ffdfdb;
    transition: 0.3s linear;
    overflow: hidden;
}

.light {
    background-image: linear-gradient(100deg, #d4f1ff, #ffffff);
    color: #1a150e;
    transition: 0.3s linear;
}

.darker {
    background-image: linear-gradient(100deg, #001214, #001f29);
    color: white;
    transition: 0.3s linear;
}

#header, #form, #datetime {
    margin: 0 1rem;
    min-height: 10vh;
    width: 100%;
}

#header {
    align-items: center;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    font-size: 3rem;
    min-height: 25vh;
    width: 100%;
}

/* Theme buttons div */
.flexrow-container {
    align-items: center;
    align-self: flex-end;
    display: flex;
    justify-content: space-around;
    margin-right: 3%;
}

.theme-selector {
    border: 1px solid #d1dae3;
    border-radius: 100%;
    height: 35px;
    margin: 0 8px;
    transition: tranform 150ms ease-in-out, box-shadow 200ms ease-in-out;
    width: 35px;
}

.theme-selector:hover { 
    box-shadow: white 0 0 8px;
    cursor: pointer;
}

.theme-selector:active {
    transform: scale(0.95);
}

.standard-theme {
    background-image: linear-gradient(100deg, #575656, #062e3f);
}

.light-theme {
    background-image: linear-gradient(100deg, #d4f1ff, #ffffff);
}

.darker-theme {
    background-image: linear-gradient(100deg, #001214, #001f29);
}

/* Animation */
#title {
    border-right: solid 3px rgba(0, 0, 0, 0.75);
    white-space: pre;
    overflow: hidden;     
    letter-spacing: 0.20rem;
    margin-top: 50px;
    margin-bottom: 20px;
    max-width: 480px;
  }
  
  /* Animation */
#title {
    animation: animated-text 2s steps(11,end) 0.5s 1 normal both,
        animated-cursor 750ms steps(11,end) infinite;
  }

#title.darker-title {
    animation: animated-text 2s steps(11,end) 0.5s 1 normal both, darker-animated-cursor 750ms steps(11,end) infinite;
}
  
  /* text animation */
  
  @keyframes animated-text{
    from{width: 0%;}
    to{width: 480px;}
  }
  
  /* cursor animations */
  
  @keyframes animated-cursor{
    from{border-right-color: rgba(0, 0, 0, 0.75);}
    to{border-right-color: transparent;}
  }

  @keyframes darker-animated-cursor {
    from{border-right-color: #01394c;}
    to{border-right-color: transparent;}
  }

form {
    display: flex;
    font-size: 1.7rem;
    justify-content: center;
    margin: 15px 0;
    padding: 0.8rem;
    width: 100%;
}

form input {
    padding: 10px;
    font-size: 17px;
    border: none;
    outline: none;
    /* border-radius: 15; */
    border-top-left-radius: 17px;
    border-bottom-left-radius: 17px;
    max-width: 500px;
    transition: background-color 200ms ease-in-out;
    width: 100%;
}

/* Input themes */
form input.standard-input {
    background-color: #181a1a;
    color: rgb(247, 226, 223);
}


form input.light-input {
    background-color: #AEB1B4;
    color: #1a150e;
}

form input.light-input::placeholder {
    color: #1a150e;
    opacity: 0.7;
}

form input.darker-input {
    background-color: #01394c;
    color: white;
}

form input.darker-input::placeholder {
    color: white;
    opacity: 0.7;
}

form input:hover {
    cursor: text;
}

form input.standard-input:hover {
    background-color: rgb(0, 0, 0);
}

form input.light-input:hover {
    background-color: #919699;
}

form input.darker-input:hover {
    background-color: #013141;
}

button {
    border: none;
    outline: none; 
    transition: box-shadow 200ms ease, background-color 200ms ease-in-out;
}

button:hover {
    cursor: pointer;
}

/* Button themes */
button.standard-button {
    background-color: rgb(247, 226, 223);
    color: rgb(0, 0, 0);
}

button.standard-button:hover {
    background-color: white;
    box-shadow: #fff8 0 0 10px;
}

button.light-button {
    background-color: white;
    color: #1a150e;
}

button.light-button:hover {
    background-color: #f0f0f0;
}

button.darker-button {
    background-color: #002837;
    color: white;
}

button.darker-button:hover {
    background-color: #001f29;
}

form button {
    padding: 10px;
    font-size: 17px;
    border-top-right-radius: 15px;
    border-bottom-right-radius: 15px;
    min-width: 100px;
}

#myUnOrdList {
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 1200px;
}

.todo-list {
    min-width: 25%;

    /* To remove the bullets of unordered list */
    list-style: none;
}

.todo {
    margin: 1rem;
    /* background: rgb(247, 226, 223); */
    /* color: black; */
    font-size: 19px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.25em 0.5em;
    border-radius: 30px;
    transition: background-color 200ms ease-in-out;
}

/* Items themes */
.standard-todo {
    background-color: rgb(26, 27, 27);
}

.light-todo {
    background-color:#AEB1B4;
}

.darker-todo {
    background-color: #01394c;
}

.todo li{
    padding: 7px;
    /* word-wrap: break-word; */
    /* flex-wrap: wrap; */
    font-size: 20px;
    flex: 1; /* To push the trash and the check button to the right */
    border-radius: 30px;

    /* wraps the links */
    overflow-wrap: anywhere;
}

.check-btn, .delete-btn {
    font-size: 19px;
    cursor: pointer;
    width: 2em;
    height: 2em;
    border-radius: 80%;
    margin: 0 5px;
}

.todo-item {
    padding: 0rem 0.5rem;
}

.fa-trash, .fa-check { 
    pointer-events: none;
}


.completed {
    transition: 0.2s;
    text-decoration: line-through;
    opacity: 0.5;
}

.fall {
    transition: 0.5s;
    transform: translateY(45rem) rotateZ(45deg);
    opacity: 0;
}

/* Responsive design */
@media only screen and (max-width: 1000px) {
    .flexrow-container {
        align-self: unset;
        margin-right: 0;
    }
}

@media only screen and (max-width: 800px) {
    #header {
        font-size: 2rem;
    }

    #title {
        animation: 
            animated-text 3s steps(16,end) 0.5s 1 normal both,
            animated-cursor 750ms steps(16,end) infinite;
        margin-bottom: 10px;
        margin-top: 30px;
        max-width: 330px;
    }
}

@media only screen and (max-width: 400px) {
    #header {
        font-size: 1.5rem;
    }

    #title {
        animation: 
            animated-text 3.5s steps(16,end) 0.5s 1 normal both,
            animated-cursor 750ms steps(16,end) infinite;
        max-width: 255px;
    }
}

@media only screen and (max-width: 400px) {
    form {
        align-items: center;
        flex-direction: column;
    }

    form input {
        border-radius: 17px;
    }

    form button {
        border-radius: 15px;
        margin-top: 15px;
        width: 50%;
    }
    form > button.light-button {
        box-shadow: 0 0 5px lightgray;
    }
}
