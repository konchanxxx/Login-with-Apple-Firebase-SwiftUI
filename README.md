# Login with Apple Firebase SwiftUI

I made this SwiftUI component to handle logging in with Apple to Firebase.

# Demo Gif

<p align="center"><img src="https://raw.githubusercontent.com/joehinkle11/Login-with-Apple-Firebase-SwiftUI/master/demo.gif"/></p>

# Usage in SwiftUI

```swift
struct ContentView: View {
    var body: some View {
        SignInWithAppleToFirebase({ response in
            if response == .success {
                print("logged into Firebase through Apple!")
            } else if response == .error {
                print("error. Maybe the user cancelled or there's no internet")
            }
        })
    }
}
```

# Setup

 1. Copy the entirety of the `SignInWithAppleToFirebase` folder to your repo. https://github.com/joehinkle11/Login-with-Apple-Firebase-SwiftUI/tree/master/LoginWithAppleFirebaseSwiftUI/SignInWithAppleToFirebase
 2. Add Firebase to your project https://firebase.google.com/docs/ios/setup?authuser=0
 3. Add sign in with Apple as a valid login method on your Firebase project at this link https://console.firebase.google.com/u/0/project/<YOUR_FIREBASE_PROJECT_ID>/authentication/providers
 
<p align="center"><img src="https://raw.githubusercontent.com/joehinkle11/Login-with-Apple-Firebase-SwiftUI/master/example3.png"/></p>
 
 4. Make sure you open the Xcode workspace generated by Cocopods (this is detailed in the Firebase tutorial in step 2)
 5. Add Sign In with Apple to your app's id configuration at https://developer.apple.com/account/resources/identifiers/list
Remove

<p align="center"><img src="https://raw.githubusercontent.com/joehinkle11/Login-with-Apple-Firebase-SwiftUI/master/example0.png"/></p>

 6. Add Sign in with Apple to your project's capabilities
 
<p align="center"><img src="https://raw.githubusercontent.com/joehinkle11/Login-with-Apple-Firebase-SwiftUI/master/example1.png"/></p>
<p align="center"><img src="https://raw.githubusercontent.com/joehinkle11/Login-with-Apple-Firebase-SwiftUI/master/example2.png"/></p>
 
 7. Add the `SignInWithAppleToFirebase` button from this codebase to your view

<p align="center"><img src="https://raw.githubusercontent.com/joehinkle11/Login-with-Apple-Firebase-SwiftUI/master/LoginWithAppleFirebaseSwiftUI/Assets.xcassets/example.imageset/button.png"/></p>

 8. Now when users click on the button, it will sign them into Firebase using sign in with Apple
 
# Gotchas

 - You need a GoogleService-Info.plist file to compile this codebase. Go through the setup process on Firebase
 - You also need to have Cocopods and run `pod install`

# Tutorials/code used

 - https://firebase.google.com/docs/auth/ios/apple?authuser=0
 - https://www.raywenderlich.com/4875322-sign-in-with-apple-using-swiftui
