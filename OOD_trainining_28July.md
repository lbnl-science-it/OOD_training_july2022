---
marp: true
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

![w:700 center](Figures/ood_system_view.png)

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


![w:700](Figures/authentication.png)

2.  Use your LRC username and PIN+one-time password (OTP)
        - Same creatials you use to login to Lawrencium 


---

### OOD Dashboard on Lawrencium
On successful authentication you will see a OOD dashboard. 

![w:800 center](Figures/dashboard.png)

---
## Interactive Apps: Jupyter notebook
Click on Interactive apps --> Jupyter Server to open Jupyter notebook

![w:800 center](Figures/Jupyter_button.png)

---
Interactive mode

![ bg w:500 center](Figures/interactive.png)

----
Compute mode

![bg w:440](Figures/compute.png) 
![bg w:600](Figures/association.png)

----
![bg vertical w:700](Figures/JS_queue.png)
![bg w:700](Figures/JS_launch.png)

---
![bg vertical w:700](Figures/JN_kernels.png)
![bg w:700](Figures/JN_hello_world.png)


---
## Custom pyKernel
If you’d like to use a different laguage or version of python or different conda environment not indicated in the drop-down menu of jupyter notebook you’ll need to create your own kernel.

**Two ways  of addiing kernel:**
1. Using conda environment
2. Manually creating a new kernel
   [Click here for details.](https://it.lbl.gov/resource/hpc/for-users/hpc-documentation/open-ondemand/jupyter-server/)
   

---
## Custom pyKernel: using conda environment

````
# Creating a pykernel for 3.9.12 version of python and installing packages

module load python/3.9.12
conda create --name=py39 ipykernel
source activate py39
python -m ipykernel install --user --name py39 --display-name="Bio_Chem"
conda install -c conda-forge openmm
conda install -c schrodinger pymol
````

---
## Interactive Apps: Rstudio

![bg w:500](Figures/Rstudio.png)
![bg w:500](Figures/RS_launch.png)

----

Compute and interactive mode 
![bg w:500](Figures/RS_interactive.png)
![bg w:500](Figures/RS_compute.png)

---
## Interactive Apps: Matlab
![bg w:500](Figures/Matlab.png)
![bg w:500](Figures/launch.png)

---
## Launching Desktop 
![bg w:400](Figures/desktop.png)
![bg w:400](Figures/desktop_cf1.png)
![bg w:400](Figures/desktop_launch.png)

---

## Desktop  
![bg w:400](Figures/desktop_screen.png)
![bg w:400](Figures/desktop_dropdown.png)
![bg w:400](Figures/desktop_terminal.png)

---
### Using Desktop to launch VMD and ParaView
![bg w:400](Figures/desktop_vmd_load.png)
![bg w:400](Figures/Desktop_vmd_app.png)
![bg w:400](Figures/desktop_vmd_protein.png)

---


# File management
- **Conventioanal approach: commad line**
  - Linux file editors for editing files: vi, vim, nano, emacs
  - File transfer: scp, rsync
- **Globus for file transfer**
- **Open OnDemand: Files feature**
  - view and edit text files
  - create or rename or delete files
  - create or renae or delete directories
  - file/directory upload and download
  ![bg w:600 right](Figures/dashboard_files.png)

---

### Files : Home directory  

![bg w:900 center](Figures/files_home_dir.png)

---

# Command-line shell access
![bg w:600](Figures/dashboard_shell.png)
![bg w:600](Figures/shell.png)


---
# Job submission and management

![bg w:600](Figures/dashboard_jobs.png)
![bg w:600](Figures/active_jobs.png)


---
# Job composer and template

![bg w:600](Figures/job_composer.png)
![bg w:600](Figures/create_template.png)

---
### Submission script 

![bg w:500](Figures/default_path.png)
![bg w:600](Figures/script.png)

---
# Job submission directory

Job composer creates a working directory by default on the path /global/home/users/spsoni/ondemand/data/sys/myjobs/projects/default
-  **Use default path:** Copy/upload all the files required for the jobs on this path before hitting Subimit button.
   -  click 'Open Dir' button at the bottom of the job script content.
   -  using a file explorer upload or transfer files

![w:300 center](Figures/open_dir.png)

  


---
**OR**

- **Set different working directory:** If you want to use files saved on different location and would like to run job in that diectory, for example: scratch.
  - add following command line in your job script
  ````
  cd /global/scratch/users/spsoni/my_working_dir
  ````
  **Note:** Use path you aim to set for your working directory. 
---

# Log out and clean up
- Log out of the portal

- Clean up
  - The portal stores temporary files for interactive apps on the path $HOME//ondemand/data/sys/dashboard/batch_connect/sys
  - It is a good practice to clean up this directory periodically.
  ```
  rm -rf $HOME/ondemand/data/sys/dashboard/batch_connect/sys/* 
  ```

---

  # Getting help
  - Vertual office hours: 
    - Walk in: every tuesday 10 am to 11.30 am
  - Send us tickets at hpcshelp@lbl.gov
  - More information about LBNL Supercluster and scientic computing services can be found [here](https://it.lbl.gov/service/scienceit/). 

Your feedback is important to us for improving HPC services and training.
Please fill out [training survey](https://docs.google.com/forms/d/1PrqmX6Y0ZO88w2_cV1LerOIkNqo8oalWhxw3lzyz3mw/edit)

![w:240 center](Figures/thankyou.png)
---