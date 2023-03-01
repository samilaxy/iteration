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

//map
let increasePrices = appPortfolio.map {$0.monthlyPrice + 2.5 }
//print(increasePrices)

//reduce
let totalUsers = appPortfolio.reduce(0, {$0 + $1.users })
//print(totalUsers)

//chaining
let recurringRevenue = appPortfolio.map {$0.monthlyPrice * Double($0.users)}.reduce(0, +)
//print(recurringRevenue)

//compactmap
let nilNumbers : [Int?] = [1,nil,34,nil,4,5,6,nil]
let nonNIlNumbers = nilNumbers.compactMap({$0})
print(nonNIlNumbers)

//flatmap
let arrayOfArrays: [[Int]] = [[1,2,3], [3,2,4],[7,6,4]]
let singleArray = arrayOfArrays.flatMap {$0.map{$0 * 2}}
print(singleArray)
