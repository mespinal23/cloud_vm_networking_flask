# Flask on Cloud VM (Assignment 2)

## Student Info
- **Name:** Melissa Espinal
- **Cloud Provider:** Microsoft Azure

## Video recording: 
**Recording:** [Watch on Loom](https://www.loom.com/share/5afe75e55cb040a8808220a6fbf9240d?sid=cc8a2949-0419-4d98-a609-9e9ed3314912)

## Steps
### 1. VM Creation
**Create a VM**:  
   - **Region:** (US) West 2
   - **Zone Option:** Azure- selected zone (Preview)
   - **Image:** Ubuntu LTS
   - **Public IP assigned**
> [!TIP]
> **Choose the smallest/free tier size. In this case the Standard B-series.**
 

[Create VM Part #1](images/Create_vm_1.png)
[Create VM Part #2](images/Create_vm_2.png)

### 2. Networking (Port 5003 Open)
**Open port 5003**:  
   - Add a firewall/security group rule to allow inbound TCP traffic on **5003**.
   -   **Destination:** 5003
   -   **Protocol:** Any
       
[Port 5003 Open](images/Networking_Port5003_Open.png)

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
[Commands](images/Install_Git_Python3_pip.png)
[Commands](images/Git_terminal.png)

### 4. Flask App Running
1. **Copy the Flask template**:  
   ```bash
   git clone https://github.com/hantswilliams/HHA-504-2025-FlaskStarter.git
   cd flask_template
   ```  
    Create new virutal environment: 
    ```
    python3 -m venv venv
    ```
    Then activate virtual environment:
    ```
    source venv/bin/activate
    ```
    Install: 
    ```
    pip install -r requirements.txt
    ``` 
2. **Run the app on port 5003**:  
   ```bash
   python3 app.py
   ```  

[Flask Terminal](images/Flask_Running_Terminal.png) 
[Flask Browser](images/Flask_Running_Browser.png)

> [!NOTE]
> **Please note that if you come across an issue with a command, simplyfying the command will work.**

### 5. Public IP Access
URL: http://20.64.253.35:5003

[Public IP Address](images/Public_IP_Access.png)
