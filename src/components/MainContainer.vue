<template>
  <main>
    <ContainerContent>
      <section class="row donate">
        <DonateCard
          title="Feliz Natal e Feliz Ano Novo!"
          btnTitle="Fazer uma doação"
          text="Nessas festas de fim de ano mande um presente para a pessoa amada e
            compartilhe a alegria do Natal."
        />
        <SectionImage image="send.svg" />
      </section>
    </ContainerContent>
    <section class="accessories">
      <ContainerContent>
        <p class="title">Acessórios</p>
        <p class="text">
          Nessas festas de fim de ano mande um presente para a pessoa amada e
          compartilhe a alegria do Natal.
        </p>

        <div class="row mt-5">
          <AcessorieCard
            image="giving1.svg"
            title="Presentes"
            text="Eles são os melhores presentes que existem."
          />
          <AcessorieCard
            image="giving2.svg"
            title="Enfeites"
            text="Dê uma decoração."
          />
          <AcessorieCard
            image="giving3.svg"
            title="Doces"
            text="Aproveite os doces natalinos."
          />
          <AcessorieCard
            image="giving4.svg"
            title="Muito amor"
            text="Aproveite os sentimentos que duram para sempre."
          />
        </div>
      </ContainerContent>
    </section>
    <ContainerContent>
      <section class="row donate">
        <SectionImage image="shared.svg" />
        <DonateCard
          title="Comemore com
        muito amor!"
          btnTitle="Fazer doação"
          text="Nestes feriados, festeje com muito amor e paz, oferecendo muitas bênçãos aos nossos entes queridos, amigos e vizinhos, desejando-lhes um Feliz Natal."
        />
      </section>
    </ContainerContent>
  </main>
</template>

<script>
import ContainerContent from "./ContainerContent.vue";
import AcessorieCard from "./AcessorieCard.vue";
import DonateCard from "./DonateCard.vue";
import SectionImage from "./SectionImage.vue";

export default {
  name: "MainContainer",
  components: {
    ContainerContent,
    AcessorieCard,
    DonateCard,
    SectionImage,
  },
};
</script>

<style scoped>
.title {
  font-size: 3rem;
  font-weight: 600;
  letter-spacing: 0.2px;
}
section.donate {
  padding: 200px 0px;
}

section.accessories {
  background-color: var(--white-color);
  padding: 48px 0px 100px 0px;
}
section.accessories .title {
  text-align: center;
}
section.accessories .text {
  max-width: 500px;
  color: var(--gray-200-color);
  margin: 0 auto;
  font-style: normal;
  font-weight: 400px;
  font-size: 0.9rem;
}
</style>