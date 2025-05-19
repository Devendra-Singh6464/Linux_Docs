Please update your mac OS and X-code if update available on setting. 
1. Download the Flutter SDK:
```bash
flutter_macos_arm64_3.24.4-stable.zip
```
2. Create a folder where you can install Flutter.
```bash
mkdir development
```
3. Go to Downloads directory.
```bash
vi Downloads
```
4. Extract the file into the directory you want to store the Flutter SDK.
```bash
unzip flutter_macos_3.24.4-stable.zip -d /Users/arshad/development/
```
5.  open the zsh environmental variable file `~/.zshenv` in your text editor. If it doesn't, create `~/.zshenv`.
```bash
touch ~/.zshenv
```
6. add the flutter path in this file.
```bash
export PATH=$HOME/development/flutter/bin:$PATH
```
and save the file.
```bash
source ~/.zshenv
```
7. change the permissions.
```bash
chmod 744 ~/.zshenv
```
To apply this change, restart all open terminal sessions.

8. To install and set up CocoaPods, run the following commands:
```bash
sudo gem install cocoapods
```
9. Copy the following line and paste it at the end of your `~/.zshenv` file.
```bash
export PATH=$HOME/.gem/bin:$PATH
```
To apply this change, restart all open terminal sessions.

10. To verify your installation of all the components, run the following command.
```bash
flutter doctor
```
Troubleshoot Flutter doctor issues
```bash
flutter doctor -v
```
make sure `/Users/arshad/Library/Android/sdk/cmdline-tools/` cmdline-tools installed 
App setting ---> Setting>Android SDK -- SDK Tools section and install `Android SDK command-line Tools`
