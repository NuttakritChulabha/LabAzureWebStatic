<script setup>
import Step1 from '@/assets/a1.jpg';
import Step2 from '@/assets/a2.jpg';
import Step3 from '@/assets/a3.jpg';
import Step4_1 from '@/assets/a4-1.jpg';
import Step4_2 from '@/assets/a4-2.jpg';
import Step4_3 from '@/assets/a4-3.jpg';
import Step5 from '@/assets/a5.jpg';
import Step6 from '@/assets/a6.jpg';
</script>

<template>
  <div class="container">
    <h1>Extra: Add a Custom Domain</h1>
    <h2>1. Go to the menu and select "Add a custom domain"</h2>
    <img :src="Step1" alt="Step 1" width="800" />
    <h2>2. Enter the domain you want to connect and click Next</h2>
    <img :src="Step2" alt="Step 2" width="800" />
    <h2>3. Enter the information provided into your domain provider, such as Cloudflare, and complete the process by clicking Add</h2>
    <img :src="Step3" alt="Step 3" width="800" />
    <h2>4. Verify that the added domain is displayed under Custom Domains</h2>
    <img :src="Step4_1" alt="Step 4-1" width="800" />
    <img :src="Step4_2" alt="Step 4-2" width="800" />
    <img :src="Step4_3" alt="Step 4-3" width="800" />
    <h2>5. Test the URL of the added domain to ensure the website displays correctly</h2>
    <img :src="Step5" alt="Step 5" width="800" />
    <h2>6. Test the URL of the added domain to ensure the website displays correctly</h2>
    <img :src="Step6" alt="Step 6" width="800" />
  </div>
</template>

<style scoped>
.container {
  background-color: #2c2c2c;
  color: #ffffff;
  padding: 2rem;
  border-radius: 8px;
}

h1 {
  margin-bottom: 2rem;
  text-align: center;
}

h2 {
  margin-top: 2rem;
  color: #dddddd;
}

img {
  display: block;
  margin: 1rem auto;
  border: 1px solid #ddd;
  border-radius: 8px;
}
</style>
