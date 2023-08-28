
<template>
  <div class = "pagesettings">
    <header>
      <img src="https://shorturl.at/kBEIL" class="logo">
      <p class="logotext"><a  href="https://tenor.com/ru/view/walter-white-gif-25141525">Хлебные крошки</a> → <a  href="https://tenor.com/ru/view/walter-white-dancing-breaking-bad-gif-26451281">Хлебные крошки</a> → <a  href="https://tenor.com/ru/view/walter-white-gif-25141525">Хлебные крошки</a></p>
      <p class="logotext1"> Подписки «Клерка»</p>
      
      <!-- отдельный список вкладок -->
    <ul class="logomenu">
     <li>
        <input type='radio' value='1' name='radio' id='radio1' checked class="input1"/>
        <label for='radio1'>Рассылки</label>
      </li>
      <li>
        <input type='radio' value='2' name='radio'  id='radio2' class="input1"/>
        <label for='radio2'>Соцсети</label>
      </li>
      <li>
        <input type='radio' value='3' name='radio'  id='radio3' class="input1"/>
        <label for='radio3'>Мессенджеры</label>
      </li>
    </ul>
    </header>
  <main>
    
    <!-- Отдельный клас для верха main до блоков -->
    <div class="main1">
          <p class="uplabel">Выберите рассылки, которые подходят именно вам</p>
        <div class="strong">
          <input type="text" name="email" v-model="email" placeholder="Электронная почта" class="field1"/>
          <button v-on:click="sendinfo(), say('Вы успешно подписались на рассылки.')" class = "forsend">Подписаться</button>
        </div>

      <p class="textbut">      
        <label class="switch">
        <input type="checkbox" @click='checkAll()' v-model='isCheckAll'>
        <div class="slider round"></div>
        </label>&nbsp;&nbsp;Подписаться на все рассылки</p>
    </div>
    
      <!-- Отдельный класс для блоков -->
      <div class= "blocks">
        <!-- Block1 -->
        <div class="blockb">
          <img src="https://shorturl.at/AEFIM" class="imgspam">
          <p class="graytext">Перед рассветом</p>
          <p class="headtext">Утренний бухгалтер</p>
          <p class="graytext1">Самые важные новости и события за день.<br> Кратко, по делу, структурировано.</p>
          <p class="maintext"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M5.08471 11.6237L1.93292 8.47186C1.57839 8.11733 1.00389 8.11631 0.648103 8.46959C0.290537 8.82464 0.289516 9.40265 0.645826 9.75896L5.08471 14.1978L15.3586 3.92397C15.7128 3.56972 15.7128 2.99537 15.3586 2.64112C15.0044 2.28699 14.4303 2.28686 14.076 2.64082L5.08471 11.6237Z" fill="#00CC33"/>
          </svg>Новости для бухгалтеров, ИП и директора</p>
          <p class="maintext"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M5.08471 11.6237L1.93292 8.47186C1.57839 8.11733 1.00389 8.11631 0.648103 8.46959C0.290537 8.82464 0.289516 9.40265 0.645826 9.75896L5.08471 14.1978L15.3586 3.92397C15.7128 3.56972 15.7128 2.99537 15.3586 2.64112C15.0044 2.28699 14.4303 2.28686 14.076 2.64082L5.08471 11.6237Z" fill="#00CC33"/>
          </svg>Подборка статей за день</p>
          <p class="maintext">       
          <label class="switch">
          <input type="checkbox" value="1" v-model="lists" @change='updateCheckall()'>
          <div class="slider round"></div>
          </label> Уже получает 59 342 человек</p>

        </div>
          <!-- Block 2 -->
          <div class="blockb">
          <img src="https://shorturl.at/ksyCP" class="imgspam">
          <p class="graytext">После заката</p>
          <p class="headtext">Ночной бухгалтер</p>
          <p class="graytext1">Самая краткая газета о налогах и бухучете <br> в мире — современная рассылка для чтения. </p>
          <p class="maintext"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M5.08471 11.6237L1.93292 8.47186C1.57839 8.11733 1.00389 8.11631 0.648103 8.46959C0.290537 8.82464 0.289516 9.40265 0.645826 9.75896L5.08471 14.1978L15.3586 3.92397C15.7128 3.56972 15.7128 2.99537 15.3586 2.64112C15.0044 2.28699 14.4303 2.28686 14.076 2.64082L5.08471 11.6237Z" fill="#00CC33"/>
          </svg>Анализ, оценка и только самое главное</p>
          <p class="maintext"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M5.08471 11.6237L1.93292 8.47186C1.57839 8.11733 1.00389 8.11631 0.648103 8.46959C0.290537 8.82464 0.289516 9.40265 0.645826 9.75896L5.08471 14.1978L15.3586 3.92397C15.7128 3.56972 15.7128 2.99537 15.3586 2.64112C15.0044 2.28699 14.4303 2.28686 14.076 2.64082L5.08471 11.6237Z" fill="#00CC33"/>
          </svg>Лучшие комменты юзеров в обзоре</p>
          <p class="maintext">       
          <label class="switch">
          <input type="checkbox" value="2" v-model="lists" @change='updateCheckall()'>
          <div class="slider round"></div>
          </label> Уже получает 37 480 человек</p>
          </div>
          <!-- Block 3 -->
          <div class="blockb">
          <img src="https://shorturl.at/kFSY4" class="imgspam">
          <p class="graytext">Раз в две недели</p>
          <p class="headtext">Ножницы скидок</p>
          <p class="graytext1">Подборка самых выгодных и полезных  <br> спецпредложений от надежных компаний.</p>
          <p class="maintext"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M5.08471 11.6237L1.93292 8.47186C1.57839 8.11733 1.00389 8.11631 0.648103 8.46959C0.290537 8.82464 0.289516 9.40265 0.645826 9.75896L5.08471 14.1978L15.3586 3.92397C15.7128 3.56972 15.7128 2.99537 15.3586 2.64112C15.0044 2.28699 14.4303 2.28686 14.076 2.64082L5.08471 11.6237Z" fill="#00CC33"/>
          </svg>Акции и скидки от лидеров рынка</p>
          <p class="maintext"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M5.08471 11.6237L1.93292 8.47186C1.57839 8.11733 1.00389 8.11631 0.648103 8.46959C0.290537 8.82464 0.289516 9.40265 0.645826 9.75896L5.08471 14.1978L15.3586 3.92397C15.7128 3.56972 15.7128 2.99537 15.3586 2.64112C15.0044 2.28699 14.4303 2.28686 14.076 2.64082L5.08471 11.6237Z" fill="#00CC33"/>
          </svg>Те, кто подписался – экономят много денег </p>
          <p class="maintext">       
          <label class="switch">
          <input type="checkbox" value="3" v-model="lists" @change='updateCheckall()'>
          <div class="slider round"></div>
          </label> Уже получает 92 118 человек</p>
          </div>
          <!-- Block 4 -->
          <div class="blockb">
          <img src="https://shorturl.at/itBPY" class="imgspam">
          <p class="graytext">По мере появления анонсов</p>
          <p class="headtext">Чемодан вебинаров</p>
          <p class="graytext1">Подборка с анонсами бесплатных вебинаров <br> на самые топовые темы при участии экспертов.</p>
          <p class="maintext"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M5.08471 11.6237L1.93292 8.47186C1.57839 8.11733 1.00389 8.11631 0.648103 8.46959C0.290537 8.82464 0.289516 9.40265 0.645826 9.75896L5.08471 14.1978L15.3586 3.92397C15.7128 3.56972 15.7128 2.99537 15.3586 2.64112C15.0044 2.28699 14.4303 2.28686 14.076 2.64082L5.08471 11.6237Z" fill="#00CC33"/>
          </svg>Анализ, оценка и только самое главное</p>
          <p class="maintext"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M5.08471 11.6237L1.93292 8.47186C1.57839 8.11733 1.00389 8.11631 0.648103 8.46959C0.290537 8.82464 0.289516 9.40265 0.645826 9.75896L5.08471 14.1978L15.3586 3.92397C15.7128 3.56972 15.7128 2.99537 15.3586 2.64112C15.0044 2.28699 14.4303 2.28686 14.076 2.64082L5.08471 11.6237Z" fill="#00CC33"/>
          </svg>Никогда не пришлем платные вебинары</p>
          <p class="maintext">       
          <label class="switch">
          <input type="checkbox" value="4" v-model="lists" @change='updateCheckall()'>
          <div class="slider round"></div>
          </label> Уже получает 92 082 человек</p>
          </div>
      </div>
      </main>
        <footer>
          <p class="txtsmile">¯\_(ツ)_/¯</p>
        </footer>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'MyWebsite',
  data() {
    return {
      isCheckAll: false,
      lists: [],
      listss: ["1","2","3","4"],
      email: ''
    }
  },
  methods: {
    // для уведомления
    say(message) {
    	alert(message)
  	},
    // для для выборки всех
    checkAll: function() {
      this.isCheckAll = !this.isCheckAll;
      this.lists = [];
      if(this.isCheckAll){ // Check all
        for (var key in this.listss) {
          this.lists.push(this.listss[key]);
        }
      }
    },
    // для проверки всех подписок
    updateCheckall: function(){
      if(this.lists.length == this.listss.length){
         this.isCheckAll = true;
      }else{
         this.isCheckAll = false;
      }
    },
    // для отправки на апи
    async sendinfo(){
      console.log(this.email,this.lists)
      let result = await axios.post("http:/ourapi/api",{email: this.email, Podpiski: this.lists})
      console.log(result)
    },
  
  mounted() {
    // для белого цвета страницы
    document.body.style.background = 'white';
  }
}
}
</script>




