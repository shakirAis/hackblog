<template>
  <div>
    <ul v-for="(blogPost, index) in blogPosts" :key="index">
      <nuxt-link :to="`~/content/blog/${blogPost.slug}`">{{blogPost.title}}</nuxt-link>
      <p>{{blogPost.description}}</p>
    </ul>
  </div>
</template>

<script>
export default {
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts
    },
  },
}
</script>

<template>
  <b-container>
    <b-row>
      <b-col md="12">
        <div id="posts" v-for="(blogPost, index) in blogPosts" :key="index">
          <div class="post">
            <h3>{{blogPost.title}}</h3>
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

                  <p class="full_version">{{blogPost.description}}</p>
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
