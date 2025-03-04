<template>
  <div class="container-fluid mb-5">
    <div class="mt-lg-12 d-flex justify-content-center row">
      <div class="col-lg-10 d-flex justify-content-center row mt-3">
        <a :href="instagramUrl" target="_blank">
          <h1 class="header">@{{ instagramToRedirect }}</h1>
        </a>
      </div>
      <div class="col-lg-11">
        <div
          class="page-body mt-1 col-lg-12 justify-content-center row d-flex container-fluid"
        >
          <div class="col-lg-6 page-card mx-md-4">
            <Description />
          </div>
          <div class="col-lg-5 page-card">
            <div>
              <h3><b>Entre em contato comigo</b></h3>
            </div>
            <div class="form-group">
              <button class="btn" @click="redirectToInstagram">
                Ir para Instagram
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row"></div>
  </div>
  <div
    class="container-fluid mt-5 d-flex justify-content-center"
    style="
      background-color: #f0f8ff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    "
  >
    <h3>Adicionar Cases e videos demonstrativos</h3>
  </div>

  <page-footer />
</template>

<script>
import PageFooter from "./PageFooter.vue";
import Description from "./Description.vue";

export default {
  components: { PageFooter, Description },
  data() {
    return {
      campos: "",
      camposativos: false,
      instagramUrl: "https://www.instagram.com/julianekarlafreire_personal/",
      instagramToRedirect: "julianekarlafreire_personal",
    };
  },
  watch: {
    campos(newValue) {
      this.camposativos = newValue !== "";
    },
  },
  methods: {
    redirectToInstagram() {
      window.open(this.instagramUrl, "_blank");
    },
  },
};
</script>

<style lang="scss" scoped>
$text-color: #007acc;
$background-color: #f0f8ff;
$card-background: #ffffff;
$card-shadow: rgba(0, 0, 0, 0.1);

.header {
  border-bottom: 4px solid $text-color;
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 1rem;
}

.form-group {
  margin-top: 10px;
  input {
    border: 1px solid rgba(0, 122, 204, 0.26);
    background-color: rgba(240, 248, 255, 0.911);
    padding: 0.5rem;
    border-radius: 4px;
    width: 100%;
  }
}

@mixin card-border {
  text-align: left;
  border-radius: 8px;
  background: $card-background;
  box-shadow: 0 4px 8px $card-shadow;
  padding: 1rem;
  transition: box-shadow 0.3s ease;
  &:hover {
    box-shadow: 0 8px 16px $card-shadow;
  }
}

.card-border {
  @include card-border;
}

.btn {
  color: #fff;
  font-weight: bold;
  background-color: $text-color;
  height: 40px;
  border: none;
  border-radius: 4px;
  box-shadow: 0 4px 8px $card-shadow;
  transition: background-color 0.3s ease, box-shadow 0.3s ease;
  &:hover {
    background-color: darken($text-color, 10%);
    box-shadow: 0 8px 16px $card-shadow;
  }
}

.page-card {
  @include card-border;
  text-align: center;
  min-height: 450px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

header,
a {
  color: $text-color;
  text-decoration: none;
  transition: color 0.3s ease, font-size 0.3s ease;
  &:hover {
    font-size: 110%;
    color: darken($text-color, 10%);
  }
}
</style>
