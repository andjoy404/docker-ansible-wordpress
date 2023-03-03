## HOW TO

* To understand the complete steps of this Task, you should have some basic knowledge of **AWS Cloud EC2 Instance, Webserver, AWS RDS service, Wordpress, Ansible ROLE.**
* Make Sure you should have account on **AWS Cloud.**
* Go to **EC2->KEY-PAIRS** service and create one new Key Pair with whatever the name you wanna give let’s say- **“key.pem”** download it and put it on our workspace. And run this command:

  * ```
    chmod 400 key.pem
    ```
* Create one **vault file** of Ansible, where we gonna put all our user credentials like  **“access_key” and “secret_key”** , that ansible use while login. Command:

  * ```
    ansible-vault create cred.yml
    ```
* It will ask you to create password, create it and put the credential like that:

  * ```
    access_key: XXXXXXXXXX

    secret_key: XXXXXXXXXXX
    ```
* **Command to run the playbook:**

  * ```
    ansible-playbook execute.yml --ask-vault-pass
    ```
* Now using the **Public Ip** of the instance over the browser, we can see the wordpress site. URL:

  * ```
    http://<PUBLIC_IP>/wordpress
    ```
