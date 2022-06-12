# [MySwiftPackage](https://medium.com/@paigeshin1991/swift-package-manager-manifest-file-tutorial-that-nobody-tells-you-about-e69781f582b2)

A description of this package.
```swift
let package = Package(
    name: "MySwiftPackage",
    platforms: [
        .iOS(.v14), .macOS(.v11), .watchOS(.v8)
    ],
    products: [
        // Products define the executables and libraries a package produces, and make them visible to other packages.
        .library(
            name: "MySwiftPackage",
            targets: ["MySwiftPackage"]),
    ],
    dependencies: [
        // Dependencies declare other packages that this package depends on.
        .package(url: "https://github.com/Alamofire/Alamofire.git", .upToNextMajor(from: "5.6.1"))
    ],
    targets: [
        // Targets are the basic building blocks of a package. A target can define a module or a test suite.
        // Targets can depend on other targets in this package, and on products in packages this package depends on.
        .target(
            name: "MySwiftPackage",
            dependencies: [
                "Alamofire"
            ],
            path: "Sources"
        )
        ,
        .testTarget(
            name: "MySwiftPackageTests",
            dependencies: ["MySwiftPackage"]),
    ]
)
```
