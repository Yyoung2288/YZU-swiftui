
<h1>SafeView<h1>

```SwiftUI
import SwiftUI


struct SafeView: View{
@State var count:Int = 0
    var body: some View{
        VStack{
            Button(action: {
                count+=1
            }, label: {
                Image("木魚")
            })
            Text(String(count))
                .padding(.all,10)
                .frame(width: 150, height: 120, alignment: .center)
                .font(.system(size: 100))
            
        }
    }
}



```
<h1>透過敲打木魚累積陰德<h1>
<img src="https://raw.githubusercontent.com/Yyoung2288/YZU-swiftui/main/SafeView.PNG">




   


