<p align="center">
  <img src="/images/azure-logo.png" width="196" height="196" />
</p>

<div align="center">

# Setting Up an Azure Virtual Machine Homelab

## Prerequisites

- St. Clair College student account
- $100 free Azure credits (available to St. Clair students, no credit card needed!)

## Step 1: Access Your Azure Educational Account

1. Navigate to [Azure for Education](https://azureforeducation.microsoft.com/devtools)
2. Click "Sign In"
3. If prompted with St. Clair login, use your existing credentials
4. If you see the Microsoft "Pick an Account" prompt, select "**Use another account**"
5. Enter your **StClairConnect email address** and **existing password**

note: if you want to original st clair tutorial download the word docx in tutorial folder

## Step 2: Navigate the Azure Portal

Once logged in, you'll see the Azure Portal dashboard:

1. Select "**All Services**" 
2. In the search field, type "**Education**"
3. This will show all available software through your student account

<div style="text-align:center;">

![Education-tab-overview](/images/education-overview.png)

</div>

## Step 3: Create Your Virtual Machine

1. From the Azure dashboard, locate and click on the "**Virtual Machines**" tab

<div style="text-align:center;">

![All-the-services](/images/all-services.png)

</div>

2. Click "**Create**" or "**+ Add**" to start creating a new VM
3. Fill in the necessary information:
   - **Virtual Machine Name**: Choose a descriptive name
   - **Image (ISO)**: Select **Windows 10 Pro** (to have access to Hyper-V)

## Step 4: Choose VM Size

Select a size based on your needs and budget:

| Size Option | Type | Specs | Monthly Cost |
|-------------|------|-------|-------------|
| **D4s_v3** | D-Series v3 (General Purpose) | 4 vCPUs, 16GB RAM | 140.16 CAD |
| **E2_v3** | E-Series v3 (Memory Optimized) | 2 vCPUs, 16GB RAM | 91.98 CAD |

> 💡 **Note**: Hyper-V is typically already enabled on the E-Series VMs.

## Step 5: Configure Basic Settings

1. Create a username and strong password
2. Select your region (choose one closest to your location)
3. Configure network settings (default settings are usually sufficient)
4. Review and create the VM

## Step 6: Connect to Your VM

1. Once the VM is deployed, go to the VM's "**Overview**" page
2. Click "**Connect**"
3. Note the connection details (example: 20.163.59.125:3389 for RDP port)
4. Download the RDP file
5. Open the RDP file and enter your VM credentials when prompted

## Step 7: Enable Hyper-V (If Not Already Enabled)

Follow the Microsoft tutorial to enable Hyper-V:
[Step-by-Step Enabling Hyper-V for Windows](https://techcommunity.microsoft.com/blog/educatordeveloperblog/step-by-step-enabling-hyper-v-for-use-on-windows-11/3745905)

Basic steps include:
1. Open PowerShell as Administrator
2. Run: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All`
3. Restart when prompted

## Step 8: Create Windows Server VMs in Hyper-V

Now you can create nested Windows Server VMs within your Azure VM:

1. Open Hyper-V Manager
2. Click "New" > "Virtual Machine"
3. Download Windows Server ISO from your Azure Education software options
4. Create and configure Windows Server VMs for practice

## Cost Management Tips

- **Shut down your VM** when not in use to save credits
- Monitor your usage in the Azure Cost Management section
- Set up budget alerts to avoid unexpected charges

---

Happy learning with your new Windows Server homelab environment! This setup will give you valuable hands-on experience for your MIT642 Network Design course.