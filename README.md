# RV32EM Simulator Guide For Mac Users
This is a guide for how to get Professor Nitta's RISC-V simulator up and running on all Macs.

_The following instructions apply to all Macs (Apple Silicon [M1, M1 Pro, & M1 Max] Macs and Macs with an x64 architecture). A Mac with an x64 architecture and another Mac with an Apple Silicon (ARM) architecture were used for testing in the making of these instructions._

## Installing XQuartz
_Do not worry if XQuartz does not ask you allow certain permissions on your Mac/restart your Mac. This does not impact XQuartz being able to show the simulator, and when testing this installation out, XQuartz did not ask for certain permissions._

_Note that **macOS 10.9 or higher** is needed to install XQuartz. To check which version of macOS is installed on your Mac, click the  Logo and then click **About This Mac**. The version number is the version of macOS your Mac is running._

<img width="1000" alt="macOS Version" src="https://user-images.githubusercontent.com/84110959/155892102-52519deb-e5ec-4963-9db4-6e111f8935c0.png">

### Instructions

1. **Download XQuartz** by clicking the following link: https://www.xquartz.org/

2. Once you have download XQuartz, open the downloaded file and double-click on “XQuartz.pkg.” A message that says “This package will run a program to determine if the software can be installed” may appear. If that message appears, click “Allow.”

<img width="1000" alt="XQuartz Prompt" src="https://user-images.githubusercontent.com/84110959/155892378-e6b482d4-29ea-47de-865b-67d6d2ba403d.png">




3. The Installer window will now show. **Click** **Continue** to read over the Read Me and License Agreement. After reviewing the License Agreement, **click Agree**.

4. **Click Install**. When prompted enter your Mac password/use Touch ID to continue the installation.

5. Once XQuartz is finished installing, **click Close** or **Log Out** (if you see “Log Out” instead of “Close”).

The following prompt may appear. 

<img width="1000" alt="Installer Prompt" src="https://user-images.githubusercontent.com/84110959/155892534-793f5a89-f169-48a2-a2fe-9ef547c8703e.png">

You can click **Keep** or **Move to Trash**. Clicking either option won’t affect the installation of XQuartz. Note that when clicking **Log Out**, your Mac will log out, so you will need to log back in. Once you log back in, XQuartz will be installed.

## Running the Simulator On The CSIF
1. **Open Terminal** by searching up “Terminal” on Spotlight or by opening Finder > Applications > Terminal.

2. **Launch Pulse Secure and connect to the Library VPN**. Connecting to the library VPN is needed to log into the CSIF. If you are not sure how to connect to the library VPN, click [here](https://www.library.ucdavis.edu/service/connect-from-off-campus/vpn-installation-guide-mac/) for further instructions.
3. Go to Terminal and **type in the following command**:

`ssh -X [username]@[pc#].cs.ucdavis.edu`

**Example:** `ssh -X gunrock@pc2.cs.ucdavis.edu`

**Note:** *You only need to use the -X flag for the simulator. Past instructions talked about using both the -X flag and the -Y flag, but using just the -X still launches the simulator.*

4. Once you enter in that command, enter your CSIF password. Once you are logged into the CSIF, you can now r**un the following command to launch the simulator in Debugger Mode**:

`/home/aaron123/riscv-console/riscv-sim/bin/riscv-console-sim -d`

Once this command is entered, XQuartz should launch and open a window with the RISC-V Simulator in Debugger Mode.

**Note:** If *copying/pasting the above command does not work, try typing the entire command out. Additionally, entering similar commands such as* `/home/aaron123/riscv-console/riscv-sim/bin/riscv-console-sim -d &` *should work and launch the simulator as well. Also note that the commands provided in this step are specifc to ECS 50 classes taught by Aaron Kaloti.*

<img width="1158" alt="RISCV Console" src="https://user-images.githubusercontent.com/84110959/155893384-cbfec828-6b92-4855-bcd9-3cd739b9dd2e.png">

## Reason Why This Guide Was Made
I made this guide because I found previous instructions for running the RV32EM simualtor on the CSIF to be confusing. It took me some time to figure out how to get the simulator up and running on my Mac, and I didn't want it to be a hassle for anyone taking ECS 50 to get the simulator running. Thus, I created these instructions to making getting the simulator running easier. 

If you are taking ECS 50 now or in the future and you find these instructions to be outdated or need revisions, feel free to let me know.






