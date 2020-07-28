<template>
  <b-container>
    <b-row>
      <b-col md="12">
        <div id="posts">
          <div class="post">
            <h3>Мобильная связь и интернет в Германии</h3>
            <b-row>
              <b-col md="4">
                <div>
                  <b-carousel
                    id="carousel-fade"
                    style="text-shadow: 0px 0px 2px #000"
                    img-width="250"
                    img-height="300"
                    fade
                    controls
                  >
                    <b-carousel-slide
                      img-src="~/assets/slide1.png"
                    ></b-carousel-slide>
                    <b-carousel-slide
                      img-src="~/assets/slide1.png"
                    ></b-carousel-slide>
                    <b-carousel-slide
                      img-src="~/assets/slide1.png"
                    ></b-carousel-slide>
                  </b-carousel>
                </div>
              </b-col>
              <b-col md="8">
                <div class="post_content">
                  <span>Источник: <a>https://t.me/tt_de</a></span>
                  <p class="short_version">В Германии существует 3 оператора мобильной связи, это Deutsche telekom, Vodafone и O2. Также существуют мобильные операторы для турков, созданные на основе трех вышеперечисленных, например Ayyildiz, которые предоставляют выгодные планы для звонков в Турцию. 

                  Чтобы приобрести сим карту, обязательно нужно иметь при себе паспорт, иной раз спрашивают ещё и немецкую прописку. Сим карта стоит денег, около 10 евро, а чтобы её "заправить" нужно платить отдельно. Вообще сим карту можно купить в любом супермаркете без предоставления документов, но чтобы её активировать нужно пройти онлайн подтверждение личности по видеосвязи.</p>

                  <p class="full_version">В Германии существует 3 оператора мобильной связи, это Deutsche telekom, Vodafone и O2. Также существуют мобильные операторы для турков, созданные на основе трех вышеперечисленных, например Ayyildiz, которые предоставляют выгодные планы для звонков в Турцию. 

                  Чтобы приобрести сим карту, обязательно нужно иметь при себе паспорт, иной раз спрашивают ещё и немецкую прописку. Сим карта стоит денег, около 10 евро, а чтобы её "заправить" нужно платить отдельно. Вообще сим карту можно купить в любом супермаркете без предоставления документов, но чтобы её активировать нужно пройти онлайн подтверждение личности по видеосвязи.
                  Как  заправляется симка тоже очень интересная история. Естественно, также как и у нас в России можно заплатить с банковской карты, но только не через приложение вашего банка, а на сайте оператора. Там можно платить картой каждый раз либо настроить автоматический платёж. В России тоже вроде раньше так можно было, но лично я этим пользовалась лет 10 назад, а потом стала закидывать деньги через мобильный банк, это намного удобнее. Либо есть альтернатива, узнав о которой я невольно вспомнила свой первый мобильный телефон и начало нулевых. Если кто помнит, тогда чтобы заправить симку надо было покупать карту в салонах мобильной связи и ввести оттуда код в свой телефон используя определенный набор "решёток" и "звёздочек". Тут тоже примерно такая система, отличие только в том, что ты покупаешь в супермаркете эту карту, там нет никакого кода, кассир пробивает карту как товар, а потом выдаёт чек, где и находится тот самый заветный код. Далее этот код надо ввести в личном кабинете. Ещё один интересный факт связанный с мобильной связью: мой аккаунт в гугл был привязан к российской банковской карте, поэтому я не могла скачать мобильное приложение своего оператора на свой смартфон, в play market попросту это приложение не отображалось. После того как  аккаунт привязала к немецкой карте, то уже приложение стало доступным для скачивания. 

                  Что касается цен, мобильные планы здесь не дешевые, а мобильный интернет по российским меркам очень дорогой. 2 гигабайта мобильного интернета стоит около 10 евро, могут быть небольшие отличия в зависимости от оператора, но у всех примерно одинаковые цены.  Если пользоваться звонками и смс, то это будет стоить еще денег. Ютубчик не глянешь короче по мобильному интернету, надо ловить вай фай. К слову, в метро, можно подключиться к бесплатному вай фаю, нужно только нажать на галочку, что ты согласен с условиями (по-моему никто эти условия не читает). 

                  Что касается домашнего интернета, операторов тоже достаточно, лично мы пользуемся услугами водафона. Договор составляется сразу на 2 года, этот нюанс кстати может оказаться немного проблематичным, в случае если ты надумаешь отказаться от этого оператора или переехать в другую квартиру. Ежемесячный платёж составляет 20 евро. В России конечно все это дело стоит гораздо дешевле и качество намного лучше. 

                  И напоследок поделюсь самой неприятной штукой по этой теме: немецким законодательством запрещено скачивать торренты. За несоблюдение этого закона приходят огромные штрафы, говорят в районе 300 евро за один торрент. Поэтому люди покупают планы на такие сервисы как Netflix, Amazon Prime итд. </p>
                  <a class="more" v-on:click="showMore">{{ buttonMessage }}</a>
                </div>
                <div class="tags">
                  <a>мобильнаясвязьвгермании</a>
                  <a>интернетвгермании</a>
                </div>
              </b-col>
            </b-row>
          </div>
        </div>
      </b-col>
    </b-row>
  </b-container>