<style scoped>
.pagesettings {
  /* настройки для всей страницы */
  margin-top: 48px;
  margin-bottom: 48px;
  margin-left: 328px;
  margin-right: 328px;
  justify-content: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  white-space: nowrap;
}
.logo {
  /* лого */
  display: block;
  margin-left: auto;
  margin-right: auto;  
  margin-top: 0px;
  height: 35px;
  width: 76px;
}
.logotext{
  margin: 0px 0px 0px 0px;
  /* для ссылок под лого */
  padding-top: 24px;
  font-family: Roboto;
  font-size: 13px;
  font-style: normal;
  font-weight: 400;
  line-height: 16px;
  color: var(--disabled, #999);
  text-align: center;
}
a {
  color: var(--disabled, #999);
}
.logotext1{
  margin: 0px 0px 0px 0px;
  /* для заголовка сайта */
  text-align: center;
  font-family: Roboto;
  font-size: 56px;
  font-style: normal;
  font-weight: 500;
  line-height: 72px; 
  letter-spacing: -0.56px;
  color: var(--base-primary, #000);
  padding-top: 24px;
}
.logomenu{
  margin: 0px 0px 2px 0px;
  /* для меню вкладок */
  display: flex;
  padding-top: 24px;
  justify-content: center;
  align-items: flex-start;
  align-self: stretch;
  color: var(--base-secondary, #666);
}
/* это все для меню вкладок */
ul {
    list-style: none;
    padding-bottom: 16px;
}
li {
    display: inline-block;
    margin-right: 15px;
}
.input1 {
    visibility:hidden;
}
label {
    cursor: pointer;

}
.input1:checked + label {
  padding-bottom: 16px;
  border-bottom:3px solid #5A8CF1;
  /* тут заканчивается меню вкладок */
}
main {
  background: #F5F5F8;
  justify-content: center;
  border-radius: 16px;
  width: auto;
  padding: 32px 24px 48px 24px;
}
.main1 {
  /* я поделил на 2 блока main и вот это для верхнего */
  /* display: flex; */
  /* align-items: flex-start;
  align-self: stretch; */
  padding: 48px 48px 0px 48px;
}
.textbut{
  color: var(--base-primary, #000);
  font-family: Roboto;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 20px;
  /* margin: 0px 0px 0px 0px; */
}
.uplabel {
  color: var(--base-primary, #000);
  text-align: center;
  font-family: Roboto;
  font-size: 24px;
  font-style: normal;
  font-weight: 500;
  line-height: 32px;
  letter-spacing: -0.24px;
  padding-bottom: 24px;
  margin: 0px 0px 0px 0px;
}
.strong {
  color: var(--base-secondary, #666);
  font-family: Roboto;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px; 
  height: 48px;
}

.field1 {   
  /* для емаила */
  display: flex;
  padding: 16px 0px 16px 16px;
  align-items: flex-start;
  flex: 1 0 0;
  width: 100%;
  height: auto;
  border-radius: 5px;
  white-space: nowrap;
  width: 80%;
  border: none;
  outline: none;
}
.forsend{
  /* кнопка для рассылки */
  display: flex;
  padding: 12px 24px;
  justify-content: center;
  align-items: center;
  gap: 8px;
  color: var(--base-primary, #FFF);
  font-family: Roboto;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
  border: #316FEE;
  border-radius: 100px;
  background: #316FEE;
  position:relative;
  left: 76%;
  bottom: 48px;
}
.switch {
  /* далее все для тогл кнопки */
  position: relative;
  display: inline-block;
  width: 32px;
  height: 16px;
  margin-top: 16px;
}

.switch input {
  display: none;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 16px;
  width: 16px;
  left: 0px;
  bottom: 0px;
  background-color: white;
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

input:checked + .slider {
  background-color: #316FEE;
}

input:focus + .slider {
  box-shadow: 0 0 1px #101010;
}

input:checked + .slider:before {
  -webkit-transform: translateX(16px);
  -ms-transform: translateX(16px);
  transform: translateX(16px);
}

.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
  /* это все для тогл кнопки */
}
.blocks {
  /* второй блок с блокам */
  display: grid;
  grid-template-columns: 420px 420px;
  gap: 24px;
}
.blockb {
  background-color: #FFF;
  border-radius: 16px;
  padding: 24px 24px 24px 24px;
}
/* далее настройки текста для блоков */
.graytext {
  color: var(--base-disabled, #999);
  font-family: Roboto;
  font-size: 13px;
  font-style: normal;
  font-weight: 400;
  line-height: 16px;
  margin-top: 0px;
  margin-bottom: 0px;
}
.graytext1 {
  color: var(--base-disabled, #666);
  font-family: Roboto;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 20px;
  padding-top: 8px;
  padding-bottom: 16px;
  margin-top: 0px;
  margin-bottom: 0px;
}
.headtext {
  color: var(--base-primary, #000);
  font-family: Roboto;
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: 28px;
  margin-top: 0px;
  margin-bottom: 0px;
}
.maintext {
  color: var(--base-primary, #000);
  font-family: Roboto;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 20px;
  margin-top: 0px;
  margin-bottom: 0px;
}
.imgspam{
  display: block;
  margin-left: auto;
  margin-right: auto;  
  margin-top: 0px;
  height: 80px;
  width: 80px;
  float: right;
}

/* для картиныки снизу */
.txtsmile{
  display: flex;
  padding-top: 48px;
  flex-direction: column;
  align-items: flex-start;
  font-size: 48px;
  color: #000;
}
/* .check1{
  height: 16px;
  width: 16px; 
}*/
/* .white {
  background-color: white;
} */
/* .logo {
  display: block;
  margin: 0 auto 2rem;
} */

/* 
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  } */

  /* .logo {
    margin: 0 2rem 0 0;
  } */
/* 
  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  } 
 } */
</style>
