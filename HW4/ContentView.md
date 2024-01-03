<h1>ContentView<h1>

```SwiftUI
import SwiftUI
struct ContentView: View{
    var body: some View{
        VStack{
            Text("劉子揚")
                .font(.largeTitle)
                .fontWeight(.heavy)
                .foregroundStyle(.primary)
            TabView{
                Group{
                    WelcomeView()
                        .tabItem{
                            Image(systemName: "person")
                            Text("自我介紹")
                        }
                    CourseListView()
                        .tabItem{
                            Image(systemName: "list.dash")
                            Text("課表")
                        }
                    CardView()
                        .tabItem{
                            Image(systemName: "book")
                            Text("老師名字")
                        }
                    SafeView()
                        .tabItem{
                            Image(systemName: "heart")
                            Text("積陰德")
                        }
                }
                .toolbarBackground(Color.black, for: .tabBar)
                .toolbarBackground(.visible, for: .tabBar)
            }
        }
        .tint(.yellow)
    }
}






```





   

