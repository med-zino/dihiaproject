<template>
  <div class="container">
    <div v-for="item in items" :key="item.id" class="item">
      <template v-if="item.id % 2 === 0">
        <img :src="item.imgSrc" :alt="'Image ' + item.id" class="item-image" data-aos="fade-right">
        <div class="item-description" data-aos="fade-left">{{ item.description }}</div>
      </template>
      <template v-else>
        <div class="item-description" data-aos="fade-right">{{ item.description }}</div>
        <img :src="item.imgSrc" :alt="'Image ' + item.id" class="item-image" data-aos="fade-left">
      </template>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { id: 1, imgSrc: require('../../public/1.png'), description: "The image features a young woman with a charming smile, posing for a selfie. She's dressed in a stylish black outfit that contrasts beautifully with the vibrant background of lush floral arrangements. The flowers provide a romantic and sophisticated ambiance, with their multitude of soft pinks, creamy whites, and hints of warm yellows. The woman's dark, flowing hair frames her face gracefully, and her gaze towards the camera is inviting and confident. The photo exudes a sense of joy and casual elegance, making it an alluring snapshot of a moment filled with beauty and charm." },
        { id: 2, imgSrc: require('../../public/2.png'), description: "This image presents a juxtaposition of style and allure, capturing two different profiles of a young woman against a captivating backdrop of dense floral arrangements. On the left, the woman's back is turned to the camera, her posture exuding a sense of mystery and grace. She is wearing an elegant, pastel pink gown with delicate lace detailing, suggesting a formal, almost fairy-tale like quality. On the right, she faces the camera with a poised and confident stance, her black dress embodying a chic, modern fashion sensibility. Her paired knee-high boots add a trendy and bold statement to her ensemble. The floral wall behind her blooms with romance, adding a dreamy quality to the scene. The overlay text NEW ARRIVAL and the call to action GET THE CELEBRITY LOOK YOU HAVE BEEN CRAVING - SHOP NOW transform the image into a stylish advertisement, inviting viewers to emulate the sophisticated and enchanting look of the woman pictured." },
        { id: 3, imgSrc: require('../../public/3.png'), description: "This image features a fashion collage that serves as a weekly style inspiration. It includes three photographs of a woman showcasing a chic and relaxed outfit. In each photo, she dons a classic striped shirt paired with casual denim jeans, complemented by black open-toe heels. Her poses vary from sitting to looking off into the distance, conveying a thoughtful and effortless vibe. The setting is minimalistic with warm, neutral tones that give a serene and sophisticated atmosphere. The images are curated within a layout that includes a homey and stylish interior design corner, suggesting that the fashion is not only for wearing but also for living in style." },
        { id: 4, imgSrc: require('../../public/4.png'), description: "This fashion-forward advertisement captures the allure of a young woman, styled in a romantic floral top paired with a confident smile, embodying the essence of GLAMOUR FASHION. Her bold red lips and expressive eyes, accented by winged eyeliner, radiate a flirtatious charm that invites onlookers to engage with the latest trends. Each portrait is a beckoning call to shop now, promising the allure of being among the first to embrace this new collection, a tempting blend of style and sophistication." }
      ]
    }
  }
}
</script>

<style scoped>
.container {
  padding: 10px 76px 10px 74px;
}

.item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 20px; /* Spacing between items */
}

.item:nth-child(odd) .item-description {
  order: -1; /* This pushes the description to the left on odd items */
}

.item-image {
  width: 450px; /* Adjust size as needed */
  height: auto;
}

.item-description {
  flex-grow: 1;
  padding: 0 20px; /* Adjust spacing as needed */
  font-size: 18px; /* Bigger font size */
  max-width: 50%; /* Smaller width, adjust as needed */
  line-height: 1.8; /* Increased line spacing */

}

</style>
