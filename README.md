# Global-Problem
//
//  ContentView.swift
//  Start Gardening
//
//  Created by Venkata Akella on 2/24/23.
//

import SwiftUI
struct SearchView: View {
var body: some View {
    List{
       
       VStack{
           Text("Why Should You Plant Gardens:")
        Text("People should start to plant gardens because:")
        Text("It improved exercise, by moving around more, as well as increases your health in terms of vitamins from the sun suh as vitamin D.")
        Text("Improved your diet, especially by eating natural and organic foods without any processed materials in them.")
        Text("By spending more time in the fresh air and in nature than sittim at home your can reduce stress levels from gardening")
        
        
           
       }
      
       VStack{
           Text("How to plant your own garden")
        Text("1.Get nutrient soil or fertalizer")
        Text("2.Get seeds or baby plants to plant in your soil or fertilizer")
        Text("3.Water and nuture everyday for best results")
        


           
       }
      
       VStack{
           Text("Helping the community")
        Text("By telling neighbors and your community about how to garden and the benefits of it, your can help eautif the Landscape, Making Fresh Produce Accessible, Promoting Healthier Lifestyle, Cleaning up the Environment and Building Stronger Communities.")

        
           
 
       }
       
     
       
        

}

}//End of SearchView
}

struct ContentView: View {
    @State var isLinkActive = false
    var body: some View {
        VStack {
        Text("Start Garderning")
        .font(Font.title)
        .foregroundColor(Color.blue)
        Image("Seedling")
        .resizable()
        .frame(width: 300, height: 200)
            NavigationView {
                VStack(alignment: .leading) {
                    NavigationLink(destination:SearchView(), isActive:$isLinkActive) {
                        Button(action:handleButton){
                          Text("Press to Continue")
                        }
                    } // End of navigation link
                    } // End of VStack
                    
                    } // End of Navigation view
                
            }
            
            } // End of body
    
    func handleButton(){
        self.isLinkActive = true
    }
        } // End of content view
    
            
        
  
    





struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}


