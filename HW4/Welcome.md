<h1>WelcomeView<h1>

```SwiftUI
import SwiftUI
struct WelcomeView: View{
    var body: some View{
        VStack{
            Image("證件照")
                .resizable()
                .frame(width: 300, height:400)
                .aspectRatio(contentMode: .fit)
            Text("元智大學資工系")
                .fontWeight(.heavy).lineSpacing(20)
                .font(.system(size: 32.0))
                .foregroundColor(.yellow).frame(width: 350, height: 70, alignment: .center)
                .background(Color.black)
                .cornerRadius(20.0).multilineTextAlignment(.center)
        }
    }
}






```





   

