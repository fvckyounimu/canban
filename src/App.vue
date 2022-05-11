<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <body>
    <div class="container-fluid">
      <h1>Tudor</h1>
    </div>
    <div class="main inline">
      <div class="left-block">
        <div class="header-name">
          <div>
            <img src="./images/todo.png">
          </div>
          <p>to do</p>
        </div>
        <div class="to-do card">
          <h2>Creating UI</h2>
          <div class="figure-block">
            <figure class="to-do-square" />
          </div>
          <div class="description-block">
            <p class="description">
              Create a design for canban task-site
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">22.02.22</p>
          </div>
        </div>
        <div class="to-do card">
          <h2>Creating UI</h2>
          <div class="figure-block">
            <figure class="to-do-square" />
          </div>
          <div class="description-block">
            <p class="description">
              Create a design for canban task-site
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">22.02.22</p>
          </div>
        </div>
        <div class="to-do card">
          <h2>Creating UI</h2>
          <div class="figure-block">
            <figure class="to-do-square" />
          </div>
          <div class="description-block">
            <p class="description">
              Create a design for canban task-site
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">22.02.22</p>
          </div>
        </div>
      </div>
      <div class="space"></div>
      <div class="content">
        <div class="header-name">
          <div>
            <img src="./images/inwork.png">
          </div>
          <p>in work</p>
        </div>
        <div class="in-work card">
          <h2>Creating UI</h2>
          <div class="figure-block">
            <figure class="in-work-square" />
          </div>
          <div class="description-block">
            <p class="description">
              Create a design for canban task-site
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">22.02.22</p>
          </div>
        </div>
        <div class="in-work card">
          <h2>Creating UI</h2>
          <div class="figure-block">
            <figure class="in-work-square" />
          </div>
          <div class="description-block">
            <p class="description">
              Create a design for canban task-site
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">22.02.22</p>
          </div>
        </div>
        <div class="in-work card">
          <h2>Creating UI</h2>
          <div class="figure-block">
            <figure class="in-work-square" />
          </div>
          <div class="description-block">
            <p class="description">
              Create a design for canban task-site
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">22.02.22</p>
          </div>
        </div>
      </div>
      <div class="space"></div>
      <div class="right-block">
        <div class="header-name new">
          <div>
            <img src="./images/done.png">
          </div>
          <p>done</p>
        </div>
        <div class="done card">
          <h2>Creating UI</h2>
          <div class="figure-block">
            <figure class="done-square" />
          </div>
          <div class="description-block">
            <p class="description">
              Create a design for canban task-site
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">22.02.22</p>
          </div>
        </div>
        <div class="done card">
          <h2>Creating UI</h2>
          <div class="figure-block">
            <figure class="done-square" />
          </div>
          <div class="description-block">
            <p class="description">
              Create a design for canban task-site
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">22.02.22</p>
          </div>
        </div>
        <div class="done card">
          <h2>Creating UI</h2>
          <div class="figure-block">
            <figure class="done-square" />
          </div>
          <div class="description-block">
            <p class="description">
              Create a design for canban task-site
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">22.02.22</p>
          </div>
        </div>
      </div>
    </div>
  </body>
</template>

<style>
:root {
    --main-font-color: #4D4E50;
    --main-card-color: #CEE5ED;
    --to-do-color:#589FD3;
    --in-work-color:#DD93E9;
    --done-color:#1FA866;
}

html {
    font-family: 'Inter', sans-serif;
}


h1 {
    text-align: center;
    color: var(--main-font-color);
    font-family: Montserrat, sans-serif;
    font-weight: 800;
    font-size: 68px;
}

h2 {
    color: var(--main-font-color);
    font-family: Inter, Verdana, Geneva, Tahoma, sans-serif;
    font-weight: 700, bold;
    font-size: 40px;
    padding-left: 20px;
    padding-top: 20px;
    margin-block-end: 0;
    margin-block-start: 0;
}

.main {
    margin:0 auto; /* Центрируем блоки */
    width:100%; /* Задаем ширину 100%, чтобы сделать ее резиновой */
    max-width:1520px;
    margin-top: 5%;/* Устанавливаем максимальную ширину */
}
.inline div {
    display:inline-block; /* Делаем блоки по горизонтали */ /* Для FireFox 2, тот же самый, что и inline-block */
    vertical-align:top; /* Выравниваем их сверху */
    font-size:16px; /* Ставим дочкам размер шрифта, иначе примет значение родителя */
    /* Для IE 6 и IE 7, чтобы блоки были по горизонтали
    zoom: 1;
    *display: inline;
    */
}
div.inline {font-size:0;} /* Ставим родителю значение 0, чтобы убрать отступы у блоков*/
.left-block {
    width:30%; /*Задаем ширину в процентах чтобы сделать ее резиновой*/
    height:100%; /* Высота блока */
}

.space {
    width:5%; /*Задаем ширину в процентах чтобы сделать ее резиновой*/
    height:100%; 
}

.content {
    width:30%;
    height:100%;
}

.right-block {
    width:30%;
    height:100%;
}

.card{
    display:flex !important;
    justify-content: space-between;
    flex-direction: row;
    flex-wrap: wrap;
    vertical-align: top;
    border-radius: 15px;
    margin-bottom: 35px;
    background-color: var(--main-card-color);
    width: 100%;
    height: 240px;
}

figure {
    height: 42px;
    width:42px;
    border-radius: 15px;
    transform: rotate(45deg);
    margin: 0 !important;
}

.to-do-square {
    background-color: var(--to-do-color);
}

.in-work-square {
    background-color: var(--in-work-color);
}

.done-square {
    background-color: var(--done-color);
}

.figure-block, .header-name{
    padding-top: 20px;
    padding-right: 20px;
}

.header-name {
    display:flex !important;
    justify-content: flex-start;
    flex-direction: row;
    flex-wrap: wrap;
    vertical-align: top;
    margin-bottom: 40px;
}

.new {
    margin-bottom: 34px;
}

img {
    padding-left: 20px;
}

.header-name p {
    color: var(--main-font-color);
    font-family: Inter, Verdana, Geneva, Tahoma, sans-serif;
    font-weight: 700;
    font-size: 35px;
    margin: 0;
    margin-left: 30px;
}

p.description {
    color: var(--main-font-color);
    font-family: Inter, Verdana, Geneva, Tahoma, sans-serif;
    font-weight: 600;
    font-size: 28px;
    padding-top: 0;
    margin-left:20px;
}

div.description-block{
    padding-top: 0;
}


p.deadline {
    background-color: white;
    color: var(--main-font-color);
    font-family: Inter;
    font-size: 14px;
    font-weight:700;
    align-content: center;
    padding: 3px 13px 3px 13px;
    border-radius: 15px;
}

.deadline-block {
    margin-left: auto;
    margin-right: 20px;
    margin-bottom: 20px;
}
</style>
