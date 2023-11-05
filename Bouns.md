<h1>Bonus<h1>

```SwiftUI
import SwiftUI

struct ContentView: View {
    var body: some View {
        ZStack{
            
            Image("background")  
            let f:Font = Font.custom("Nagurigaki-Crayon", size:50)            
            
                Text("我的箱子")
                .font(f)
                .padding(.all,10)
                .foregroundColor(.white)
                .background(Color.black)
                .opacity(0.7)
                .cornerRadius(15)  
                .offset(x:0, y:-300)
            VStack {
                Spacer(minLength: 70)
                HStack{
                    TopView(imageName:"yoda")
                    TopView(imageName:"sheep")
                    TopView(imageName:"cat")
                }
                HStack{
                    TopView(imageName:"ipad")
                    TopView(imageName:"projector")
                    TopView(imageName:"iphone")
                }
                HStack{
                    TopView(imageName: "controller")
                    TopView(imageName: "airpodspro")
                    TopView(imageName: "switch")
                }
                
            }    
      }
        
    }
}

struct TitleView: View{
    var body: some View{
        Text("我的櫃子")
            .font(.system(size:200))
    }
}

struct TopView :View{
    var imageName:String
    var body: some View{
        VStack{
            Image(imageName)
                .resizable()
                .aspectRatio( contentMode: .fit)
                .frame(height:100, alignment:.center)
            Text(imageName.capitalized)
                .fontWeight(/*@START_MENU_TOKEN@*/.bold/*@END_MENU_TOKEN@*/)
                .font(.system(size:25))
        }
        .frame(minWidth: 0, idealWidth: 5, maxWidth: 240, minHeight: 0, idealHeight: 5, maxHeight: .infinity, alignment: .center)    }
}




```

<img src="https://raw.githubusercontent.com/Yyoung2288/YZU-swiftui/main/IMG_0268.jpeg">



   
