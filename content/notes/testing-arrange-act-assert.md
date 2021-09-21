---
title: "How to structure your unit tests"

tags: ["software testing", "best practice"]
categories: []
---

When writing test cases, we can organize our tests into three segments

- **Arrange** – set variables, stubs, mocks, spies, etc
- **Act** – the action that you wish to assert on
- **Assert** – make an assertion on the expected and actual results

Here's a simple example:

```jsx
test("renders correct number of books", () => {
    // arrange
    const books = [
        {title: "Animal Farm", author: "George Orwell"}, 
        {title: "Nineteen Eighty-Four", author: "George Orwell"}, 
        {title: "Down and Out in Paris and London", author: "George Orwell"}, 
    ]
    
    // act
    const { queryAllByTestId } = render(<BookList books={books} />);
    
    // assert
    expect(queryAllByTestId('book-item').length).toBe(3);
})
```
