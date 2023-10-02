<h1>HW1<h1>

```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        Image("Selfie")
            .resizable()
            .aspectRatio( contentMode: .fit)
            .frame(width: 200,height: 200,alignment:.bottom)
        Form {
            Text("姓名： 劉子揚")
            Text("學號：1101509")
            Text("興趣： 打排球")
                .overlay(
                    Image(systemName: "volleyball")
                        .resizable()
                        .scaledToFit()
                        .position(CGPoint(x: 125.0, y: 10.0))
                        .foregroundColor(/*@START_MENU_TOKEN@*/.blue/*@END_MENU_TOKEN@*/)
                ) 
            Text("我的一句話：請多多指教")
            
        }
    }
}
struct Content_Previews: PreviewProvider {
    static var previews: some View {
        Text("Homework1")
            .foregroundColor(.blue)
    }
}
im


```

<img src="https://raw.githubusercontent.com/Yyoung2288/YZU-swiftui/main/IMG_0236.jpeg">



   
