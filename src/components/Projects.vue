<template>
  <div id="projects">
    <div class="projectsheader">
      <div class="projectbox">
        <p>PROJECTS</p>
        </div>
    </div>
    <div class="carousel">
          <v-carousel hide-delimiters interval=60000 light>
              <v-carousel-item v-for="(item,i) in items" :key="i">
                <div class="projlink" >
                  <a :href="item.link">
                  <img :src="item.src" class="projimg"/>
                  </a>
                </div>
              </v-carousel-item>
      </v-carousel>
    </div>
  </div>
</template>

<script>
export default {
  name: "Projects",
  data() {
    return {
      items: [
        {
          // src: "../assets/bullutinfullscreen.png",
          src: "/landing-page/img/bullutinfullscreen.png",
          link: "https://bullutin.herokuapp.com/#/"
        },
        {
          // src: "../assets/battle-cards.png",
          src: "/landing-page/img/battle-cards.png",
          link: "https://michaelgreen94.github.io/battle-cards/"
        },
        {
          // src: "../assets/usingmusic.png",
          src: "/landing-page/img/usingmusic.png",
          link: "https://michaelgreen94.github.io/Music-Is-Fun/"
        },
        {
          // src: "../assets/kanban.png",
          src: "/landing-page/img/kanban.png",
          link: "https://cmcarlsonkanban.herokuapp.com/#/login"
        }
      ]
    };
  }
};
</script>


<style>
p {
  margin-bottom: 0;
}

.projimg {
  object-fit: cover;
  object-position: center;
  height: 70vh;
  width: 100%;
}

.projlink {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 70vh;
  cursor: pointer;
}

#projects {
  height: 70vh;
  width: 100%;
  flex-wrap: wrap;
  background-color: white;
  display: flex;
}
.v-carousel {
  height: 65vh !important;
  width: 85%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel {
  height: 100%;
  width: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-size: contain;
}
.projectbox {
  width: fit-content;
  border: 0.2rem solid black;
  padding: 0.5rem;
  color: black;
}

.v-carousel__item {
  width: 80% !important;
}

/* :global(.v-image__image) {
  background-size: contain !important;
} */

.projectsheader {
  height: 100%;
  width: 40%;
  font-size: 2rem;
  font-weight: 800;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-bottom: 0;
  padding-top: 0;
}

@media (max-width: 768px) {
  #projects {
    height: 100vh;
  }
  p {
    margin-bottom: 0 !important;
  }
  .projectsheader {
    height: 20%;
    width: 100%;
    font-size: 2rem;
    font-weight: 800;
    display: flex;
    justify-content: center;
    align-items: flex-end;
    padding-bottom: 0.5rem;
  }
  .carousel {
    height: 80%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-size: contain;
  }
  .v-carousel__item {
    width: 90% !important;
  }
  .v-carousel {
    height: 70vh !important;
  }

  :global(.v-image__image) {
    background-size: cover !important;
  }
}
</style>
