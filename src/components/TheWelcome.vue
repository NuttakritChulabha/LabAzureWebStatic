<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'

import Step1 from '@/assets/1.jpg';
import Step2 from '@/assets/2.jpg';
import Step3 from '@/assets/3.jpg';
import Step4 from '@/assets/4.jpg';
import Step5_1 from '@/assets/5-1.jpg';
import Step5_2 from '@/assets/5-2.jpg';
import Step6 from '@/assets/6.jpg';
import Step7 from '@/assets/7.jpg';
import Step8_1 from '@/assets/8-1.jpg';
import Step8_2 from '@/assets/8-2.jpg';
</script>

<template>
  <div>
    <h1>Lab Azure Static Web Apps Deploy CI/CD</h1>

    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>1. เข้าไปที่ Azure Portal ค้นหา Resource Group ที่ต้องการสร้าง Static Web App และกด Create</template>
      <ul>
        <li>เข้าไปที่ Azure Portal และสร้าง Resource Group ใหม่หรือเลือก Resource Group ที่ต้องการสำหรับ Static Web App ของคุณ.</li>
      </ul>
      <img :src="Step1" alt="Step 1" width="800" />
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <ToolingIcon />
      </template>
      <template #heading>2. ที่ marketplace สามาพิมพ์ static web app เพื่อหา service ต้องการ และเลือก Static Web App</template>
      <ul>
        <li>ที่ marketplace สามาพิมพ์ static web app เพื่อหา service ต้องการ และเลือก Static Web App</li>
      </ul>
      <img :src="Step2" alt="Step 2" width="800" />
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <EcosystemIcon />
      </template>
      <template #heading>3. กด Create</template>
      <ul>
        <li>กด Create</li>
      </ul>
      <img :src="Step3" alt="Step 3" width="800" />
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <CommunityIcon />
      </template>
      <template #heading>4. Display Create Static Web App</template>
      <ul>
        <li>4.1 ตรวจสอบ Subscription และ Resource Group:</li>
        <li>เลือก Subscription ที่ถูกต้องจากรายการที่ปรากฏในดรอปดาวน์ (ในกรณีนี้ Subscription ถูกเลือกไว้แล้ว)</li>
        <li>เลือกหรือสร้าง Resource Group ใหม่ตามต้องการ (ในภาพตัวอย่างได้สร้าง Resource Group ใหม่ชื่อ "LabAzureWebStatic-demo")</li>
        
        <li>4.2 ตั้งชื่อ Static Web App:</li>
        <li>กรอกชื่อของ Static Web App ในช่อง "Name" (ในกรณีนี้ได้ตั้งชื่อว่า "LabAzureWebStatic-demo")</li>

        <li>4.3 เลือก Hosting Plan:</li>
        <li>เลือก Plan Type ที่ต้องการ สำหรับกรณีนี้เลือก Plan Type แบบ "Free: For hobby or personal projects" เนื่องจากเป็นการทดสอบ demo</li>
        <li>มีตัวเลือกอื่น ๆ เช่น "Standard: For general purpose production apps" และ "Dedicated (preview): For general purpose production apps" สำหรับการใช้งานในสถานการณ์ที่ต้องการความสามารถสูงขึ้น</li>

        <li>4.4 Deployment Details:</li>
        <li>เลือกแหล่งที่มาของโค้ดสำหรับการดีพลอย (ในภาพได้เลือก "GitHub")</li>
        <li>เลือกหรือเปลี่ยน GitHub account ที่จะใช้ (ในภาพได้เลือก GitHub account ไว้แล้ว)</li>
        <img :src="Step4" alt="Step 4" width="800" />

      </ul>
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <SupportIcon />
      </template>
      <template #heading>5. ในการตั้งค่า Build and Deployment Details สำหรับ Static Web App บน Microsoft Azure โดยใช้ GitHub repository</template>
      <ul>
        <li>5.1 Organization:</li>
        <li>เลือก Organization ที่เกี่ยวข้องจากดรอปดาวน์ (ในกรณีนี้เลือก "NuttakritChulabha")</li>
        <li>5.2 Repository:</li>
        <li>เลือก Repository ที่ต้องการดีพลอย (ในกรณีนี้เลือก "LabAzureWebStatic")</li>
        <li>5.3 Branch:</li>
        <li>เลือก Branch ที่ต้องการดีพลอย (ในกรณีนี้เลือก "developer_demo")</li>
        <li>5.4 Build Details:</li>
        <li>Build Presets:</li>
        <li>ระบบจะตรวจสอบประเภทของโปรเจคและแนะนำการตั้งค่าที่เหมาะสมโดยอัตโนมัติ (ในกรณีนี้ระบบตรวจพบว่าเป็นโปรเจค Vue.js)</li>
        <li>App location:</li>
        <li>ตั้งค่า App location เป็น root directory ของโปรเจค (ในกรณีนี้เป็น "/")</li>
        <li>Output location:</li>
        <li>ตั้งค่า Output location เป็น "dist" ซึ่งเป็นโฟลเดอร์ที่สร้างไฟล์ผลลัพธ์หลังจาก build</li>
        <li>5.5 Review & Create:</li>
        <li>เมื่อเสร็จสิ้นการตั้งค่าทั้งหมด สามารถคลิกปุ่ม "Review + create" เพื่อตรวจสอบรายละเอียดและสร้าง Static Web App</li>
        <img :src="Step5_1" alt="Step 5-1" width="800" />
        <img :src="Step5_2" alt="Step 5-2" width="800" />
      </ul>
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <SupportIcon />
      </template>
      <template #heading>6. รอระบบสร้างให้เรา</template>
      <ul>
        <li>หลังจากที่ระบบทำการสร้างเสร็จสิ้น, กลับมาที่ Resource Group ที่ได้สร้าง Static Web App</li>
      </ul>
      <img :src="Step6" alt="Step 6" width="800" />

    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <SupportIcon />
      </template>
      <template #heading>7. กลับมาที่ Resource Group ที่ได้สร้าง Static Web App</template>
      <ul>
        <li>กลับมาที่ Resource Group ที่ได้สร้าง Static Web App แล้วตรวจสอบการทำงาน</li>
      </ul>
      <img :src="Step7" alt="Step 7" width="800" />

    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <SupportIcon />
      </template>
      <template #heading>8. ตรวจสอบผลการทำงาน</template>
      <ul>
        <li>กดเข้าไปที่ service และทำการ Click URL เพื่อตรวจสอบ ว่า service run ปกติ Ex. <a href="https://jolly-desert-0a2e16700.5.azurestaticapps.net/" target="_blank" rel="noopener">https://jolly-desert-0a2e16700.5.azurestaticapps.net/</a></li>
      </ul>
      <img :src="Step8_1" alt="Step 8-1" width="800" />
      <img :src="Step8_2" alt="Step 8-2" width="800" />

    </WelcomeItem>
  </div>
</template>

<style scoped>
h1 {
  margin-bottom: 2rem;
  text-align: center;
}

h2 {
  margin-top: 2rem;
  color: #333;
}

img {
  display: block;
  margin: 1rem auto;
  border: 1px solid #ddd;
  border-radius: 8px;
}
</style>
