```
Last login: Tue Oct 29 17:30:42 on ttys002
zsh compinit: insecure directories and files, run compaudit for list.
Ignore insecure directories and files and continue [y] or abort compinit [n]? y
arshad@arshad91 ~ % 
arshad@arshad91 ~ % export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"
arshad@arshad91 ~ % node -v
v14.16.0
arshad@arshad91 ~ % ndoe install 22
zsh: command not found: ndoe
arshad@arshad91 ~ % node install 22
internal/modules/cjs/loader.js:883
  throw err;
  ^

Error: Cannot find module '/Users/arshad/install'
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:880:15)
    at Function.Module._load (internal/modules/cjs/loader.js:725:27)
    at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:72:12)
    at internal/main/run_main_module.js:17:47 {
  code: 'MODULE_NOT_FOUND',
  requireStack: []
}
arshad@arshad91 ~ % node -v
v14.16.0
arshad@arshad91 ~ % nvm -v
0.40.0
arshad@arshad91 ~ % npm -v
6.14.11
arshad@arshad91 ~ % nvm install 22

Downloading and installing node v22.10.0...
Downloading https://nodejs.org/dist/v22.10.0/node-v22.10.0-darwin-x64.tar.xz...
######################################################################### 100.0%
Computing checksum with sha256sum
Checksums matched!
Now using node v22.10.0 (npm v10.9.0)
Creating default alias: default -> 22 (-> v22.10.0)
arshad@arshad91 ~ % node -v       
v22.10.0
arshad@arshad91 ~ % nvm -v
0.40.0
arshad@arshad91 ~ % npm -v
10.9.0
arshad@arshad91 ~ % cd Library/
Accessibility/                       Keychains/
Accounts/                            LanguageModeling/
Android/                             LaunchAgents/
AppleMediaServices/                  LockdownMode/
Application\ Scripts/                Logs/
Application\ Support/                Mail/
Assistant/                           Messages/
Assistants/                          Metadata/
Audio/                               Mozilla/
Autosave\ Information/               Passes/
Biome/                               PersonalizationPortrait/
Caches/                              Photos/
Calendars/                           PreferencePanes/
CallServices/                        Preferences/
ColorPickers/                        Printers/
Colors/                              PrivateCloudCompute/
Compositions/                        Safari/
Contacts/                            Saved\ Application\ State/
ContainerManager/                    Screen\ Savers/
Containers/                          Services/
CoreFollowUp/                        Sharing/
Daemon\ Containers/                  Shortcuts/
DataDeliveryServices/                Sounds/
Developer/                           Spelling/
DoNotDisturb/                        Spotlight/
DuetExpertCenter/                    StatusKit/
Favorites/                           Stickers/
Finance/                             Suggestions/
FontCollections/                     Thunderbird/
Fonts/                               Trial/
FrontBoard/                          UnifiedAssetFramework/
Google/                              Weather/
Group\ Containers/                   WebKit/
HTTPStorages/                        com.apple.aiml.instrumentation/
HomeKit/                             com.apple.bluetooth.services.cloud/
IdentityServices/                    com.apple.iTunesCloud/
Input\ Methods/                      com.apple.icloud.searchpartyd/
IntelligencePlatform/                com.apple.internal.ck/
Internet\ Plug-Ins/                  homeenergyd/
Keyboard\ Layouts/                   studentd/
KeyboardServices/                    
arshad@arshad91 ~ % cd Library/Java
cd: no such file or directory: Library/Java
arshad@arshad91 ~ % cd Library/
Accessibility/                       Keychains/
Accounts/                            LanguageModeling/
Android/                             LaunchAgents/
AppleMediaServices/                  LockdownMode/
Application\ Scripts/                Logs/
Application\ Support/                Mail/
Assistant/                           Messages/
Assistants/                          Metadata/
Audio/                               Mozilla/
Autosave\ Information/               Passes/
Biome/                               PersonalizationPortrait/
Caches/                              Photos/
Calendars/                           PreferencePanes/
CallServices/                        Preferences/
ColorPickers/                        Printers/
Colors/                              PrivateCloudCompute/
Compositions/                        Safari/
Contacts/                            Saved\ Application\ State/
ContainerManager/                    Screen\ Savers/
Containers/                          Services/
CoreFollowUp/                        Sharing/
Daemon\ Containers/                  Shortcuts/
DataDeliveryServices/                Sounds/
Developer/                           Spelling/
DoNotDisturb/                        Spotlight/
DuetExpertCenter/                    StatusKit/
Favorites/                           Stickers/
Finance/                             Suggestions/
FontCollections/                     Thunderbird/
Fonts/                               Trial/
FrontBoard/                          UnifiedAssetFramework/
Google/                              Weather/
Group\ Containers/                   WebKit/
HTTPStorages/                        com.apple.aiml.instrumentation/
HomeKit/                             com.apple.bluetooth.services.cloud/
IdentityServices/                    com.apple.iTunesCloud/
Input\ Methods/                      com.apple.icloud.searchpartyd/
IntelligencePlatform/                com.apple.internal.ck/
Internet\ Plug-Ins/                  homeenergyd/
Keyboard\ Layouts/                   studentd/
KeyboardServices/                    
arshad@arshad91 ~ % ls          
AndroidStudioProjects	Library			Public
Desktop			Movies			development
Documents		Music
Downloads		Pictures
arshad@arshad91 ~ % cd Library/
Accessibility/                       Keychains/
Accounts/                            LanguageModeling/
Android/                             LaunchAgents/
AppleMediaServices/                  LockdownMode/
Application\ Scripts/                Logs/
Application\ Support/                Mail/
Assistant/                           Messages/
Assistants/                          Metadata/
Audio/                               Mozilla/
Autosave\ Information/               Passes/
Biome/                               PersonalizationPortrait/
Caches/                              Photos/
Calendars/                           PreferencePanes/
CallServices/                        Preferences/
ColorPickers/                        Printers/
Colors/                              PrivateCloudCompute/
Compositions/                        Safari/
Contacts/                            Saved\ Application\ State/
ContainerManager/                    Screen\ Savers/
Containers/                          Services/
CoreFollowUp/                        Sharing/
Daemon\ Containers/                  Shortcuts/
DataDeliveryServices/                Sounds/
Developer/                           Spelling/
DoNotDisturb/                        Spotlight/
DuetExpertCenter/                    StatusKit/
Favorites/                           Stickers/
Finance/                             Suggestions/
FontCollections/                     Thunderbird/
Fonts/                               Trial/
FrontBoard/                          UnifiedAssetFramework/
Google/                              Weather/
Group\ Containers/                   WebKit/
HTTPStorages/                        com.apple.aiml.instrumentation/
HomeKit/                             com.apple.bluetooth.services.cloud/
IdentityServices/                    com.apple.iTunesCloud/
Input\ Methods/                      com.apple.icloud.searchpartyd/
IntelligencePlatform/                com.apple.internal.ck/
Internet\ Plug-Ins/                  homeenergyd/
Keyboard\ Layouts/                   studentd/
KeyboardServices/                    
arshad@arshad91 ~ % ls                        
AndroidStudioProjects	Library			Public
Desktop			Movies			development
Documents		Music
Downloads		Pictures
arshad@arshad91 ~ % cd Library/
Accessibility/                       Keychains/
Accounts/                            LanguageModeling/
Android/                             LaunchAgents/
AppleMediaServices/                  LockdownMode/
Application\ Scripts/                Logs/
Application\ Support/                Mail/
Assistant/                           Messages/
Assistants/                          Metadata/
Audio/                               Mozilla/
Autosave\ Information/               Passes/
Biome/                               PersonalizationPortrait/
Caches/                              Photos/
Calendars/                           PreferencePanes/
CallServices/                        Preferences/
ColorPickers/                        Printers/
Colors/                              PrivateCloudCompute/
Compositions/                        Safari/
Contacts/                            Saved\ Application\ State/
ContainerManager/                    Screen\ Savers/
Containers/                          Services/
CoreFollowUp/                        Sharing/
Daemon\ Containers/                  Shortcuts/
DataDeliveryServices/                Sounds/
Developer/                           Spelling/
DoNotDisturb/                        Spotlight/
DuetExpertCenter/                    StatusKit/
Favorites/                           Stickers/
Finance/                             Suggestions/
FontCollections/                     Thunderbird/
Fonts/                               Trial/
FrontBoard/                          UnifiedAssetFramework/
Google/                              Weather/
Group\ Containers/                   WebKit/
HTTPStorages/                        com.apple.aiml.instrumentation/
HomeKit/                             com.apple.bluetooth.services.cloud/
IdentityServices/                    com.apple.iTunesCloud/
Input\ Methods/                      com.apple.icloud.searchpartyd/
IntelligencePlatform/                com.apple.internal.ck/
Internet\ Plug-Ins/                  homeenergyd/
Keyboard\ Layouts/                   studentd/
KeyboardServices/                    
arshad@arshad91 ~ % cd Library/              
arshad@arshad91 Library % ls
Accessibility				Keychains
Accounts				LanguageModeling
Android					LaunchAgents
AppleMediaServices			LockdownMode
Application Scripts			Logs
Application Support			Mail
Assistant				Messages
Assistants				Metadata
Audio					Mozilla
Autosave Information			Passes
Biome					PersonalizationPortrait
Caches					Photos
Calendars				PreferencePanes
CallServices				Preferences
ColorPickers				Printers
Colors					PrivateCloudCompute
Compositions				Safari
Contacts				Saved Application State
ContainerManager			Screen Savers
Containers				Services
CoreFollowUp				Sharing
Daemon Containers			Shortcuts
DataDeliveryServices			Sounds
Developer				Spelling
DoNotDisturb				Spotlight
DuetExpertCenter			StatusKit
Favorites				Stickers
Finance					Suggestions
FontCollections				Thunderbird
Fonts					Trial
FrontBoard				UnifiedAssetFramework
Google					Weather
Group Containers			WebKit
HTTPStorages				com.apple.aiml.instrumentation
HomeKit					com.apple.bluetooth.services.cloud
IdentityServices			com.apple.iTunesCloud
Input Methods				com.apple.icloud.searchpartyd
IntelligencePlatform			com.apple.internal.ck
Internet Plug-Ins			homeenergyd
Keyboard Layouts			studentd
KeyboardServices
arshad@arshad91 Library % cd  
arshad@arshad91 ~ % /usr/libexec/java_home -V

Matching Java Virtual Machines (2):
    23.0.1 (x86_64) "Oracle Corporation" - "Java SE 23.0.1" /Library/Java/JavaVirtualMachines/jdk-23.jdk/Contents/Home
    21.0.5 (x86_64) "Oracle Corporation" - "Java SE 21.0.5" /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home
/Library/Java/JavaVirtualMachines/jdk-23.jdk/Contents/Home
arshad@arshad91 ~ % cd  /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/ 

arshad@arshad91 Contents % ls
Home		Info.plist	MacOS		_CodeSignature
arshad@arshad91 Contents % pwd
/Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents
arshad@arshad91 Contents % cd Home 
arshad@arshad91 Home % ls
LICENSE	README	bin	conf	include	jmods	legal	lib	man	release
arshad@arshad91 Home % pwd
/Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home
arshad@arshad91 Home % cd
arshad@arshad91 ~ % vi ~/.zshrc
arshad@arshad91 ~ % source ~/.zshrc
arshad@arshad91 ~ % vi ~/.zshrc    
arshad@arshad91 ~ % source ~/.zshrc
arshad@arshad91 ~ % echo $ANDROID_HOME
/Users/arshad/Library/Android/sdk
arshad@arshad91 ~ % echo $PATH        
/Users/arshad/.nvm/versions/node/v22.10.0/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Users/mohitkumar/Downloads/flutter/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/local/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/appleinternal/bin:/Library/Apple/usr/bin:/Users/arshad/.gem/bin:/Users/arshad/development/flutter/bin:/Users/arshad/Library/Android/sdk/emulator:/Users/arshad/Library/Android/sdk/platform-tools
arshad@arshad91 ~ % 
arshad@arshad91 ~ % npm install -g react-native-cli
npm warn deprecated glob@7.2.3: Glob versions prior to v9 are no longer supported
npm warn deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
npm warn deprecated rimraf@2.7.1: Rimraf versions prior to v4 are no longer supported

added 89 packages in 3s

41 packages are looking for funding
  run `npm fund` for details
arshad@arshad91 ~ % npm install -g react-native-cli

npm warn deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
npm warn deprecated rimraf@2.7.1: Rimraf versions prior to v4 are no longer supported
npm warn deprecated glob@7.2.3: Glob versions prior to v9 are no longer supported

changed 89 packages in 979ms

41 packages are looking for funding
  run `npm fund` for details
arshad@arshad91 ~ % npx react-native init MyNewProject

This will walk you through creating a new React Native project in /Users/arshad/MyNewProject
Installing react-native...
Consider installing yarn to make this faster: https://yarnpkg.com
npm warn deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
npm warn deprecated glob@7.2.3: Glob versions prior to v9 are no longer supported
npm warn deprecated @babel/plugin-proposal-class-properties@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-class-properties instead.
npm warn deprecated @babel/plugin-proposal-optional-chaining@7.21.0: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-optional-chaining instead.
npm warn deprecated rimraf@3.0.2: Rimraf versions prior to v4 are no longer supported
npm warn deprecated @babel/plugin-proposal-nullish-coalescing-operator@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-nullish-coalescing-operator instead.
npm warn deprecated rimraf@2.6.3: Rimraf versions prior to v4 are no longer supported

added 502 packages, and audited 503 packages in 17s

30 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
/Users/arshad/.nvm/versions/node/v22.10.0/lib/node_modules/react-native-cli/index.js:302
  cli.init(root, projectName);
      ^

TypeError: cli.init is not a function
    at run (/Users/arshad/.nvm/versions/node/v22.10.0/lib/node_modules/react-native-cli/index.js:302:7)
    at createProject (/Users/arshad/.nvm/versions/node/v22.10.0/lib/node_modules/react-native-cli/index.js:249:3)
    at init (/Users/arshad/.nvm/versions/node/v22.10.0/lib/node_modules/react-native-cli/index.js:200:5)
    at Object.<anonymous> (/Users/arshad/.nvm/versions/node/v22.10.0/lib/node_modules/react-native-cli/index.js:153:7)
    at Module._compile (node:internal/modules/cjs/loader:1546:14)
    at Object..js (node:internal/modules/cjs/loader:1689:10)
    at Module.load (node:internal/modules/cjs/loader:1318:32)
    at Function._load (node:internal/modules/cjs/loader:1128:12)
    at TracingChannel.traceSync (node:diagnostics_channel:315:14)
    at wrapModuleLoad (node:internal/modules/cjs/loader:218:24)

Node.js v22.10.0
arshad@arshad91 ~ % npm -v
10.9.0
arshad@arshad91 ~ % node -v
v22.10.0
arshad@arshad91 ~ % nvm -v
0.40.0
arshad@arshad91 ~ % nvm install 18
Downloading and installing node v18.20.4...
Downloading https://nodejs.org/dist/v18.20.4/node-v18.20.4-darwin-x64.tar.xz...
####################################################################################################################################################### 100.0%
Computing checksum with sha256sum
Checksums matched!
Now using node v18.20.4 (npm v10.7.0)
arshad@arshad91 ~ % nvm use 18
Now using node v18.20.4 (npm v10.7.0)
arshad@arshad91 ~ % mode -v
zsh: command not found: mode
arshad@arshad91 ~ % node -v
v18.20.4
arshad@arshad91 ~ % npx react-native init YourProjectName    

Need to install the following packages:
react-native@0.76.1
Ok to proceed? (y) y

npm warn deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
npm warn deprecated @babel/plugin-proposal-nullish-coalescing-operator@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-nullish-coalescing-operator instead.
npm warn deprecated @babel/plugin-proposal-class-properties@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-class-properties instead.
npm warn deprecated rimraf@2.6.3: Rimraf versions prior to v4 are no longer supported
npm warn deprecated @babel/plugin-proposal-optional-chaining@7.21.0: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-optional-chaining instead.
npm warn deprecated rimraf@3.0.2: Rimraf versions prior to v4 are no longer supported
npm warn deprecated glob@7.2.3: Glob versions prior to v9 are no longer supported

⚠️ The `init` command is deprecated.
The behavior will be changed on 12/31/2024 (62 days).

- Switch to npx @react-native-community/cli init for the identical behavior.
- Refer to the documentation for information about alternative tools: https://reactnative.dev/docs/getting-started

Running: npx @react-native-community/cli init

Need to install the following packages:
@react-native-community/cli@15.0.0
Ok to proceed? (y) y

                                                          
               ######                ######               
             ###     ####        ####     ###             
            ##          ###    ###          ##            
            ##             ####             ##            
            ##             ####             ##            
            ##           ##    ##           ##            
            ##         ###      ###         ##            
             ##  ########################  ##             
          ######    ###            ###    ######          
      ###     ##    ##              ##    ##     ###      
   ###         ## ###      ####      ### ##         ###   
  ##           ####      ########      ####           ##  
 ##             ###     ##########     ###             ## 
  ##           ####      ########      ####           ##  
   ###         ## ###      ####      ### ##         ###   
      ###     ##    ##              ##    ##     ###      
          ######    ###            ###    ######          
             ##  ########################  ##             
            ##         ###      ###         ##            
            ##           ##    ##           ##            
            ##             ####             ##            
            ##             ####             ##            
            ##          ###    ###          ##            
             ###     ####        ####     ###             
               ######                ######               
                                                          

              Welcome to React Native 0.76.1!                
                 Learn once, write anywhere               

✔ Downloading template
✔ Copying template
✔ Processing template
✔ Installing dependencies
✔ Do you want to install CocoaPods now? Only needed if you run your project in Xcode directly … no
info 💡 To enable automatic CocoaPods installation when building for iOS you can create react-native.config.js with automaticPodsInstallation field. 
For more details, see https://github.com/react-native-community/cli/blob/main/docs/projects.md#projectiosautomaticpodsinstallation
            

  
  Run instructions for Android:
    • Have an Android emulator running (quickest way to get started), or a device connected.
    • cd "/Users/arshad/YourProjectName" && npx react-native run-android
  
  Run instructions for iOS:
    • cd "/Users/arshad/YourProjectName/ios"
    
    • Install Cocoapods
      • bundle install # you need to run this only once in your project.
      • bundle exec pod install
      • cd ..
    
    • npx react-native run-ios
    - or -
    • Open YourProjectName/ios/YourProjectName.xcodeproj in Xcode or run "xed -b ios"
    • Hit the Run button
    
  Run instructions for macOS:
    • See https://aka.ms/ReactNativeGuideMacOS for the latest up-to-date instructions.
    
  
arshad@arshad91 ~ % ls
AndroidStudioProjects	Documents		Library			Music			Pictures		YourProjectName
Desktop			Downloads		Movies			MyNewProject		Public			development
arshad@arshad91 ~ % rm -rf MyNewProject                  
arshad@arshad91 ~ % ls
AndroidStudioProjects	Documents		Library			Music			Public			development
Desktop			Downloads		Movies			Pictures		YourProjectName
arshad@arshad91 ~ % npx react-native init myproject      

⚠️ The `init` command is deprecated.
The behavior will be changed on 12/31/2024 (62 days).

- Switch to npx @react-native-community/cli init for the identical behavior.
- Refer to the documentation for information about alternative tools: https://reactnative.dev/docs/getting-started

Running: npx @react-native-community/cli init

                                                          
               ######                ######               
             ###     ####        ####     ###             
            ##          ###    ###          ##            
            ##             ####             ##            
            ##             ####             ##            
            ##           ##    ##           ##            
            ##         ###      ###         ##            
             ##  ########################  ##             
          ######    ###            ###    ######          
      ###     ##    ##              ##    ##     ###      
   ###         ## ###      ####      ### ##         ###   
  ##           ####      ########      ####           ##  
 ##             ###     ##########     ###             ## 
  ##           ####      ########      ####           ##  
   ###         ## ###      ####      ### ##         ###   
      ###     ##    ##              ##    ##     ###      
          ######    ###            ###    ######          
             ##  ########################  ##             
            ##         ###      ###         ##            
            ##           ##    ##           ##            
            ##             ####             ##            
            ##             ####             ##            
            ##          ###    ###          ##            
             ###     ####        ####     ###             
               ######                ######               
                                                          

              Welcome to React Native 0.76.1!                
                 Learn once, write anywhere               

✔ Downloading template
✔ Copying template
✔ Processing template
✔ Installing dependencies
✔ Do you want to install CocoaPods now? Only needed if you run your project in Xcode directly … yes
✔ Installing Ruby Gems
✔ Installing CocoaPods dependencies  (this may take a few minutes)
info 💡 To enable automatic CocoaPods installation when building for iOS you can create react-native.config.js with automaticPodsInstallation field. 
For more details, see https://github.com/react-native-community/cli/blob/main/docs/projects.md#projectiosautomaticpodsinstallation
            

  
  Run instructions for Android:
    • Have an Android emulator running (quickest way to get started), or a device connected.
    • cd "/Users/arshad/myproject" && npx react-native run-android
  
  Run instructions for iOS:
    • cd "/Users/arshad/myproject"
    
    • npx react-native run-ios
    - or -
    • Open myproject/ios/myproject.xcworkspace in Xcode or run "xed -b ios"
    • Hit the Run button
    
  Run instructions for macOS:
    • See https://aka.ms/ReactNativeGuideMacOS for the latest up-to-date instructions.
    
  
arshad@arshad91 ~ % npx react-native init project1 

⚠️ The `init` command is deprecated.
The behavior will be changed on 12/31/2024 (62 days).

- Switch to npx @react-native-community/cli init for the identical behavior.
- Refer to the documentation for information about alternative tools: https://reactnative.dev/docs/getting-started

Running: npx @react-native-community/cli init

                                                          
               ######                ######               
             ###     ####        ####     ###             
            ##          ###    ###          ##            
            ##             ####             ##            
            ##             ####             ##            
            ##           ##    ##           ##            
            ##         ###      ###         ##            
             ##  ########################  ##             
          ######    ###            ###    ######          
      ###     ##    ##              ##    ##     ###      
   ###         ## ###      ####      ### ##         ###   
  ##           ####      ########      ####           ##  
 ##             ###     ##########     ###             ## 
  ##           ####      ########      ####           ##  
   ###         ## ###      ####      ### ##         ###   
      ###     ##    ##              ##    ##     ###      
          ######    ###            ###    ######          
             ##  ########################  ##             
            ##         ###      ###         ##            
            ##           ##    ##           ##            
            ##             ####             ##            
            ##             ####             ##            
            ##          ###    ###          ##            
             ###     ####        ####     ###             
               ######                ######               
                                                          

              Welcome to React Native 0.76.1!                
                 Learn once, write anywhere               

✔ Downloading template
✔ Copying template
✔ Processing template
✔ Installing dependencies
✔ Do you want to install CocoaPods now? Only needed if you run your project in Xcode directly … yes
✔ Installing Ruby Gems
✔ Installing CocoaPods dependencies  (this may take a few minutes)
info 💡 To enable automatic CocoaPods installation when building for iOS you can create react-native.config.js with automaticPodsInstallation field. 
For more details, see https://github.com/react-native-community/cli/blob/main/docs/projects.md#projectiosautomaticpodsinstallation
            

  
  Run instructions for Android:
    • Have an Android emulator running (quickest way to get started), or a device connected.
    • cd "/Users/arshad/project1" && npx react-native run-android
  
  Run instructions for iOS:
    • cd "/Users/arshad/project1"
    
    • npx react-native run-ios
    - or -
    • Open project1/ios/project1.xcworkspace in Xcode or run "xed -b ios"
    • Hit the Run button
    
  Run instructions for macOS:
    • See https://aka.ms/ReactNativeGuideMacOS for the latest up-to-date instructions.
    
  
arshad@arshad91 ~ % vi ~/.zshrc
arshad@arshad91 ~ % source ~/.zshrc

```

