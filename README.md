# Cash Settlement Project

Welcome to the a cash settlement project! This project aims to minimise the cashflow and simplify the process of managing expenses among groups of people, making it easier to track and settle debts without the need for complex calculations or constant back-and-forth exchanges.

## Technologies Used

- **HTML/CSS/JavaScript**: Frontend development technologies.
- **Netork visualization**: Drawing surface for graphic design.

## Intuition

Here's the intuition of how this project can be used in an application:

• Expense Tracking: It will allow users to log expenses they incur, specifying who participated in the expense and how much each person owes or is owed. For example, if a group of friends goes out for dinner, one person can pay the bill and then log the details of the expense in this application.

• Shared Expenses: When an expense is logged, users can specify who should share the cost. This could be one or multiple people involved in the transaction. It automatically calculates how much each person owes or is owed based on predefined sharing rules.

• Simplified Debt Management: It will keep a running tally of who owes money to whom within a group. It aggregates individual transactions to show a clear picture of overall balances, simplifying the process of settling debts among friends or colleagues.

• Balance Settlements: Instead of settling debts for every single expense, it will allow users to settle balances periodically. For instance, if one person owes money to another due to multiple shared expenses, they can settle the entire balance with one transaction rather than paying back each individual expense separately.

## Algorithm

• Naive approach: Let's store the users who payed the bills on behlaf of others in one container, let's say a vector and the rest users who are in debt in anothor vector, both in non-decreasing order. Now, we can run a loop and in each iteration we will extract the user with the highest credit from the first vector and the user with the highest debt from the second vector. We can then take the minimum out of them and try to settle the debt between them. If there is remaining we add them back to their respective vectors and sort them to maintain the order. Thus, after all the iterations are done, all the debts will be settled within the group

Time Complexity: Let's say, there are n users in total. In each iteration, one user will be settled for sure. Hence, at max there will be n number of iterations. In each iteration we are sorting the vectors to maintain the order which in itself has a time complexity of O(n.log(n)). Hence, the total time complexity of this approach is (O(n^2.log(n))).

• Efficient approach: A better approach will be to use the priority queue or the binary heap data structure in javascript. A binary heap is a complete binary tree where each node has a key value, and the key at the root is the minimum (for a min-heap) or maximum (for a max-heap) among all keys present in the heap. The BinaryHeap() class used in this project is a custom built class for implementing a binary heap data structure. We can use this class to define both min heap and max heap and settle out all the users using one loop only.

Time Complexity: Only one loop is used and in each iteration, the highest values of the min heap and max heap are accessed and updated which has a time complexity of O(log(n)). Hence, the total time complexity of this approach is (O(n.log(n))), which is substantial improvement.



## Contributing

Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature-name`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature/your-feature-name`).
6. Create a new Pull Request.


## Support

If you encounter any issues or have any questions, please feel free to [create an issue](https://github.com/Dodo-sr13/reactjs-cash-settlement/issues). We're here to help!

---

Thank you for visiting. Happy gossip!