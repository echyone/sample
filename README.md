# sample

We have a Swift/Objective C project to generate a framework fro public distribution. The project imports several Swift only internally produced libraries using Cocoapods. Our framework project compiles and works in Objective C files in an app. However, importing the framework into a Swift file results in a compile error that a library cannot be loaded.

This sample demonstrates the problem. We must use use_modular_headers! so that we dont't have to distriibute and expose API's for the private libraries we use in the framework. In Test.swift commenting out import sample will allow the app to compile and run. ViewController is able to import and use both the Swift and Objective C classes and methods in the framework.

