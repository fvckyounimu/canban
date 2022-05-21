<template>
  <h1 class="container-fluid">
    Tudor
  </h1>
  <div class="main inline">
    <div class="cards-column">
      <div class="header-name">
        <div>
          <img src="./images/todo.png">
        </div>
        <p>to do</p>
      </div>
      <template
          v-for="(card, id) in cards.todo"
          :key="id"
      >
        <div class="card">
          <h2 class="card-title">{{ card.title }}</h2>
          <div class="figure-block">
            <figure class="to-do-square" />
          </div>
          <div class="description-block">
            <p class="description">
              {{card.description}}
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">{{card.date.getDate()}}.{{card.date.getMonth()}}.{{card.date.getFullYear()}}</p>
          </div>
        </div>
      </template>
    </div>
    <div class="cards-column">
      <div class="header-name">
        <case-icon></case-icon>
        <p>in work</p>
      </div>
      <template
          v-for="(card, id) in cards.in_work"
          :key="id"
      >
        <div class="card">
          <h2 class="card-title">{{ card.title }}</h2>
          <div class="figure-block">
            <figure class="to-do-square" />
          </div>
          <div class="description-block">
            <p class="description">
              {{card.description}}
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">{{card.date.getDate()}}.{{card.date.getMonth()}}.{{card.date.getFullYear()}}</p>
          </div>
        </div>
      </template>
    </div>
    <div class="cards-column">
      <div class="header-name new">
        <div>
          <img src="./images/done.png">
        </div>
        <p>done</p>
      </div>
      <template
          v-for="(card, id) in cards.done"
          :key="id"
      >
        <div class="card">
          <h2 class="card-title">{{ card.title }}</h2>
          <div class="figure-block">
            <figure class="to-do-square" />
          </div>
          <div class="description-block">
            <p class="description">
              {{card.description}}
            </p>
          </div>
          <div class="deadline-block">
            <p class="deadline">{{card.date.getDate()}}.{{card.date.getMonth()}}.{{card.date.getFullYear()}}</p>
          </div>
        </div>
      </template>
    </div>
  </div>
</template>

<script>
import caseIcon from './components/icons/caseIcon.vue'

export default {
  components: {
    caseIcon
  },
  data() {
    return {
      cards: {
        todo: [
          {
            title: 'Create a design for canban task-site',
            description: 'Create a design for canban task-site',
            date: new Date()
          },
          {
            title: 'Creating UI',
            description: 'Create a design for canban task-site',
            date: new Date()
          }
        ],
        in_work: [
          {
            title: 'Creating UI',
            description: 'Create a design for canban task-site',
            date: new Date()
          },
          {
            title: 'Creating UI',
            description: 'Create a design for canban task-site',
            date: new Date()
          }
        ],
        done: [
          {
            title: 'Creating UI',
            description: 'Create a design for canban task-site',
            date: new Date()
          },
          {
            title: 'Creating UI',
            description: 'Create a design for canban task-site',
            date: new Date()
          },
          {
            title: 'Creating UI',
            description: 'Create a design for canban task-site',
            date: new Date()
          }
        ]
      }
    }
  },
}
</script>

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
  margin-block-end: 0;
  margin-block-start: 0;
}

.main {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 50px;
}

.cards-column {
  display: flex;
  flex-direction: column;
  grid-row-gap: 50px;
}

.card{
  position: relative;
  justify-content: space-between;
  flex-direction: row;
  flex-wrap: wrap;
  vertical-align: top;
  border-radius: 15px;
  background-color: var(--main-card-color);
  padding: 10px;
  width: 100%;
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

.figure-block, .header-name{
  position: absolute;
  top: 20px;
  right: 20px;
}

.header-name {
  display:flex;
  height: 50px;
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

.card-title {
  max-width: 70%;
}

.deadline-block {
  display: flex;
  width: 100%;
  justify-content: flex-end;
}
</style>
