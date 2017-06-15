# [ZenCash](http://zensystem.io) Desktop GUI Wallet - binary release v0.69-beta

This document describes how to install binary release v0.69-beta of the [ZenCash](http://zensystem.io) 
Desktop GUI Wallet. This release of the ZenCash Desktop GUI Wallet is tested with ZenCash version 
2.0.9. Users who encounter issues are welcome to report them in 
the [issues section](https://github.com/aicjofs/zencash-swing-wallet-ui/issues). 

![Screenshot](https://github.com/aicjofs/zencash-swing-wallet-ui/raw/master/docs/ZClassicWallet.png "Main Window")

## Installing and running the Wallet GUI

For Windows Installer check here [Information](https://github.com/aicjofs/zencash-swing-wallet-ui/blob/master/docs/Readme-Windows.md) or [Download for Windows](https://github.com/aicjofs/zencash-swing-wallet-ui/files/1079155/ZenCashSwingWallet4win693.zip)

1. Downloading the wallet
 
   Download file [ZencashSwingWalletUI.jar](https://github.com/aicjofs/zencash-swing-wallet-ui/releases/download/0.69.3-SNAPSHOT/ZenCashSwingWalletUI.jar)
   and place it in a folder like `~/Downloads`. Then please make the JAR executable with a command like:
   ```
   user@ubuntu:~/Downloads$ chmod u+x ./ZencashSwingWalletUI.jar
   ```
   
2. Verifying the download

   **This step is very important!** To verify that the file `ZenCashSwingWalletUI.jar` is an authentic release, you
   need to compute its SHA256 checksum, like this:
   ```
   user@ubuntu:~/Downloads$ sha256sum ZenCashSwingWalletUI.jar 
   FE3C443B6DDFBF1FD31ACBF8B141E27101D226317746B65B64EEF521AAB82CE5  ZenCashSwingWalletUI.jar
   ```
   **If the resulting checksum is not `FE3C443B6DDFBF1FD31ACBF8B141E27101D226317746B65B64EEF521AAB82CE5` then**
   **something is wrong and you should discard the downloaded wallet!**

3. Installing the downloaded ZenCash GUI wallet

  3.1. If you have built ZenCash from source code:

   Assuming you have already built from source code [ZenCash](http://zensystem.io) in directory `/home/user/zen/src` (for 
   example - this is the typical build dir. for ZenCash v2.0.9) which contains the command line tools `zen-cli` 
   and `zend`, you need to take the file `ZenCashSwingWalletUI.jar` and copy it 
   to diretcory `/home/user/zen/src` (the same dir. that contains `zen-cli` and `zend`). Example copy command:
   ```
   user@ubuntu:~/Downloads$ cp ./ZenCashSwingWalletUI.jar /home/user/zen/src    
   ```
   
4. Running the installed ZenCash GUI wallet

   Before running the GUI you need to start zcashd (e.g. `zend --daemon`). The wallet GUI is a Java program packaged 
   as an executable JAR file. It may be run from command line or started from another GUI tool (e.g. file manager). 
   Assuming you have already installed [ZenCash](http://zensystem.io) and the GUI Wallet `ZenCashSwingWalletUI.jar` in 
   directory `/home/user/zen/src` one way to run it from command line is:
   ```
   user@ubuntu:~$ java -jar /home/user/zen/src/ZenCashSwingWalletUI.jar
   ```
   If you are using Ubuntu (or similar ;) Linux you may instead just use the file manager and 
   right-click on the `ZenCashSwingWalletUI.jar` file and choose the option "Open with OpenJDK 8 Runtime". 
   This will start the ZClassic GUI wallet.

### Donations accepted
This project is non-commercial in nature and developed by volunteers. If you find the GUI
Wallet useful, please consider making a donation for its further development. Your contribution matters! Donations 
are accepted at ZClassic address:
```
znmReNZJKE4vSpyZjLyEhr9AP3yj4VVzyrj
```

### License
This program is distributed under an [MIT License](https://github.com/aicjofs/zencash-swing-wallet-ui/raw/master/LICENSE).

### Disclaimer

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

