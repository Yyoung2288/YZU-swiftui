<h1>Bonus<h1>

```SwiftUI
import SwiftUI

struct ContentView: View{
    let displayFontType = [".default", ".rounded", ".monospaced", ".serif"]
    @State var displayFontSelected = 0
    @State var IsDeepScheme = false
    @State var colorArray:Array = [255.0,255.0,255.0]
    @State var stepperValue = 0
    @State var sliderValue = 0.0
    @State var selectedDate = Date()
    var body: some View{
        NavigationView{
            Form(content:{
                Section(header: Text("字型設定"), content: {
                    Picker(selection:$displayFontSelected, label:Text("字型選擇(\(displayFontSelected))"),content:{
                        ForEach(0..<displayFontType.count,id: \.self, content:{
                            Text(self.displayFontType[$0])
                        })//foreach
                    })//label
                })//section
                Section(header:Text("背景風格"),
                        content: {
                    Toggle(isOn:$IsDeepScheme,
                           label:{Text("深色(\(String(IsDeepScheme)))")  
                    })//toggle
                })//section
                Section(header:Text("計數器")){
                    Stepper("Stepper(\(stepperValue))",
                            onIncrement:{stepperValue+=1},
                            onDecrement:{stepperValue-=1})
                }//section 可不寫content
                Section(header:Text("滑桿(\(sliderValue,specifier:"%.2f"))")){
                    Slider(value:$sliderValue, in:0...1)
                }//section
                Section(header:Text("選擇日期")){
                    DatePicker("\(selectedDate.formatted(date: .abbreviated, time: .omitted))", selection:$selectedDate, displayedComponents: .date)
                }
                
                
            })//form
            .navigationBarTitle("Setting 設定")
        }//navigation
    }//body View
}//struct



```
<a href = https://drive.google.com/drive/folders/1-0J1p8UEkRxa4UraJhLrIQjqkzOUexaV?usp=drive_link>功能示範影片</a>
<img src="https://raw.githubusercontent.com/Yyoung2288/YZU-swiftui/main/IMG_0268.jpeg">



   
