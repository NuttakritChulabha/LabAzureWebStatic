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
      <template #heading>1. Go to the Azure Portal, search for the desired Resource Group to create a Static Web App, and click Create</template>
      <ul>
        <li>Go to the Azure Portal and create a new Resource Group or select an existing Resource Group for your Static Web App.</li>
      </ul>
      <img :src="Step1" alt="Step 1" width="800" />
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <ToolingIcon />
      </template>
      <template #heading>2. In the marketplace, type "static web app" to find the desired service, and select Static Web App</template>
      <ul>
        <li>In the marketplace, type "static web app" to find the desired service, and select Static Web App.</li>
      </ul>
      <img :src="Step2" alt="Step 2" width="800" />
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <EcosystemIcon />
      </template>
      <template #heading>3. Click Create</template>
      <ul>
        <li>Click Create.</li>
      </ul>
      <img :src="Step3" alt="Step 3" width="800" />
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <CommunityIcon />
      </template>
      <template #heading>4. Display Create Static Web App</template>
      <ul>
        <li>4.1 Check Subscription and Resource Group:</li>
        <li>Select the correct Subscription from the dropdown list (in this case, the Subscription is already selected).</li>
        <li>Select or create a new Resource Group as needed (in the example image, a new Resource Group named "LabAzureWebStatic-demo" was created).</li>
        
        <li>4.2 Name the Static Web App:</li>
        <li>Enter the name of the Static Web App in the "Name" field (in this case, named "LabAzureWebStatic-demo").</li>

        <li>4.3 Choose Hosting Plan:</li>
        <li>Select the desired Plan Type. For this example, select the "Free: For hobby or personal projects" plan type since it is for demo testing.</li>
        <li>Other options include "Standard: For general purpose production apps" and "Dedicated (preview): For general purpose production apps" for higher capability requirements.</li>

        <li>4.4 Deployment Details:</li>
        <li>Choose the source of code for deployment (in the image, "GitHub" is selected).</li>
        <li>Select or change the GitHub account to be used (in the image, a GitHub account is already selected).</li>
        <img :src="Step4" alt="Step 4" width="800" />

      </ul>
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <SupportIcon />
      </template>
      <template #heading>5. Configure Build and Deployment Details for Static Web App on Microsoft Azure using GitHub repository</template>
      <ul>
        <li>5.1 Organization:</li>
        <li>Select the related Organization from the dropdown (in this case, "NuttakritChulabha" is selected).</li>
        <li>5.2 Repository:</li>
        <li>Select the Repository to deploy (in this case, "LabAzureWebStatic" is selected).</li>
        <li>5.3 Branch:</li>
        <li>Select the Branch to deploy (in this case, "developer_demo" is selected).</li>
        <li>5.4 Build Details:</li>
        <li>Build Presets:</li>
        <li>The system will automatically detect the type of project and suggest appropriate settings (in this case, the system detects it as a Vue.js project).</li>
        <li>App location:</li>
        <li>Set the App location to the root directory of the project (in this case, "/").</li>
        <li>Output location:</li>
        <li>Set the Output location to "dist", which is the folder that creates the output files after the build.</li>
        <li>5.5 Review & Create:</li>
        <li>Once all settings are complete, click the "Review + create" button to review the details and create the Static Web App.</li>
        <img :src="Step5_1" alt="Step 5-1" width="800" />
        <img :src="Step5_2" alt="Step 5-2" width="800" />
      </ul>
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <SupportIcon />
      </template>
      <template #heading>6. Wait for the system to create the app</template>
      <ul>
        <li>After the system has finished creating the app, return to the Resource Group where the Static Web App was created.</li>
      </ul>
      <img :src="Step6" alt="Step 6" width="800" />

    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <SupportIcon />
      </template>
      <template #heading>7. Return to the Resource Group where the Static Web App was created</template>
      <ul>
        <li>Return to the Resource Group where the Static Web App was created and check its operation.</li>
      </ul>
      <img :src="Step7" alt="Step 7" width="800" />

    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <SupportIcon />
      </template>
      <template #heading>8. Verify operation</template>
      <ul>
        <li>Click into the service and click the URL to verify that the service is running correctly. For example: <a href="https://jolly-desert-0a2e16700.5.azurestaticapps.net/" target="_blank" rel="noopener">https://jolly-desert-0a2e16700.5.azurestaticapps.net/</a></li>
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