</template>
<script>
export default {
  asyncData () {
    return {
      name: process.static ? 'static' : (process.server ? 'server' : 'client')
    }
  },
  data () {
    return {
      isClicked: false,
      buttonMessage: 'Читать подробнее...',
    }
  },
  methods: {
    showMore() {
      this.isClicked = !this.isClicked;
      let shortBlock = document.getElementsByClassName('short_version')[0];
      let bigBlock = document.getElementsByClassName('full_version')[0];
      if (this.isClicked) {
        bigBlock.style.display = "block";
        shortBlock.style.display = "none";
        this.buttonMessage = 'Скрыть';
      } else {
        bigBlock.style.display = "none";
        shortBlock.style.display = "block";
        this.buttonMessage = 'Читать подробнее...';
      }
    },
  },
}
</script>
<style>
#posts {
  width: 100%;
  height: auto;
  display: block;
  margin-top: 50px;
  margin-bottom: 50px;
}
.post {
  min-height: 400px;
  height: auto;
  display: block;
  border-bottom: 5px solid #ffffd1;
}
.carousel-item {
  width: 250px;
  height: 300px;
}
.carousel-control-next-icon,
.carousel-control-prev-icon {
  position: absolute;
  width: 30px;
  height: 30px;
}
.carousel-control-prev-icon {
  left: 0;
  background-image: url(../assets/prev.png);
}
.carousel-control-next-icon {
  right: 0;
  background-image: url(../assets/next.png);
}
.carousel-inner {
  width: 250px;
  height: 300px;
  margin: auto;
  position: relative;
  margin-top: 25px;
}
p {
  font-family: "Open Sans";
  font-size: 14px;
  color: #000000;
  line-height: 18px;
  text-align: justify;
  margin-top: 20px;
  height: 220px;
}
h3 {
  color: #372424;
  text-align: center;
  font-family: "Roboto";
  font-weight: 500;
  font-size: 22px;
  margin-bottom: 10px;
}
span {
  font-family: "Roboto";
  font-weight: 400;
  font-size: 14px;
  text-align: right;
  display: inline-block;
  width: 100%;
  line-height: 20px;
}
span a {
  font-weight: 700;
  font-style: italic;
  line-height: 20px;
  font-size: 15px;
  color: #372424 !important;
  cursor: pointer;
}
.post_content {
  min-height: 250px;
  height: auto;
  margin-top: 20px;
  position: relative;
  display: block;
  width: 100%;
}
.post_content p.short_version {
  position: relative;
  height: 130px;
  width: 100%;
  overflow: hidden;
  display: block;
}
.post_content p.short_version:after {
  content: "...";
}
.post_content p.full_version {
  display: none;
  height: auto;
  padding-bottom: 50px;
}
.more {
  width: auto;
  line-height: 20px;
  height: 20px;
  display: inline-block;
  font-family: "Roboto";
  font-size: 16px;
  font-weight: 700;
  font-style: italic;
  position: absolute;
  right: 0;
  bottom: 20px;
  cursor: pointer;
  color: #372424 !important;
}
.tags {
  height: 20px;
  cursor: pointer;
  margin-bottom: 20px;
}
.tags a {
  color: #356666;
  font-family: "Roboto";
  font-size: 14px;
  font-style: normal;
  line-height: 20px;
  height: 20px;
  width: 200px;
  background-image: url(../assets/hashtag.svg);
  background-repeat: no-repeat;
  background-position: 0 50%;
  background-size: 11px;
  padding-left: 14px;
  cursor: pointer;
}
.tags a:hover {
  color: #356666;
  font-weight: 700;
  padding-left: 14px;
}
</style>
