# iteration


import Foundation

var greeting = "Hello, playground"

//: [Next](@next)

struct IndieApp {
    let name: String
    let monthlyPrice: Double
    let users: Int
}

let appPortfolio = [IndieApp(name: "Name 1", monthlyPrice: 11.3, users: 123),
                          IndieApp(name: "Name 2", monthlyPrice: 34.3, users: 590),
                          IndieApp(name: "Name 3", monthlyPrice: 12.3, users: 345),
                          IndieApp(name: "Name 4", monthlyPrice: 45.6, users: 765)]

//filter
let filter = appPortfolio.filter {$0.monthlyPrice > 11.3 }
//print(filter)
