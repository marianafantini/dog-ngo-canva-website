<script setup>
import { Typography } from 'ant-design-vue';
import { FacebookFilled, TwitterOutlined, InstagramOutlined } from '@ant-design/icons-vue';
const { Title, Paragraph } = Typography;
</script>

<template>
  <Layout class="layout">
    <Content class="content">
      <div class="first-half">
        <div>
          <Title :level="2">Contact Us</Title>
          <Paragraph class="paragraph">123 Anywhere St., Any City, ST 12345</Paragraph>
          <Paragraph class="paragraph">123-456-7890</Paragraph>
          <Paragraph class="paragraph">hello@reallygreatsite.com</Paragraph>
        </div>
        <div>
          <FacebookFilled class="image" />
          <TwitterOutlined class="image" />
          <InstagramOutlined class="image" />
          <Title :level="5">#suppawt our quest on social media @reallygreatsite</Title>
        </div>
      </div>
      <div class="second-half"></div>
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
}
.first-half {
  background-color: #1c7c54;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  .image {
    margin-right: 0.5rem;
  }
}
.second-half {
  background-color: #a5b5eb;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url('/assets/formatted-image-contact.png');
  background-position: center;
  img {
    margin: 0 1rem;
    width: 80%;
  }
}
.first-half,
.second-half {
  width: 50%;
  height: 100vh;
}
h2,
.paragraph {
  color: whitesmoke;
}
.image,
h5 {
  color: #ddf1cf;
  margin-top: 0;
}

@media (min-width: 1024px) {
  .first-half,
  .second-half {
    width: 50%;
    height: 100vh;
  }
  .first-half {
    padding: 5rem;
  }
  .second-half {
    background-size: 80% auto;
    background-repeat: no-repeat;
  }
}
@media (max-width: 1024px) {
  .content {
    flex-direction: column;
  }
  .first-half,
  .second-half {
    width: 100%;
  }
  .first-half {
    height: 60vh;
    padding: 0 2rem;
  }
  .second-half {
    height: 40vh;
    background-size: 100% auto;
    background-image: url('/assets/contact.jpeg');
  }
  h2 {
    font-size: 3rem;
  }
  .paragraph,
  .green-paragraph {
    font-size: 1.2rem;
    width: 100%;
    font-weight: 400;
  }
}
</style>
