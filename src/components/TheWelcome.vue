<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>สร้าง Git Repository</template>

    <ul>
      <li>Clone โครงการจาก <a href="https://github.com/NuttakritChulabha/LabAzureWebStatic" target="_blank" rel="noopener">GitHub Repository นี้</a> ไปยังเครื่องของคุณโดยใช้คำสั่ง:
        <pre><code>git clone https://github.com/NuttakritChulabha/LabAzureWebStatic</code></pre>
      </li>
      <li>สร้าง repository ใหม่ในบัญชี GitHub ของคุณและ push โค้ดจากเครื่องของคุณไปยัง repository ใหม่นี้:
        <pre><code>
git remote set-url origin https://github.com/YourUsername/YourNewRepo.git
git push -u origin main
        </code></pre>
      </li>
    </ul>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>สร้าง Resource Group</template>

    <ul>
      <li>เข้าไปที่ Azure Portal และสร้าง Resource Group ใหม่หรือเลือก Resource Group ที่ต้องการสำหรับ Static Web App ของคุณ.</li>
    </ul>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>ตั้งค่า Static Web App</template>

    <ul>
      <li>เข้าไปที่ Resource Group ที่เลือกและสร้าง Static Web App โดยเชื่อมต่อกับ GitHub repository ที่คุณสร้างในขั้นตอนที่ 1.</li>
    </ul>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>ตรวจสอบการทำงานของ Pipeline</template>

    <ul>
      <li>ตรวจสอบว่าการตั้งค่า pipeline (GitHub Actions หรืออื่นๆ) ทำงานได้ตามปกติโดยดูที่แท็บ "Actions" ใน GitHub repository ของคุณ.</li>
    </ul>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>เรียก URL และตรวจสอบผลการทำงาน</template>

    <ul>
      <li>หลังจากที่ Pipeline ทำงานเสร็จสิ้น, เรียก URL ที่ได้รับจาก Azure เพื่อแสดงผลเว็บของคุณ.</li>
    </ul>
  </WelcomeItem>
</template>
