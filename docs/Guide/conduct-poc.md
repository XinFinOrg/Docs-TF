

##**1.Set up Master Node**

**Prerequisite**

- Operating System : Ubuntu 16.04 64-bit or higher Should be facing internet directly with public IP & without NAT

- Tools: Git, Docker, Docker Compose

- Network Ports

Following network ports need to be open for the nodes to communicate.

8545  TCP - RPC <br>   
30303 TCP/UDP - XDC

**How to Setup Masternode ?**

**0. Install Git**

* Check whether git is preinstalled.

    > git --version

If present, output will be something like git version 2.17.1. in this case, go to step a.

* Otherwise follow the below steps.

- sudo apt update
- sudo apt install git
- git --version

* Configure Git.

- git config --global user.name "Your Name"
- git config --global user.email "youremail@domain.com"

**a. Clone repository**

Run the following commands on your terminal.

- git clone [https://github.com/XinFinOrg/XinFin-Node.git](https://github.com/XinFinOrg/XinFin-Node.git)
- cd XinFin-Node

The git clone command will create a new folder XinFin-Node. cd XinFin-Node command changes the current directory to XinFin-Node

**b. Install docker & docker-compose**

       sudo ./install\_docker.sh

The above command will install docker and docker-compose for you.

**c. Update .env file with details**

* Copy a env.example file from XinFin-Node directory and name it as a .en
* Open .env file and edit values for following

- INSTANCE_NAME : A Display name of your masternode
- CONTACT_DETAILS : Your Email ID

![overview](/assets/xinfin-node.png)

![overview](/assets/masternode-.env.png)


**d. Start your Node**

        sudo docker-compose -f docker-services.yml up -d

This will start a Masternode and connect to a XinFin Testnet.

You should be able to see your node listed on this page: [XinFin Network](https://www.xinfin.network) (Make sure, you are connected to XinFin Testnet. If not, switch to Tesnet on top right corner)

Your coinbase address can be found in xdcchain/coinbase.txt file.

![overview](/assets/masternode-listing.png)

##**2. Stake XDC**

  **Create XDC Wallet**

      > Visit http://xinfin.network/#webWallet and Click on create a new wallet.
      > you can create use a web wallet or download eWallet app from Google Play Store.
      > Create an account
      > Store your private key at a safe place (Hardware wallet is recommended)

![overview](/assets/xinfin_wallet.png)


   **Buy XDC**

     > get your free XDC to use on XinFin Testnet
     > Visit XinFin TestNet Faucet http://xinfin.network/#getTestXDC.
     > Add your wallet address created in step 2.b and request XDC

![overview](/assets/masternode-faucet.png)

##**3. Upload KYC**

    > Visit http://xinfin.network/#masternode
    > Upload a notarized kyc

##**4. Become a Candidate**

Add your account address and click on Become a Candidate to become a masternode. You must have minimum 10 Million XDC in your account. Once your candidature is accepted your stake of 10 Million XDC is locked.

![overview](/assets/1.png)


##**5. Website Set-Up**

#**Prerequisite**

Xampp

Clone this Repo directly into xampp/htdocs path.

![screenshot_2019-02-26 xinfinorg tradefinexlive](https://user-images.githubusercontent.com/22572604/53394517-8d17d280-39c5-11e9-875c-510792592022.png)

#**Front End**

Go to - application/config.php

Set - $config['base_url'] = 'http://example.com/' or 'https://example.com/'

![ss2](https://user-images.githubusercontent.com/22572604/53398863-ae31f080-39d0-11e9-9c6c-4c293bfa2220.png)

Go to - application/database.php

Set -
'hostname' => 'localhost', (change required if needed)
'username' => '',
'password' => '',
'database' => '',

![ss3](https://user-images.githubusercontent.com/22572604/53399063-2ef0ec80-39d1-11e9-8f1a-f29c38c1d422.png)

Go to - application/emailc.php

Set -

$config['$econfig'] = array('protocol' => 'smtp',

'smtp_host' => '', /* email gateway host /

'smtp_port' => 465,

'smtp_user' => '', / email gateway username /

'smtp_pass' => '', / email gateway password */

'wordwrap' => TRUE,

'charset' => 'utf-8');

![ss4](https://user-images.githubusercontent.com/22572604/53399233-9444dd80-39d1-11e9-8cb1-87b9e948066b.png)


#**Admin Panel**

Go to - application/adminpanel/config.php

Set - $config['base_url'] = 'http://example.com/adminpanel/' or 'https://example.com/adminpanel/'

![ss5](https://user-images.githubusercontent.com/22572604/53400806-a5dbb480-39d4-11e9-9efd-165507ee1d2e.png)


Go to - application/adminpanel/constants.php

Set to - define('BASE_FRONT_URL', 'http://example.com/' or 'https://example.com/');

![ss6](https://user-images.githubusercontent.com/22572604/53404917-ac6e2a00-39dc-11e9-9dea-463783a8bdc8.png)

Go to - application/adminpanel/database.php

Set to -

'hostname' => 'localhost', (change required if needed)

'username' => '',

'password' => '',

'database' => '',

![ss7](https://user-images.githubusercontent.com/22572604/53493055-74d8ae00-3ac0-11e9-8da4-b632c1619ba5.png)