and 
```
Last login: Tue Oct 29 16:31:58 on ttys000
arshad@arshad91 ~ % vi ~/.zshenv
arshad@arshad91 ~ % flutter doctor

  ╔════════════════════════════════════════════════════════════════════════════╗
  ║                 Welcome to Flutter! - https://flutter.dev                  ║
  ║                                                                            ║
  ║ The Flutter tool uses Google Analytics to anonymously report feature usage ║
  ║ statistics and basic crash reports. This data is used to help improve      ║
  ║ Flutter tools over time.                                                   ║
  ║                                                                            ║
  ║ Flutter tool analytics are not sent on the very first run. To disable      ║
  ║ reporting, type 'flutter config --no-analytics'. To display the current    ║
  ║ setting, type 'flutter config'. If you opt out of analytics, an opt-out    ║
  ║ event will be sent, and then no further information will be sent by the    ║
  ║ Flutter tool.                                                              ║
  ║                                                                            ║
  ║ By downloading the Flutter SDK, you agree to the Google Terms of Service.  ║
  ║ The Google Privacy Policy describes how data is handled in this service.   ║
  ║                                                                            ║
  ║ Moreover, Flutter includes the Dart SDK, which may send usage metrics and  ║
  ║ crash reports to Google.                                                   ║
  ║                                                                            ║
  ║ Read about data we send with crash reports:                                ║
  ║ https://flutter.dev/to/crash-reporting                                     ║
  ║                                                                            ║
  ║ See Google's privacy policy:                                               ║
  ║ https://policies.google.com/privacy                                        ║
  ║                                                                            ║
  ║ To disable animations in this tool, use                                    ║
  ║ 'flutter config --no-cli-animations'.                                      ║
  ╚════════════════════════════════════════════════════════════════════════════╝


Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 3.24.4, on macOS 15.0.1 24A348 darwin-x64, locale en-IN)
[✗] Android toolchain - develop for Android devices
    ✗ Unable to locate Android SDK.
      Install Android Studio from: https://developer.android.com/studio/index.html
      On first launch it will assist you in installing the Android SDK components.
      (or visit https://flutter.dev/to/macos-android-setup for detailed instructions).
      If the Android SDK has been installed to a custom location, please use
      `flutter config --android-sdk` to update to that location.

[✓] Xcode - develop for iOS and macOS (Xcode 16.0)
[✓] Chrome - develop for the web
[✓] Android Studio (version 2024.2)
[✓] VS Code (version 1.94.2)
[✓] Connected device (2 available)
[✓] Network resources

! Doctor found issues in 1 category.
The Flutter CLI developer tool uses Google Analytics to report usage and diagnostic
data along with package dependencies, and crash reporting to send basic crash
reports. This data is used to help improve the Dart platform, Flutter framework,
and related tools.

Telemetry is not sent on the very first run. To disable reporting of telemetry,
run this terminal command:

    flutter --disable-analytics

If you opt out of telemetry, an opt-out event will be sent, and then no further
information will be sent. This data is collected in accordance with the Google
Privacy Policy (https://policies.google.com/privacy).

arshad@arshad91 ~ % flutter doctor -v
[✓] Flutter (Channel stable, 3.24.4, on macOS 15.0.1 24A348 darwin-x64, locale en-IN)
    • Flutter version 3.24.4 on channel stable at /Users/arshad/development/flutter
    • Upstream repository https://github.com/flutter/flutter.git
    • Framework revision 603104015d (5 days ago), 2024-10-24 08:01:25 -0700
    • Engine revision db49896cf2
    • Dart version 3.5.4
    • DevTools version 2.37.3

[✗] Android toolchain - develop for Android devices
    ✗ Unable to locate Android SDK.
      Install Android Studio from: https://developer.android.com/studio/index.html
      On first launch it will assist you in installing the Android SDK components.
      (or visit https://flutter.dev/to/macos-android-setup for detailed instructions).
      If the Android SDK has been installed to a custom location, please use
      `flutter config --android-sdk` to update to that location.


[✓] Xcode - develop for iOS and macOS (Xcode 16.0)
    • Xcode at /Applications/Xcode.app/Contents/Developer
    • Build 16A242d
    • CocoaPods version 1.16.0

[✓] Chrome - develop for the web
    • Chrome at /Applications/Google Chrome.app/Contents/MacOS/Google Chrome

[✓] Android Studio (version 2024.2)
    • Android Studio at /Applications/Android Studio.app/Contents
    • Flutter plugin can be installed from:
      🔨 https://plugins.jetbrains.com/plugin/9212-flutter
    • Dart plugin can be installed from:
      🔨 https://plugins.jetbrains.com/plugin/6351-dart
    • Java version OpenJDK Runtime Environment (build 21.0.3+-79915915-b509.11)

[✓] VS Code (version 1.94.2)
    • VS Code at /Applications/Visual Studio Code.app/Contents
    • Flutter extension can be installed from:
      🔨 https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter

[✓] Connected device (2 available)
    • macOS (desktop) • macos  • darwin-x64     • macOS 15.0.1 24A348 darwin-x64
    • Chrome (web)    • chrome • web-javascript • Google Chrome 130.0.6723.70

[✓] Network resources
    • All expected network resources are available.

! Doctor found issues in 1 category.
arshad@arshad91 ~ % flutter doctor   
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 3.24.4, on macOS 15.0.1 24A348 darwin-x64, locale en-IN)
[✗] Android toolchain - develop for Android devices
    ✗ Unable to locate Android SDK.
      Install Android Studio from: https://developer.android.com/studio/index.html
      On first launch it will assist you in installing the Android SDK components.
      (or visit https://flutter.dev/to/macos-android-setup for detailed instructions).
      If the Android SDK has been installed to a custom location, please use
      `flutter config --android-sdk` to update to that location.

[✓] Xcode - develop for iOS and macOS (Xcode 16.0)
[✓] Chrome - develop for the web
[✓] Android Studio (version 2024.2)
[✓] VS Code (version 1.94.2)
[✓] Connected device (2 available)
[✓] Network resources

! Doctor found issues in 1 category.
arshad@arshad91 ~ % flutter config --android-sdk
Missing argument for "android-sdk".


Run 'flutter -h' (or 'flutter <command> -h') for available flutter commands and options.
arshad@arshad91 ~ % flutter -h
Manage your Flutter app development.

Common commands:

  flutter create <output directory>
    Create a new Flutter project in the specified directory.

  flutter run [options]
    Run your Flutter application on an attached device or in an emulator.

Usage: flutter <command> [arguments]

Global options:
-h, --help                  Print this usage information.
-v, --verbose               Noisy logging, including all shell commands executed.
                            If used with "--help", shows hidden options. If used with "flutter doctor", shows additional diagnostic information. (Use "-vv" to
                            force verbose logging in those cases.)
-d, --device-id             Target device id or name (prefixes allowed).
    --version               Reports the version of this tool.
    --enable-analytics      Enable telemetry reporting each time a flutter or dart command runs.
    --disable-analytics     Disable telemetry reporting each time a flutter or dart command runs, until it is re-enabled.
    --suppress-analytics    Suppress analytics reporting for the current CLI invocation.

Available commands:

Flutter SDK
  bash-completion   Output command line shell completion setup scripts.
  channel           List or switch Flutter channels.
  config            Configure Flutter settings.
  doctor            Show information about the installed tooling.
  downgrade         Downgrade Flutter to the last active version for the current channel.
  precache          Populate the Flutter tool's cache of binary artifacts.
  upgrade           Upgrade your copy of Flutter.

Project
  analyze           Analyze the project's Dart code.
  assemble          Assemble and build Flutter resources.
  build             Build an executable app or install bundle.
  clean             Delete the build/ and .dart_tool/ directories.
  create            Create a new Flutter project.
  drive             Run integration tests for the project on an attached device or emulator.
  gen-l10n          Generate localizations for the current project.
  pub               Commands for managing Flutter packages.
  run               Run your Flutter app on an attached device.
  test              Run Flutter unit tests for the current project.

Tools & Devices
  attach            Attach to a running app.
  custom-devices    List, reset, add and delete custom devices.
  devices           List all connected devices.
  emulators         List, launch and create emulators.
  install           Install a Flutter app on an attached device.
  logs              Show log output for running Flutter apps.
  screenshot        Take a screenshot from a connected device.
  symbolize         Symbolize a stack trace from an AOT-compiled Flutter app.

Run "flutter help <command>" for more information about a command.
Run "flutter help -v" for verbose help output, including less commonly used options.
arshad@arshad91 ~ % flutter config --android-sdk
Missing argument for "android-sdk".


Run 'flutter -h' (or 'flutter <command> -h') for available flutter commands and options.
arshad@arshad91 ~ % cd Library 
arshad@arshad91 Library % sl
zsh: command not found: sl
arshad@arshad91 Library % ls
Accessibility				CoreFollowUp				KeyboardServices			Services
Accounts				Daemon Containers			Keychains				Sharing
Android					DataDeliveryServices			LanguageModeling			Shortcuts
AppleMediaServices			Developer				LaunchAgents				Sounds
Application Scripts			DoNotDisturb				LockdownMode				Spelling
Application Support			DuetExpertCenter			Logs					Spotlight
Assistant				Favorites				Mail					StatusKit
Assistants				Finance					Messages				Stickers
Audio					FontCollections				Metadata				Suggestions
Autosave Information			Fonts					Mozilla					Thunderbird
Biome					FrontBoard				Passes					Trial
Caches					Google					PersonalizationPortrait			UnifiedAssetFramework
Calendars				Group Containers			Photos					Weather
CallServices				HTTPStorages				PreferencePanes				com.apple.aiml.instrumentation
ColorPickers				HomeKit					Preferences				com.apple.bluetooth.services.cloud
Colors					IdentityServices			Printers				com.apple.iTunesCloud
Compositions				Input Methods				PrivateCloudCompute			com.apple.icloud.searchpartyd
Contacts				IntelligencePlatform			Safari					com.apple.internal.ck
ContainerManager			Internet Plug-Ins			Saved Application State			homeenergyd
Containers				Keyboard Layouts			Screen Savers				studentd
arshad@arshad91 Library % cd Android 
arshad@arshad91 Android % ls
sdk
arshad@arshad91 Android % cd sdk 
arshad@arshad91 sdk % pwd
/Users/arshad/Library/Android/sdk
arshad@arshad91 sdk % cd
arshad@arshad91 ~ % flutter dockor
Could not find a command named "dockor".

Did you mean one of these?
  doctor



Run 'flutter -h' (or 'flutter <command> -h') for available flutter commands and options.
arshad@arshad91 ~ % flutter doctor
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 3.24.4, on macOS 15.0.1 24A348 darwin-x64, locale en-IN)
[!] Android toolchain - develop for Android devices (Android SDK version 34.0.0)
    ✗ cmdline-tools component is missing
      Run `path/to/sdkmanager --install "cmdline-tools;latest"`
      See https://developer.android.com/studio/command-line for more details.
    ✗ Android license status unknown.
      Run `flutter doctor --android-licenses` to accept the SDK licenses.
      See https://flutter.dev/to/macos-android-setup for more details.
[✓] Xcode - develop for iOS and macOS (Xcode 16.0)
[✓] Chrome - develop for the web
[✓] Android Studio (version 2024.2)
[✓] VS Code (version 1.94.2)
[✓] Connected device (2 available)
[✓] Network resources

! Doctor found issues in 1 category.
arshad@arshad91 ~ % flutter doctor --android-licenses 
Android sdkmanager not found. Update to the latest Android SDK and ensure that the cmdline-tools are installed to resolve this.
arshad@arshad91 ~ % cd Library/Android 
arshad@arshad91 Android % ls
sdk
arshad@arshad91 Android % cd sdk 
arshad@arshad91 sdk % ls
build-tools	emulator	licenses	platform-tools	platforms	sources		system-images
arshad@arshad91 sdk % ls
build-tools	emulator	licenses	platform-tools	platforms	sources		system-images
arshad@arshad91 sdk %  --install "cmdline-tools;latest
dquote> 
dquote> 
dquote> 
dquote> 
dquote> exit                            
dquote> 
dquote> 
dquote> 
dquote> 
arshad@arshad91 sdk % ls
build-tools	emulator	licenses	platform-tools	platforms	sources		system-images
arshad@arshad91 sdk % pwd 
/Users/arshad/Library/Android/sdk
arshad@arshad91 sdk % ls
build-tools	emulator	licenses	platform-tools	platforms	sources		system-images
arshad@arshad91 sdk % cd build-tools 
arshad@arshad91 build-tools % ls
34.0.0	35.0.0
arshad@arshad91 build-tools % cd ..
arshad@arshad91 sdk % cd platform
cd: no such file or directory: platform
arshad@arshad91 sdk % cd platform-tools 
arshad@arshad91 platform-tools % ls
NOTICE.txt		fastboot		make_f2fs		mke2fs.conf		sqlite3
adb			hprof-conv		make_f2fs_casefold	package.xml
etc1tool		lib64			mke2fs			source.properties
arshad@arshad91 platform-tools % cd ..
arshad@arshad91 sdk % pwd
/Users/arshad/Library/Android/sdk
arshad@arshad91 sdk % ls
build-tools	emulator	licenses	platform-tools	platforms	sources		system-images
arshad@arshad91 sdk % ls
build-tools	cmdline-tools	emulator	licenses	platform-tools	platforms	sources		system-images
arshad@arshad91 sdk % cd cmdline-tools 
arshad@arshad91 cmdline-tools % ls
latest
arshad@arshad91 cmdline-tools % ls 
latest
arshad@arshad91 cmdline-tools % cd latest 
arshad@arshad91 latest % ls
NOTICE.txt		bin			lib			package.xml		source.properties
arshad@arshad91 latest % cd bin 
arshad@arshad91 bin % ls
apkanalyzer		d8			profgen			resourceshrinker	screenshot2
avdmanager		lint			r8			retrace			sdkmanager
arshad@arshad91 bin % cd s
cd: no such file or directory: s
arshad@arshad91 bin % cd sdkmanager 
cd: not a directory: sdkmanager
arshad@arshad91 bin % ls
apkanalyzer		d8			profgen			resourceshrinker	screenshot2
avdmanager		lint			r8			retrace			sdkmanager
arshad@arshad91 bin % ~/Library/Android/sdk/cmdline-tools/latest/bin/sdkmanager --install "cmdline-tools;latest"

Warning: Errors during XML parse:                                               
Warning: Additionally, the fallback loader failed to parse the XML.             
[=======================================] 100% Computing updates...             

arshad@arshad91 bin % /sdkmanager --install "cmdline-tools;latest" 

zsh: no such file or directory: /sdkmanager
arshad@arshad91 bin % ls    
apkanalyzer		d8			profgen			resourceshrinker	screenshot2
avdmanager		lint			r8			retrace			sdkmanager
arshad@arshad91 bin % cd sdkmanager --install "cmdline-tools;latest"
cd: too many arguments
arshad@arshad91 bin % sdkmanager --install "cmdline-tools;latest" 
zsh: command not found: sdkmanager
arshad@arshad91 bin % ./sdkmanager --install "cmdline-tools;latest"

Warning: Errors during XML parse:                                               
Warning: Additionally, the fallback loader failed to parse the XML.             
[=======================================] 100% Computing updates...             

arshad@arshad91 bin % cd
arshad@arshad91 ~ % cd Library/Android/sdk/
arshad@arshad91 sdk % ls
build-tools	cmdline-tools	emulator	licenses	platform-tools	platforms	sources		system-images
arshad@arshad91 sdk % ./sdkmanager --update

zsh: no such file or directory: ./sdkmanager
arshad@arshad91 sdk % cd cmdline-tools/latest/bin       
arshad@arshad91 bin % ls
apkanalyzer		d8			profgen			resourceshrinker	screenshot2
avdmanager		lint			r8			retrace			sdkmanager
arshad@arshad91 bin % ./sdkmanager --update

Warning: Errors during XML parse:                                               
Warning: Additionally, the fallback loader failed to parse the XML.             
[===                                    ] 10% Computing updates...              
No updates available
[=======================================] 100% Computing updates...             

arshad@arshad91 bin % pwd
/Users/arshad/Library/Android/sdk/cmdline-tools/latest/bin
arshad@arshad91 bin % cd
arshad@arshad91 ~ % cd myproject 
arshad@arshad91 myproject % ls
App.tsx			android			jest.config.js		tsconfig.json
Gemfile			app.json		metro.config.js		vendor
Gemfile.lock		babel.config.js		node_modules
README.md		index.js		package-lock.json
__tests__		ios			package.json
arshad@arshad91 myproject % pwd
/Users/arshad/myproject
arshad@arshad91 myproject % 

arshad@arshad91 myproject % 
arshad@arshad91 myproject % npx react-native run-ios
info Found Xcode workspace "myproject.xcworkspace"
info No booted devices or simulators found. Launching first available simulator...
info Launching iPhone SE (3rd generation) (iOS 18.0)
info Building (using "xcodebuild -workspace myproject.xcworkspace -configuration Debug -scheme myproject -destination id=B98826FE-441A-4DE8-B594-66F73C83FEFC")
success Successfully built the app
--- xcodebuild: WARNING: Using the first of multiple matching destinations:
{ platform:iOS Simulator, id:dvtdevice-DVTiOSDeviceSimulatorPlaceholder-iphonesimulator:placeholder, name:Any iOS Simulator Device }
{ platform:iOS Simulator, id:BFB2675F-9A16-454B-B691-FE80E328480F, OS:18.0, name:iPad (10th generation) }
{ platform:iOS Simulator, id:16438292-42FF-4647-963A-062A01018696, OS:18.0, name:iPad Air 11-inch (M2) }
{ platform:iOS Simulator, id:D2123BFB-8843-4D44-899F-2495DF2CA9EB, OS:18.0, name:iPad Air 13-inch (M2) }
{ platform:iOS Simulator, id:20993C29-A235-45CE-908C-66E03943CDD3, OS:18.0, name:iPad Pro 11-inch (M4) }
{ platform:iOS Simulator, id:3EA37E06-2073-443D-9372-9D315865D947, OS:18.0, name:iPad Pro 13-inch (M4) }
{ platform:iOS Simulator, id:31E9D1C7-334F-436A-98F3-6C0C59FC02F6, OS:18.0, name:iPad mini (6th generation) }
{ platform:iOS Simulator, id:D4A1C64A-3B58-47F6-86F5-553031B17376, OS:18.0, name:iPhone 16 }
{ platform:iOS Simulator, id:92C027AC-5BD4-4C0B-8302-567BA0D1F6F5, OS:18.0, name:iPhone 16 Plus }
{ platform:iOS Simulator, id:F011E500-0BE0-4939-B76B-8277AF0918E0, OS:18.0, name:iPhone 16 Pro }
{ platform:iOS Simulator, id:F42203C1-6688-423E-8C79-F42D45BAC4FB, OS:18.0, name:iPhone 16 Pro Max }
{ platform:iOS Simulator, id:B98826FE-441A-4DE8-B594-66F73C83FEFC, OS:18.0, name:iPhone SE (3rd generation) }
{ platform:iOS, id:dvtdevice-DVTiPhonePlaceholder-iphoneos:placeholder, name:Any iOS Device }
info Installing "/Users/arshad/Library/Developer/Xcode/DerivedData/myproject-eqfbeqwldljehtbrzrrpjubpsczm/Build/Products/Debug-iphonesimulator/myproject.app
info Launching "org.reactjs.native.example.myproject"
success Successfully launched the app
arshad@arshad91 myproject % cd 
arshad@arshad91 ~ % ls
AndroidStudioProjects	Library			Public			project1
Desktop			Movies			YourProjectName
Documents		Music			development
Downloads		Pictures		myproject
arshad@arshad91 ~ % cd project1 
arshad@arshad91 project1 % npx react-native run-android
/bin/sh: adb: command not found
info Launching emulator...
error Failed to launch emulator. Reason: No emulators found as an output of `emulator -list-avds`.
warn Please launch an emulator manually or connect a device. Otherwise app may fail to launch.
info Installing the app...
Downloading https://services.gradle.org/distributions/gradle-8.10.2-all.zip
.....................10%......................20%......................30%.....................40%......................50%......................60%......................70%.....................80%......................90%......................100%

Welcome to Gradle 8.10.2!

Here are the highlights of this release:
 - Support for Java 23
 - Faster configuration cache
 - Better configuration cache reports

For more details see https://docs.gradle.org/8.10.2/release-notes.html

Starting a Gradle Daemon (subsequent builds will be faster)
13 actionable tasks: 13 executed

info 💡 Tip: Make sure that you have set up your development environment correctly, by running npx react-native doctor. To read more about doctor command visit: https://github.com/react-native-community/cli/blob/main/packages/cli-doctor/README.md#doctor 


FAILURE: Build failed with an exception.

* What went wrong:
A problem occurred configuring project ':app'.
> SDK location not found. Define a valid SDK location with an ANDROID_HOME environment variable or by setting the sdk.dir path in your project's local properties file at '/Users/arshad/project1/android/local.properties'.

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.
> Get more help at https://help.gradle.org.

BUILD FAILED in 2m 49s
error Failed to install the app. Command failed with exit code 1: ./gradlew app:installDebug -PreactNativeDevServerPort=8081 FAILURE: Build failed with an exception. * What went wrong:
A problem occurred configuring project ':app'.
> SDK location not found. Define a valid SDK location with an ANDROID_HOME environment variable or by setting the sdk.dir path in your project's local properties file at '/Users/arshad/project1/android/local.properties'. * Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.
> Get more help at https://help.gradle.org. BUILD FAILED in 2m 49s.
info Run CLI with --verbose flag for more details.
arshad@arshad91 project1 % 
```
and. 
```
Last login: Tue Oct 29 16:24:18 on ttys000
arshad@arshad91 ~ % sudo gem install cocoapods
Password:
sudo: no password was provided
sudo: a password is required
arshad@arshad91 ~ % su wadmin
Password:
wadmin@arshad91 arshad % sudo gem install cocoapods
Password:

Fetching cocoapods-core-1.16.0.gem
Fetching xcodeproj-1.26.0.gem
Fetching cocoapods-1.16.0.gem
Fetching nanaimo-0.4.0.gem
Successfully installed nanaimo-0.4.0
Successfully installed xcodeproj-1.26.0
Successfully installed cocoapods-core-1.16.0
Successfully installed cocoapods-1.16.0
Parsing documentation for nanaimo-0.4.0
Installing ri documentation for nanaimo-0.4.0
Parsing documentation for xcodeproj-1.26.0
Installing ri documentation for xcodeproj-1.26.0
Parsing documentation for cocoapods-core-1.16.0
Installing ri documentation for cocoapods-core-1.16.0
Parsing documentation for cocoapods-1.16.0
Installing ri documentation for cocoapods-1.16.0
Done installing documentation for nanaimo, xcodeproj, cocoapods-core, cocoapods after 3 seconds
4 gems installed
wadmin@arshad91 arshad % 
wadmin@arshad91 arshad % cd
wadmin@arshad91 ~ % ls
Desktop		Documents	Downloads	Library		Movies		Music		Pictures	Public
wadmin@arshad91 ~ % pwd
/Users/wadmin
wadmin@arshad91 ~ % curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash

  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 16555  100 16555    0     0  47442      0 --:--:-- --:--:-- --:--:-- 47435
=> Downloading nvm from git to '/Users/wadmin/.nvm'
=> Cloning into '/Users/wadmin/.nvm'...
remote: Enumerating objects: 378, done.
remote: Counting objects: 100% (378/378), done.
remote: Compressing objects: 100% (326/326), done.
remote: Total 378 (delta 43), reused 164 (delta 25), pack-reused 0 (from 0)
Receiving objects: 100% (378/378), 375.83 KiB | 4.04 MiB/s, done.
Resolving deltas: 100% (43/43), done.
* (HEAD detached at FETCH_HEAD)
  master
=> Compressing and cleaning up git repository

=> Profile not found. Tried ~/.bashrc, ~/.bash_profile, ~/.zprofile, ~/.zshrc, and ~/.profile.
=> Create one of them and run this script again
   OR
=> Append the following lines to the correct file yourself:

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm

=> Close and reopen your terminal to start using nvm or run the following to use it now:

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
wadmin@arshad91 ~ % export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
wadmin@arshad91 ~ % nvm install 22

Downloading and installing node v22.10.0...
Downloading https://nodejs.org/dist/v22.10.0/node-v22.10.0-darwin-x64.tar.xz...
########################################################################################################################### 100.0%
Computing checksum with sha256sum
Checksums matched!
Now using node v22.10.0 (npm v10.9.0)
Creating default alias: default -> 22 (-> v22.10.0)
wadmin@arshad91 ~ % node -v
v22.10.0
wadmin@arshad91 ~ % npm -v
10.9.0
wadmin@arshad91 ~ % 
```
after project run open cli 
```
Last login: Wed Oct 30 11:04:10 on ttys003
/Users/arshad/project1/node_modules/.generated/launchPackager.command ; exit;
zsh compinit: insecure directories and files, run compaudit for list.
Ignore insecure directories and files and continue [y] or abort compinit [n]? compinit: initialization aborted
complete:13: command not found: compdef
arshad@arshad91 ~ % Users/arshad/project1/node_modules/.generated/launchPackager.command ; exit;
zsh: no such file or directory: Users/arshad/project1/node_modules/.generated/launchPackager.command

Saving session...
...copying shared history...
...saving history...truncating history files...
...completed.

[Process completed]
```

