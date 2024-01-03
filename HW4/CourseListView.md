<h1>WelcomeView<h1>

```SwiftUI
import SwiftUI
struct Course:Identifiable{
    var id = UUID()
    var name:String
    var image:String
    var description:String
}
var courses = [
    Course(name: "微型程式設計", image: "ipad", description: "人工智慧介紹"),
    Course(name: "編譯程式概論", image: "compiler", description: "Python介紹"),
    Course(name: "生物學概論", image: "bio", description: "資料科學介紹"),
    Course(name: "影片中學英文", image: "english", description: "微軟Azure介紹"),
    Course(name: "電腦與安全概論", image: "cybersecurity", description: "亞馬遜AWS介紹")
]




struct BasicImageRow: View{
    var thisCourse:Course
    var body: some View{
        HStack{
            Image(thisCourse.image)
                .resizable()
                .frame(width: 40, height: 40)
                .cornerRadius(5)
            Text(thisCourse.name)
        }
    }
}




struct CourseDetailView:View{
    @Environment(\.presentationMode)
    var presentationMode
    var thisCourse:Course
    var body: some View{
        ScrollView{
            VStack{
                Image(thisCourse.image)
                    .resizable()
                    .aspectRatio(contentMode: .fill)
                    .clipped()
                Text(thisCourse.name)
                    .font(.system(.title, design:.rounded))
                    .fontWeight(.black)
                Spacer()
                Text(thisCourse.description)
                    .font(.system(.subheadline, design:.rounded))
                    .fontWeight(.light)
                Spacer()
            }
        }
        .overlay(
            HStack{
                Spacer()
                VStack{
                    Button(action:{
                        self.presentationMode.wrappedValue.dismiss()
                    },label:{
                        Image(systemName:"chevron.down.circle.fill")
                            .font(.largeTitle)
                            .foregroundColor(.white)
                    })
                    .padding(.trailing, 20)
                    .padding(.top, 40)
                    Spacer()
                }
            }
        )
    }
}




struct CourseListView:View{
    @State var showDetailView = false
    @State var selectedCourse:Course?
var body: some View{
    NavigationView{
        List(courses){ courseItem in
            BasicImageRow(thisCourse: courseItem)
                .onTapGesture{
                    self.showDetailView = true
                    self.selectedCourse = courseItem
                }
        }
        .sheet(item: self.$selectedCourse){ thisCourse in CourseDetailView(thisCourse: thisCourse)
        }
        .navigationBarTitle("課表")
    }
}
}





```





   

