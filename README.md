# VM Lifecycle on GCP and OCI — Tutorial

## Video Tutorials:
GCP: <paste link> \
OCI: <paste link>

## Prereqs
- Cloud access to GCP and OCI
- No PHI/PII; smallest/free-tier shapes

---

## Google Cloud (GCP)
### Create/Start VM
 **pictures of each step are under the images and gcp folder* * 
1. Go to [google cloud](https://console.cloud.google.com)
2. Make sure you created and selected a project
3. Click Create a VM

![GCP create](images/gcp/gcp_step1-3.png)

4. Give it a name under " Name* "
5. Chose a " Region* " and " Zone* " of your chose, better if it's a region near you
6. Scroll down and choose a Machine type
- In this case E2 (smallest available/free-eligible) and scroll down more and pick e2-micro

![GCP create](images/gcp/gcp_step6.2.png)

7. Then click " OS and storage "
8. Click " Change "
9. Under " Operating system ", click " Ubuntu " and then click " Select "

![GCP create](images/gcp/gcp_step9-10.png)

10. Others will remain at default
- Boot disk: default minimal
- Network: default VPC; ephemeral public IP
11. Click " Create "
- Once you see a green circle with a check next to the name of your VM, it is up and running

![GCP create](images/gcp/gcp_step11.2.png)

### Optional
12. Now click on the name of your VM
13. Click the " SSH " button and then " Authorize "
14. Type in "sudo apt-get update" and then enter
- This command updates the package lists for upgrades of packages that need upgrading
- Example: you can type " python3 " after to run python codes

![GCP create](images/gcp/gcp_step14.png)

15. Type in "exit()" and then enter and close the tab to leave

### Stop VM
16. Click the back arrow next to the name of your VM
17. Click on the 3 dots
18. Click " Stop " and " Stop " again

![GCP create](images/gcp/gcp_step17-18.1.png)

- Once it shows a gray circle with a white square, it means your VM has stopped running

![GCP create](images/gcp/gcp_step18.3.png)

- To start it again you can click the 3 dots and click on " Start/Resume " and then go back to step 11

### Delete VM
19. To delete it, click the 3 dots again
20. Then click delete
21. Once it is deleted, you should not see it anymore under " VM instances "

![GCP create](images/gcp/gcp_step21.png)

---

## Oracle Cloud (OCI)
### Create
1. Compartment: <name>
2. Networking: VCN with Internet Connectivity (defaults)
3. Shape: <smallest/free-eligible>
4. Image: Ubuntu (or Oracle Linux)
5. Public IP: ephemeral
6. Boot volume: default minimal

![OCI create](images/oci_create.png)

### Start/Stop
- Start: <state shows RUNNING>
- Stop: <state shows STOPPED>

![OCI running](images/oci_running.png)

### Terminate
- Terminate and delete boot volume; verify cleanup

![OCI cleaned](images/oci_clean.png)

---

## Reflections
### Similarities
- <brief bullets>

### Differences
- <brief bullets>

### Preference (OCI vs GCP) and Why
- <one short paragraph>