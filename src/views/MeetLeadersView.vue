<script setup>
import { Layout, Typography } from 'ant-design-vue';
const { Title } = Typography;
const { Content } = Layout;

const volunteerList = [
  'Jackson Davis',
  'Elias Gillete',
  'Freya Moore',
  'Elvira Montanez',
  'Herman Adelphi',
];
</script>

<template>
  <Layout class="layout">
    <Content class="content">
      <div class="first-half">
        <Title :level="2">Meet Our Intrepid Rescue Leaders</Title>
      </div>
      <div class="second-half">
        <div class="leaders-wrapper" v-for="volunteer in volunteerList" :key="volunteer">
          <img
            class="image"
            :style="{ borderRadius: '50%', objectFit: 'cover' }"
            :src="'./assets/' + volunteer.replace(' ', '-') + '.jpg'"
          />
          {{ volunteer }}
        </div>
      </div>
    </Content>
  </Layout>
</template>

<style lang="scss" scoped>
.layout,
.content {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  background-color: #ddf1cf;
}
.second-half {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}

.leaders-wrapper {
  display: grid;
  align-items: center;
  grid-auto-columns: auto;
  grid-auto-rows: auto;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
}

@media (min-width: 1024px) {
  .first-half h2 {
    font-size: 4.5rem;
    width: 85%;
    padding: 0 5rem;
  }
  .first-half,
  .second-half {
    width: 50%;
    height: 100vh;
  }
  .second-half {
    background-size: 80% auto;
    background-repeat: no-repeat;
    padding: 4rem 0;
  }
  .image {
    width: 6rem;
    height: 6rem;
  }
}
@media (max-width: 1024px) {
  .first-half h2 {
    padding: 0 2rem;
  }
  .first-half,
  .second-half {
    width: 100%;
  }
  .first-half {
    height: 40vh;
  }
  .second-half {
    height: 60vh;
    background-size: 100% auto;
    display: flex;
    flex-wrap: wrap;
  }
  .content {
    flex-direction: column;
  }
  .image {
    width: 4rem;
    height: 4rem;
  }
  .leaders-wrapper {
    width: 50%;
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
    padding: 0 2rem 1rem 2rem;
  }
}
</style>
