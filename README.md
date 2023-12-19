# SwiftUI-Text
Briefly introduce how to use Text in SwiftUI.
# The first part
![IMG_1273](https://github.com/S-way520/SwiftUI-Text/assets/95877651/fa631e8d-89d2-4ddc-baa1-a6a5553452d0)
![IMG_1272](https://github.com/S-way520/SwiftUI-Text/assets/95877651/3610b595-3983-4a00-8485-30c2543e21d8)
# The second part
Code file 1
```swift
import SwiftUI

@main
struct MyApp: App {
    var body: some Scene {
        WindowGroup {
            TextTutorial()
        }
    }
}

```
Code file 2
```swift
import SwiftUI

/*
// （1）MARK: System default font (系统默认字体)
struct TextTutorial: View {
    var body: some View {
        VStack {
            Text("Hello, World!")
        }
    }
}
*/

/*
// （2）MARK: Font size (字体大小)
struct TextTutorial: View {
    var body: some View {
        VStack {
            Text("Hello, World!")
                //.font(.title)
                .font(.system(size: 36))
        }
    }
}
*/

/*
// （3）MARK: Bold font (字体加粗)
struct TextTutorial: View {
    var body: some View {
        VStack {
            Text("Hello, World!")
                .bold()
        }
    }
}
*/

/*
// （4）MARK: Italic (斜体)
struct TextTutorial: View {
    var body: some View {
        VStack {
            Text("Hello, World!")
                .italic()
        }
    }
}
*/

/*
// （5）MARK: Underline (下划线)
struct TextTutorial: View {
    var body: some View {
        VStack {
            Text("Hello, World!")
                //.underline()
                .underline(true, color: Color.blue)
        }
    }
}
*/

/*
// （6）MARK: Strikethrough (删除线)
struct TextTutorial: View {
    var body: some View {
        VStack {
            Text("Hello, World!")
                //.strikethrough()
                .strikethrough(true, color: Color.blue)
        }
    }
}
*/

/*
// （7）MARK: Multiline text alignment (多行文本对齐)
struct TextTutorial: View {
    var body: some View {
        VStack {
            Text("Multiline text alignment, Multiline text alignment, Multiline text alignment.")
                //.multilineTextAlignment(.leading)
                //.multilineTextAlignment(.trailing)
                .multilineTextAlignment(.center)
        }
    }
}
*/

/*
// （8）MARK: Baseline offset (行间距)
struct TextTutorial: View {
    var body: some View {
        VStack {
            Text("Baseline offset, Baseline offset, Baseline offset, Baseline offset.")
                .baselineOffset(50.0)
        }
    }
}
*/

/*
// （9）MARK: Character spacing (字符间距)
struct TextTutorial: View {
    var body: some View {
        VStack {
            Text("Character spacing, Character spacing, Character spacing. 字符间距, 字符间距, 字符间距。")
                .kerning(5.0)
        }
    }
}
*/

/*
 // （10）MARK: Font color (字体颜色)
struct TextTutorial: View {
    var body: some View {
        VStack {
            Text("Font color. 字体颜色。")
                .foregroundColor(Color.blue)
        }
    }
}
*/

/*
// （11）MARK: Border size (边框大小)
struct TextTutorial: View {
    var body: some View {
        VStack {
            Text("Border size.")
                .frame(width: 280, height: 150, alignment: .bottom)
                .border(Color.red)
        }
    }
}
*/


// （12）MARK: The entire line of text is curved (整行文字弯曲)
struct TextTutorial: View {
    var body: some View {
        HStack {
            ForEach(1..<11, id: \.self) { index in
                Text("B")
                    .font(.title.bold())
                    .rotation3DEffect(Angle(degrees: 45), axis: (x: 10.0, y: 0, z: 0))
                    .rotationEffect(Angle(degrees: (2 * cos(0.3 * Double(index) + 0)) * 30))
                    .offset(y: (4 * sin(0.3 * Double(index) + 0) * 30))
            }
        }
    }
}


```
