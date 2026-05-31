<template>
    <div class="flex flex-col justify-center items-center my-12">
        <h4 class="font-bold text-3xl">Featured Blog Posts</h4>
        <div class="flex gap-8 mt-7">
            <UiCardBlog
            v-for="item in articles" 
            :key="item.id"
            :image="item.image"
            :title="item.title"
            :description="item.description"
             />
        </div>
    </div>
</template>

<script setup>
import img1 from '@/assets/images/Group 5.png';
import img2 from '@/assets/images/Group 6.png';
import img3 from '@/assets/images/Group 7.png';
// Contoh data, nantinya ini bisa berasal dari API atau database
const articles = ref([
  {
    id: 1,
    image: img1,
    title: 'The Future of Medical Devices: What’s Next?',
    description: 'Explore the latest trends and innovations shaping the medical device industry. From AI-powered diagnostics to wearable health technologies, learn how these advancements are transforming patient care and the healthcare system.'
  },
  {
    id: 2,
    image: img2,
    title: 'How Our Devices Are Revolutionizing Healthcare Delivery',
    description: 'Discover how our medical devices are helping healthcare professionals provide more accurate diagnoses, better patient monitoring, and improved treatment options. This blog post explores the real-world impact of our products in hospitals and clinics around the world.'
  },
  {
    id: 3,
    image: img3,
    title: 'Ensuring Safety in Medical Device Manufacturing',
    description: 'Safety is our top priority. In this post, we take you behind the scenes of our stringent testing and quality control processes to ensure that every device meets the highest safety standards. Learn more about our commitment to keeping patients and healthcare workers safe.'
  }
])
</script>