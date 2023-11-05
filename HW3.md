<h1>HW2<h1>

```SwiftUI
import SwiftUI

struct ContentView: View {
    @State var number = 0
    @State var en = 0
    @State var WOL = ""
    var body: some View {
        ZStack{
            Image("img_background")
            
            VStack{
                Text(WOL)
                    .foregroundColor(.white)
                    .font(.system(size:50))
                if(number == 1)
                {
                    Image("img_paper")
                        .resizable()
                        .aspectRatio(contentMode:.fit)
                        .frame(width:400, height:200,alignment:.center)
                        .rotationEffect(.degrees(180))
                }
                
                else if(number == 2)
                {
                    Image("img_scissors")
                        .resizable()
                        .aspectRatio(contentMode:.fit)
                        .frame(width:400, height:200,alignment:.center)
                        .rotationEffect(.degrees(180))
                }
                else if(number == 3)
                {
                    Image("img_stone")
                        .resizable()
                        .aspectRatio(contentMode:.fit)
                        .frame(width:400, height:200,alignment:.center)
                        .rotationEffect(.degrees(180))
                }
                
                if(en == 1)
                {
                    Image("img_paper")
                        .resizable()
                        .aspectRatio(contentMode:.fit)
                        .frame(width:400, height:200,alignment:.center)
                }              
                else if(en == 2)
                {
                    Image("img_scissors")
                        .resizable()
                        .aspectRatio(contentMode:.fit)
                        .frame(width:400, height:200,alignment:.center)
                }         
                else if(en == 3)
                {
                    Image("img_stone")
                        .resizable()
                        .aspectRatio(contentMode:.fit)
                        .frame(width:400, height:200,alignment:.center)
                }   
                HStack{
                    Button(action: {number = Int.random(in: 1...3);en = 1
                        if(en == number){
                            WOL = "平手"
                        }
                        
                        if(number == 2){
                            WOL = "你輸了"
                        }
                        else if(number == 3){
                            WOL = "你贏了"
                        }
                        
                        
                      }, label: {
                        Text("布👋")
                            .padding(.all,10)
                            .frame(width:100, height:50,alignment: .center)
                            .background(Color.white)
                            .cornerRadius(30)
                            .foregroundColor(.black)                    
                    })                    
                    
                    Button(action: {number = Int.random(in: 1...3);
                        en = 2
                        if(en == number){
                            WOL = "平手"
                        }
                        
                        
                        if(number == 3){
                            WOL = "你輸了"
                        }
                        else if(number == 1){
                            WOL = "你贏了"
                        }
                        
                               
                    }, label: {
                        Text("剪刀✂️")
                            .padding(.all,10)
                            .frame(width:100, height:50,alignment: .center)
                            .background(Color.white)
                            .cornerRadius(30)
                            .foregroundColor(.black)                    
                    })
                    
                    Button(action: {number = Int.random(in: 1...3);
                        en = 3
                        if(en == number){
                            WOL = "平手"
                        }
                        
                        
                        if(number == 1){
                            WOL = "你輸了"
                        }
                        else if(number == 2){
                            WOL = "你贏了"
                        }
                    }, label: {
                        Text("石頭🪨")
                            .padding(.all,10)
                            .frame(width:100, height:50,alignment: .center)
                            .background(Color.white)
                            .cornerRadius(30)
                            .foregroundColor(.black)                    
                    })                    
                    
                    
                }//Hstack
            }//vstack
        }//zstack
    }//body
}


```

<img src="https://raw.githubusercontent.com/Yyoung2288/YZU-swiftui/main/IMG_0267.png">



   
