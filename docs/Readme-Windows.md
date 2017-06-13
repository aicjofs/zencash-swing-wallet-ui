# [Zencash](https://zensystem.io) Desktop GUI Wallet - for Windows

The [ZenCash](https://zensystem.io) development team has released a [version for Windows](https://github.com/cronicc/zen/releases).
Before installing the GUI wallet on Windows you need to install ZClassic on Windows.

![Screenshot](https://github.com/aicjofs/zencash-swing-wallet-ui/raw/master/docs/ZClassicWalletWindows.png "ZenCash Wallet for Windows")

1. Installing Zencash on Windows

   1.1. Download the ZenCash node(link may change with newer versions always check for latest release) [Zen_Win_binaries_soft_fork_v1.zip](https://github.com/cronicc/zen/releases/download/v.2.0.9-2-b4315d9-soft-fork/Zen_Win_binaries_soft_fork_v1.zip)

   1.2. Unzip the file so that the executables `zend.exe` and `zend-cli.exe` are in one directory.
   
   1.3. Download the [ZenCash Proving Key](https://z.cash/downloads/sprout-proving.key)
        and store it in directory `%APPDATA%\ZcashParams`.
        
   1.4. Download the [ZenCash Verifying Key](https://z.cash/downloads/sprout-verifying.key)
        and store it in directory `%APPDATA%\ZcashParams`.
        
   After downloading the two keys, they should be available in the same directory similar to:
![Screenshot](https://github.com/aicjofs/zencash-swing-wallet-ui/raw/master/docs/ZCashKeyDir.png "ZenCash keys directory on Windows")

   1.5. Create directory `%APPDATA%\Zen` and a text file `zen.conf` in it with the following content:
   ```
   rpcuser=zenrpc
   rpcpassword=fortytwo   
   ```
   1.6 Note: Steps 1.3 through 1.5 can be done automatically by running "start zend.bat" after the proving/verifying keys are downloaded
             the batch file may be stopped.
  
2. Installing the Zen Desktop GUI wallet

   2.1. Install JDK 8 for Windows - e.g. [use this good tutorial](http://www.wikihow.com/Install-the-Java-Software-Development-Kit)

   2.2. You may use the [latest binary release of the ZenCash Desktop GUI wallet](https://github.com/aicjofs/zencash-swing-wallet-ui/releases/latest).
   Download file [ZencashSwingWalletUI.jar](https://github.com/aicjofs/zencash-swing-wallet-ui/releases/download/)
   and place it in the same folder as `zend.exe` and `zen-cli.exe`. The result needs to be similar to:
![Screenshot](https://github.com/aicjofs/zencash-swing-wallet-ui/raw/master/docs/ZClassicWinDir.png "ZenCash directory on Windows")

4. Running the installed ZenCash GUI wallet

   The wallet GUI is a Java program packaged as an executable JAR file. It may be run from command line or started from another GUI tool 
   (e.g. file manager). One way to run it from command line is:
   ```
   java -jar ZClassicSwingWalletUI.jar
   ```
   You may instead just use Windows the file manager and double-click on the `ZencashSwingWalletUI.jar`. 
   This will start the ZClassic GUI wallet.

### Donations accepted
This project is non-commercial in nature and developed by volunteers. If you find the GUI
Wallet useful, please consider making a donation for its further development. Your contribution matters! Donations 
are accepted at Zen address:
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

### Known issues and limitations

1. Issue: Wallet versions 0.58 and below, when running on Windows systems with (typically non-western) locales that
redefine the decimal point in the Windows locale settings, have problems with updating the GUI wallet state. 
A workaround is to change the Windows [locale settings](https://windows.lbl.gov/software/optics/5-1-2/Optics4.jpg) to have dot as decimal separator.