runproject
```
arshad@arshad91 project %       cd            
arshad@arshad91 ~ % npx react-native@latest init project1

Need to install the following packages:
react-native@0.76.1
Ok to proceed? (y) y

npm warn deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
npm warn deprecated @babel/plugin-proposal-nullish-coalescing-operator@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-nullish-coalescing-operator instead.
npm warn deprecated @babel/plugin-proposal-class-properties@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-class-properties instead.
npm warn deprecated rimraf@2.6.3: Rimraf versions prior to v4 are no longer supported
npm warn deprecated @babel/plugin-proposal-optional-chaining@7.21.0: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-optional-chaining instead.
npm warn deprecated rimraf@3.0.2: Rimraf versions prior to v4 are no longer supported
npm warn deprecated glob@7.2.3: Glob versions prior to v9 are no longer supported

⚠️ The `init` command is deprecated.
The behavior will be changed on 12/31/2024 (62 days).

- Switch to npx @react-native-community/cli init for the identical behavior.
- Refer to the documentation for information about alternative tools: https://reactnative.dev/docs/getting-started

Running: npx @react-native-community/cli init

                                                          
               ######                ######               
             ###     ####        ####     ###             
            ##          ###    ###          ##            
            ##             ####             ##            
            ##             ####             ##            
            ##           ##    ##           ##            
            ##         ###      ###         ##            
             ##  ########################  ##             
          ######    ###            ###    ######          
      ###     ##    ##              ##    ##     ###      
   ###         ## ###      ####      ### ##         ###   
  ##           ####      ########      ####           ##  
 ##             ###     ##########     ###             ## 
  ##           ####      ########      ####           ##  
   ###         ## ###      ####      ### ##         ###   
      ###     ##    ##              ##    ##     ###      
          ######    ###            ###    ######          
             ##  ########################  ##             
            ##         ###      ###         ##            
            ##           ##    ##           ##            
            ##             ####             ##            
            ##             ####             ##            
            ##          ###    ###          ##            
             ###     ####        ####     ###             
               ######                ######               
                                                          

              Welcome to React Native 0.76.1!                
                 Learn once, write anywhere               

✔ Downloading template
✔ Copying template
✔ Processing template
✔ Installing dependencies
✔ Do you want to install CocoaPods now? Only needed if you run your project in Xcode directly … yes
✔ Installing Ruby Gems
✔ Installing CocoaPods dependencies  (this may take a few minutes)
info 💡 To enable automatic CocoaPods installation when building for iOS you can create react-native.config.js with automaticPodsInstallation field. 
For more details, see https://github.com/react-native-community/cli/blob/main/docs/projects.md#projectiosautomaticpodsinstallation
            

  
  Run instructions for Android:
    • Have an Android emulator running (quickest way to get started), or a device connected.
    • cd "/Users/arshad/project1" && npx react-native run-android
  
  Run instructions for iOS:
    • cd "/Users/arshad/project1"
    
    • npx react-native run-ios
    - or -
    • Open project1/ios/project1.xcworkspace in Xcode or run "xed -b ios"
    • Hit the Run button
    
  Run instructions for macOS:
    • See https://aka.ms/ReactNativeGuideMacOS for the latest up-to-date instructions.
    

```