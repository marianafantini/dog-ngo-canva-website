<script setup>
import { Layout, Typography } from 'ant-design-vue';
const { Title, Paragraph } = Typography;
const { Content } = Layout;
</script>

<template>
  <Layout class="layout">
    <Content class="content">
      <Title :level="2">How We Help</Title>

      <div class="flex">
        <div class="items">
          <img class="image" src="/assets/dog-icon.png" />
          <div>
            <Title :level="4">Animal Rescue</Title>
            <Paragraph class="paragraph">
              We go on quests to rescue and recover any dog or cat roaming our streets.
            </Paragraph>
          </div>
        </div>
        <div class="items">
          <img class="image" src="/assets/vet-icon.png" />
          <div>
            <Title :level="4">Veterinary Services</Title>
            <Paragraph class="paragraph">
              We provide free veterinary treatment to strays, rescues, and pets.
            </Paragraph>
          </div>
        </div>
        <div class="items">
          <img class="image" src="/assets/home-icon.png" />
          <div>
            <Title :level="4">Fostering and Adoption</Title>
            <Paragraph class="paragraph">
              We help our rescues find their temporary and forever homes.
            </Paragraph>
          </div>
        </div>
      </div>
    </Content>
  </Layout>
</template>

<style lang="scss" scoped>
.layout {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  background-color: #a5b5eb;
}
.content {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.flex {
  display: grid;
  align-items: center;
  font-weight: 400;
  height: 100%;
}
.image {
  height: 6rem;
  width: 6rem;
}
@media (max-width: 1024px) {
  h2 {
    font-size: 3rem;
    padding: 1rem 2rem;
  }
  h4 {
    font-size: 1.5rem;
    margin-top: 0;
  }
  .ant-typography.paragraph {
    font-size: 1.2rem;
    font-weight: 400;
  }
  .flex {
    padding: 0 2rem 2rem 2rem;
    grid-template-rows: repeat(auto-fill, minmax(10rem, 1fr));
  }
  .image {
    height: 4rem;
    width: 4rem;
  }
  .items {
    display: flex;
    justify-content: space-around;
    & > div {
      padding-left: 1rem;
    }
  }
}
@media (min-width: 1024px) {
  h2 {
    font-size: 4.5rem;
    padding: 3rem;
  }
  .flex {
    padding: 4rem;
    grid-template-columns: repeat(auto-fill, minmax(33%, 1fr));
    div {
      max-width: 80%;
    }
  }
}
</style>
