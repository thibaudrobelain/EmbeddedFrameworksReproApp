A repro app for an embedded frameworks problem in CocoaPods

Repro steps:  
Run `pod install`, open ReproApp.xcworkspace  
Run ReproApp in Release configuration  

Either check the build target dir:  
Check the build log to get the target build dir frameworks' path (I print it at the bottom)  
Open, verify Alamofire.framework is there, when it's explicitly not whitelisted in "Release"  

Or check the Embed Frameworks shell script:  
`subl Pods/Target\ Support\ Files/Pods-ReproAppAbstract-ReproApp/Pods-ReproAppAbstract-ReproApp-frameworks.sh`  
At the bottom, you can see Alamofire will be copied for release builds

Uncomment the Alamofire pod target for ReproApp in Podfile  
Do the same steps again  
Verify Alamofire.framework has disappeared from either the build target dir or the embed frameworks script, as expected.