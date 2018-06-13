# Using the Private Ethereum Blockchain (Ether-Dev)

To run Ether-Dev, first you need to install [Parity](https://github.com/paritytech/parity#config-file)

#### Simple one-line installer of parity for Mac and Ubuntu

```bash
bash <(curl https://get.parity.io -Lk)
```

The one-line installer always defaults to the latest beta release. To install a stable release, run:

```bash
bash <(curl https://get.parity.io -Lk) -r stable
```


For more details about parity please refer to the official [website](https://www.parity.io/)

For details about installation please refer the link for [Parity](https://github.com/paritytech/parity#config-file)

## About Ether-Dev

We created a personal node for testing, by using the steps below. Since all the work is already done, you may simply take the ether-dev file from this repository and run `ether-dev` Shell script.

It will,

1. If there are any existing blockchain data it will Delete them.
2. Initialize a new chain having node1 with `dev.json` which gives 100 ether for each account
3. It will automatically create private test network with 3 ether nodes and its corresponding interface.
4. Start the chain where it shows for node1
    1. Unlock all the accounts for easy testing
    2. Expose RPC interface at http://127.0.0.0:8545
    3. Expose WebSocket interface at ws://127.0.0.0:8546
    4. Expose Parity UI interface at http://127.0.0.0:8180
5. Url for 1st node is accessed along with signer token

## Usage

    ether-dev [options] command...
       Performs install and start when command is not specified.
       Commands will be executed one by one in the same order

    COMMANDS:
       install         Create private chain in current working directory
       uninstall       Remove chain from current working directory
       reset           Perform uninstall and install
       start           Start development chain in current working directory
       stop            Stop development chain running in current working directory

    OPTIONS:
       -v | --version  Print version number
       -h | --help     Shows a list of commands and options


### Install the Ethereum Blockchain (Parity)

    ether-dev install

Terminal looks like below image

![](images/etherdev-install.png)

### Start the Ethereum Blockchain (Parity)

    ether-dev start

After starting the process, output is shown as below

![](images/etherdev-start.png)

1. Open the Parity UI url as shown in your terminal along with given token (eg:http://13.229.123.120:8180/#/?token=EJJU-Zzay-9z6g-OaQF)
    1. After opening the the URL shown in your terminal , it appears as below
    ![](images/parityui-1.png)
    2. Click the check box shown, next at the bottom right corner a pop message appears. Select **APPROVE**
    3. Now select **Parity Wallet** icon
    4. The Parity UI will appear like the image below having 10 accounts with 100 ether each.
    ![](images/ParityUI.png)

2. Open http://remix.ethereum.org under **RUN** go to **Environment** field and select **Web3 Provider** from the drop down list.
3. It prompts for dialog box saying **Are you sure you want to connect to an ethereum node?** select **OK**
4. Now provide the Web3 Provider Endpoint url which is displayed in your terminal for Remix IDE (eg: http://172.31.21.36:8545) and select **OK**
5. Remix is now connected to you dev nodes, where it displays all the 10 accounts created under Accounts field in drop down showing all the accounts having 100 ether each.

![](images/RemixIDE.png)

### Stop the Ethereum Blockchain (Parity)


    ether-dev stop

Output looks like the image below

![](images/ether-dev_stop.png)

### Uninstall the Ethereum Blockchain (Parity)

    ether-dev uninstall

Output should appear like below image

![](images/etherdev-uninstall.png)
