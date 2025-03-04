<template>
  <div class="description">
    <h2>Sobre mim</h2>
    <p>
      Olá! Eu sou Juliane Karla Freire, uma personal trainer dedicada a ajudar
      você a alcançar seus objetivos de fitness. Com anos de experiência e uma
      abordagem personalizada, ofereço treinos adaptados às suas necessidades
      individuais.
    </p>
    <p class="text-align-left h5 mt-3">Meus serviços incluem:</p>

    <div class="text-align-left">
      <ul class="text-align-left">
        <li>Treinamento personalizado</li>
        <li>Acompanhamento de progresso</li>
        <li>Avaliação física</li>
        <li>Planos de treino online via aplicativo</li>
      </ul>
    </div>
    <p>Junte-se a mim e transforme sua vida com saúde e bem-estar!</p>
  </div>
</template>

<script>
export default {
  name: "Description",
};
</script>

<style scoped>
.description {
  background-color: #f0f8ff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.description h2 {
  color: #007acc;
}

.description p,
.description ul {
  color: #333;
}
.text-align-left {
  text-align: left;
}

.description ul {
  list-style-type: disc;
  padding-left: 20px;
}
</style>
