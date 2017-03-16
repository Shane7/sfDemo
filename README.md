"# sfDemo" 

power shell command samples used with this app and the dev cluster:

Connect-ServiceFabricCluster localhost:19000

Copy-ServiceFabricApplicationPackage -ApplicationPackagePath 'C:\code\gitsfDemo2\sfDemo\nodeApp' -ImageStoreConnectionString 'file:C:\SfDevCluster\Data\ImageStoreShare' -ApplicationPackagePathInImageStore 'NodeAppType'
Register-ServiceFabricApplicationType -ApplicationPathInImageStore 'NodeAppType'

Start-ServiceFabricApplicationUpgrade -ApplicationName fabric:/NodeAppType -ApplicationTypeVersion "2.1" -UnmonitoredAuto
