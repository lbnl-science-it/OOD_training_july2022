---
#marp: true
theme: gaia
color: #000
footer: 'HPC training : 28 July, 2022'
colorSecondary: #333
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.jpg')

---
<style>section { font-size: 25px; }</style>
<!-- _class: lead -->
<!-- _paginate: false -->

# Open OnDemand on Lawrencium 
#### Sapana Soni


---
<style scoped>section { font-size: 28px; }</style>
<!-- paginate: true -->
# Outline

1. [Introduction](#3)
2. [Accessing OOD on Lawrencium](#4)
3. [OOD attributes](#5)
   - Interactive Applications: Jupyter notebook, Rstudio, Matlab, desktop environment
   -  Customize Jupyter kernels 
   -  File explorer
   -  Cluster shall access
   -  Job management
  

----
<style scoped>section { font-size: 24px; }</style>
# Introduction 
- What is Open OnDemand?
   - OpenOnDemand is a web platform that provides an easy access to the cluster’s HPC resourcess and services.  
   - Designed and developed by Ohio Supercomputer Center.
- Why OOD?
  - new users: intutive and easy access to computing resourses, removes barrier in using HPC resourses for their research. 
  - advanced users: alternate and conviniet way to traditional command line access
  - System admins: Support users form diverse backgrounds



---
<!-- _class: lead -->
<style>
footer { font-size: 20px
    }
</style>

<style scoped>section { font-size: 24px; }</style>
- How OOD works at system level? 
<style>
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
</style>

![w:700 center](ood_system_view.png)

Users are able to use HPC services more efficiently through Open OnDemand. 

---

### OOD services available at Lawrencium
<style scoped>section { font-size: 28px; }</style>

- Easy file management
- Command-line shell access
- Facile job submission and monitoring
- Interactive applications:
  - Graphical desktop environment
  - Jupyter notebook
  - Rstudio
  - Matlab
- More applications can be added as per user demand

---

# How to access OOD on Lawrencium?
<style scoped>section { font-size: 25px; }</style>
 1. Web link to connect : [https://lrc-ondemand.lbl.gov/](https://lrc-ondemand.lbl.gov/)
**Note:** Use Chrome or Firefox to brows this page. Safari has some issues.


![w:700](authentication.png)

2.  Use your LRC username and PIN+one-time password (OTP)
        - Same creatials you use to login to Lawrencium 


---

### OOD Dashboard on Lawrencium
On successful authentication you will see a OOD dashboard. 

![w:800 center](dashboard.png)

---
## Interactive Apps: Jupyter notebook
Click on Interactive apps --> Jupyter Server to open Jupyter notebook

![w:800 center](Jupyter_button.png)

---
Interactive mode

![ bg w:500 center](interactive.png)

----
Compute mode

![bg w:440](compute.png) 
![bg w:600](association.png)

----
![bg vertical w:700](JS_queue.png)
![bg w:700](JS_launch.png)

---
![bg vertical w:700](JN_kernels.png)
![bg w:700](JN_hello_world.png)


---
## Custom pyKernel
If you’d like to use a language or version of python or different conda environment not indicated in the drop-down menu of jupyter notebook you’ll need to create your own kernel.


**Two ways of customization:** 
1. Using a Conda environment
2. Manually creating a new kernel

[Click here for details.](https://it.lbl.gov/resource/hpc/for-users/hpc-documentation/open-ondemand/jupyter-server/)

---
## Interactive Apps: Rstudio

![bg w:500](Rstudio.png)
![bg w:500](RS_launch.png)

----

Compute and interactive mode 
![bg w:500](RS_interactive.png)
![bg w:500](RS_compute.png)

---
## Interactive Apps: Matlab
![bg w:500](Matlab.png)
![bg w:500](launch.png)

---
## Desktop 

---
### Using Desktop to launch VMD and ParaView

---

# File management

---

# Command-line shell access

---
# Job submission and management

---
