# Uncomment the next line to define a global platform for your project

platform :ios, '10.0'
use_frameworks!

workspace 'ReproApp.xcworkspace'

abstract_target 'ReproAppAbstract' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  target 'EmbeddedFramework' do
    project './Modules/EmbeddedFramework/EmbeddedFramework.xcodeproj'
    pod 'Alamofire', :configurations => ['Debug']
  end

  # Pods for ReproApp
  target 'ReproApp' do
    # Uncomment, run pod install and then check the Release builds Frameworks/ folder
    # pod 'Alamofire', :configurations => ['Debug']
  end
end
