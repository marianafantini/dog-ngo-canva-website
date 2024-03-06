<script setup>
import { Layout, Typography } from 'ant-design-vue';
const { Title, Paragraph } = Typography;

const { Content } = Layout;
</script>

<template>
  <Layout class="layout">
    <Content class="content">
      <div class="first-half">
        <Title :level="2" class="first-title">Pets change our lives.</Title>
        <Title :level="2" class="second-title">We're on a quest to change theirs.</Title>
        <Paragraph class="paragraph">
          Quest for Paws Animal Rescue and Sanctuary is a nonprofit organization dedicated to
          rescuing, fostering, and rehoming the abandoned, sick, and injured animals around our
          city.
        </Paragraph>
        <Paragraph class="paragraph">
          With you help, we hope to make a difference in the lives of these wonderful animals.
        </Paragraph>
      </div>
      <div class="second-half"></div>
    </Content>
  </Layout>
</template>

<style lang="scss" scoped>
.content {
  display: flex;
  width: 100%;
}
.first-half {
  background-color: #1c7c54;
}
.second-half {
  background-color: #ddf1cf;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url('/assets/formatted-image-about.png');
  background-position: center;
}

.first-title {
  margin-bottom: 0;
  color: #ddf1cf;
}
.second-title {
  margin-top: 0 !important;
  color: #ddf1cf;
}
.layout {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
}
.first-title,
.paragraph {
  color: whitesmoke;
  .second-title {
    margin: 0 5rem;
    max-width: 60%;
  }
}

@media (min-width: 1024px) {
  .first-title {
    margin: 7rem 5rem 0 5rem;
    font-size: 3rem;
  }
  .second-title {
    margin: 0 5rem 4rem 5rem !important;
    font-size: 3rem;
  }
  .paragraph {
    font-size: 1.5rem;
    padding: 0 3rem 0 5rem;
  }
  .first-half,
  .second-half {
    width: 50%;
    height: 100vh;
  }
  .second-half {
    background-size: 80% auto;
    background-repeat: no-repeat;
  }
}
@media (max-width: 1024px) {
  .first-title,
  .second-title {
    font-size: 2.8rem;
    margin-left: 1rem;
    margin-right: 1rem;
  }
  .paragraph {
    font-size: 1.2rem;
    font-weight: 400;
    padding: 0 1rem 0 1rem;
  }
  .first-half,
  .second-half {
    width: 100%;
  }
  .first-half {
    height: 70vh;
  }
  .second-half {
    height: 30vh;
    background-size: 100% auto;
    background-image: url('/assets/about.jpeg');
    .image {
      height: 70%;
    }
  }
  .content {
    flex-direction: column;
  }
}
</style>
