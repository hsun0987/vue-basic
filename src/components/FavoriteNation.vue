<template>
    <div>
        <h1>좋아하는 나라</h1>
    </div>
    <div class="card-list">
        <a @click="countUP(0)" href="#" class="card-item">
            <h3>한국</h3>
            <img src="https://i.namu.wiki/i/aLO9MpbKUYhqPEgbSnOUo1Wku1JcNcwud4trmFKZJpro_e442JAx8WUDfsFwbe4cPE4cOs9bM_eXEToMaVIp9BjKMA859W0KWp2F61Ob03kMb1Equ38qbs343neuZ42HiPOEqzy1b8WTMyfQIc2odQ.svg" alt="Card Image">
            <h3 class="count">클릭수 : {{ click[0] }}</h3>
        </a>
        
        <a @click="countUP(i+1)" v-for="(nation, i) in nations" :key="nation" href="#" class="card-item">
            <h3>{{ nation }}</h3>
            <img :src="flags[i]" alt="Card Image">
            <h3 class="count">클릭수 : {{ click[i+1] }}</h3>
        </a>
    </div>
</template>
<script>
export default {
  data() {
    return {
        nations : ['미국', '영국', '독일'],
        flags : ['https://i.namu.wiki/i/Dj_I51HG6tAfOvWyq7GV0RsxqKuRIB59GKetL-FebRS0ydGqU6K_XSoszMrVnY4L54PxXdkzF36O7gKjU7FSNA.svg', 'https://i.namu.wiki/i/WNw8JiSr4x94S6McVTaDj70J_VmBtOPAV6NzP5FBOyRXD7E7nalYplrZeyGtsKq8KyAezsTqtS3Uec3jchRRUw.svg', 'https://i.namu.wiki/i/KiykE29mubKM3qGGIT5i3xubJFilCDaC-6R0j4WUCbTVYIeHYqw8zAhidpwGhlBI7T2zHpdS4tjqSgvrcITPEw.svg'],
        click : [0, 0, 0, 0]
    }
  },
  methods : {
    countUP(idx){
        this.click[idx]++;
    }
  }
}
</script>
<style scoped>
/* Importing Google font - Open Sans */
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;500;600;700&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Open Sans', sans-serif;
}

body {
    background: #ecececdb;
}

.card-list {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    max-width: 1250px;
    margin: 150px auto;
    margin-top: 0px;
    margin-bottom: 0px;
    padding: 20px;
    gap: 20px;
}

.card-list .card-item {
    background: #fff;
    padding: 50px;
    border-radius: 8px;
    box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.04);
    list-style: none;
    cursor: pointer;
    text-decoration: none;
    border: 2px solid transparent;
    transition: border 0.5s ease;
}

.card-list .card-item:hover {
    border: 2px solid #000;
}

.card-list .card-item img {
    margin-top: 20px;
    width: 100%;
    aspect-ratio: 16/9;
    border-radius: 8px;
    object-fit: cover;
}

.card-list span {
    display: inline-block;
    background: #F7DFF5;
    margin-top: 32px;
    padding: 8px 15px;
    font-size: 0.75rem;
    border-radius: 50px;
    font-weight: 600;
}
.card-item h3 {
    color: #000;
    font-size: 1.438rem;
    /* margin-top: 28px; */
    font-weight: 600;
    text-align: center;
    
}

.count {
    background-color: yellowgreen;
}
.capital {
    background-color: yellow;
}

@media (max-width: 1200px) {
    .card-list .card-item {
        padding: 15px;
    }
}

@media screen and (max-width: 980px) {
    .card-list {
        margin: 0 auto;
    }
}
</style>