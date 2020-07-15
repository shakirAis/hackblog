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
                  <p>
                    В Германии существует 3 оператора мобильной связи, это
                    Deutsche telekom, Vodafone и O2. Также существуют мобильные
                    операторы для турков, созданные на основе трех
                    вышеперечисленных, например Ayyildiz, которые предоставляют
                    выгодные планы для звонков в Турцию. <br /><br />Чтобы
                    приобрести сим карту, обязательно нужно иметь при себе
                    паспорт, иной раз спрашивают ещё и немецкую прописку. Сим
                    карта стоит денег, около 10 евро, а чтобы её "заправить"
                    нужно платить отдельно. Вообще сим карту можно купить в
                    любом супермаркете без предоставления документов, но чтобы
                    её активировать нужно пройти онлайн подтверждение личности
                    по видеосвязи...
                  </p>
                  <a class="more">Читать подробнее...</a>
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
<style>
#posts {
  width: 100%;
  height: auto;
  display: block;
  margin-top: 50px;
  margin-bottom: 50px;
}
.post {
  height: 400px;
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
  height: 250px;
  margin-top: 20px;
  position: relative;
  display: block;
  width: 100%;
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
  bottom: 10px;
  cursor: pointer;
  color: #372424 !important;
}
.tags {
  height: 20px;
  cursor: pointer;
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
