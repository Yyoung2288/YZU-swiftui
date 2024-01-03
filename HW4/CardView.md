<h1>ContentView<h1>

```SwiftUI
import SwiftUI
struct TermAndDescription: Identifiable{
    var id = UUID()
    var term:String
    var description:String
}




var myDictionary = [
    TermAndDescription(term: "徐逸懷", description: "編譯程式老師"),
    TermAndDescription(term: "邱昱偉", description: "生物概論老師"),
    TermAndDescription(term: "歐崇明", description: "電腦安全概論老師"),
    TermAndDescription(term: "鐘祥仁", description: "微型程式設計老師")
]




struct CardView: View{
    @State var currentCard = 0
    var body: some View{
        VStack{
            VStack{
                Text(myDictionary[currentCard].term)
                    .font(.title)
                    .padding(.all, 10)
                    .foregroundColor(.white)
                Text(myDictionary[currentCard].description)
                    .font(.body).foregroundColor(.yellow)
                    .padding(.all, 10)
            }
            .frame(minWidth: 0, idealWidth: 100, maxWidth: 300, minHeight: 0, idealHeight: 100, maxHeight: 300, alignment: .center)
            .background(Color.black)
            .onTapGesture{
                if currentCard<myDictionary.count-1{
                    currentCard+=1
                }else{
                    currentCard=0
                }
            }
            Text("點擊查看下一個老師")
                .padding(.all, 10)
        }
    }
}






```





   


