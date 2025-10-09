# Flask on Cloud VM (Assignment 2)

## Student Info
- Name: Melissa Espinal
- Cloud Provider: Microsoft Azure

## Video recording: 
**Recording:** [Watch on Loom](https://www.loom.com/share/5afe75e55cb040a8808220a6fbf9240d?sid=cc8a2949-0419-4d98-a609-9e9ed3314912)

## Steps
### 1. VM Creation
**Create a VM**:  
   - **Region:** (US) West 2
   - **Zone Option:** Azure- selected zone (Preview)
   - **Image:** Ubuntu LTS
   - Public IP assigned
> [!TIP]
> Choose the smallest/free tier size. In this case the Standard B-series.
 

[Create VM Part #1](images/create_vm_1)
[Create VM Part #2](images/create_vm_2)

### 2. Networking (Port 5003 Open)
**Open port 5003**:  
   - Add a firewall/security group rule to allow inbound TCP traffic on **5003**.
   -   **Destination:** 5003
   -   **Protocol:** Any
       
[Port 5003 Open](images/Networking_Port5003_Open)

### 3. OS Update + Python Install
a. **SSH into your VM** (terminal).  
b. **Update OS**: To update, type in the following in your terminal:
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```  
c. **Install Git, Python 3 + pip**:  
   ```bash
   sudo apt install python3 python3-pip git -y
   ```
 ```bash
  git
   ```  
[Commands](images/Install_Git_Python3_pip)
[Commands](images/Git_terminal)

### 4. Flask App Running
[screenshot of terminal + browser]

### 5. Public IP Access
URL: http://XX.XX.XXX.XXX:5003  
[screenshot]

### 6. (Bonus) Domain Name
Domain: http://mydomain.tech:5003  
[screenshot]
