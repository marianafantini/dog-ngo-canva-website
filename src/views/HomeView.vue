<script setup>
import { Layout, Typography, Button } from 'ant-design-vue';
const { Title } = Typography;
const { Content } = Layout;
</script>

<template>
  <Layout class="layout">
    <Content>
      <Title :level="1">Our four-legged friends need your help</Title>
      <Title :level="4">Quest for Paws Animal Rescue and Sanctuary</Title>
      <Button size="large">Sponsor a rescue today</Button>
    </Content>
  </Layout>
</template>

<style lang="scss" scoped>
.layout {
  background-image: url('/assets/home.jpeg');
  background-repeat: no-repeat;
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: row;
  align-items: center;
}
h1,
h4 {
  color: whitesmoke;
}
button {
  margin: 2rem 5rem;
  background-color: #ddf1cf;
  border-color: #ddf1cf;
  font-weight: bold;
  font-size: 1rem !important;

  &:hover {
    color: #0a3162;
    border-color: #0a3162;
  }
}
@media (min-width: 1024px) {
  .layout {
    background-size: 100% auto;
  }
  h1 {
    font-size: 4rem;
  }
  h1,
  h4 {
    max-width: 27%;
    margin: 0 5rem;
  }
}
@media (max-width: 1024px) {
  .layout {
    background-size: cover;
  }
  h1 {
    font-size: 3rem;
  }
  h1,
  h4 {
    margin: 0 3rem;
  }
  button {
    margin: 3rem;
  }
}
</style>
