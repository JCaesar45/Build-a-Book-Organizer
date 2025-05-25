````markdown
# 📚 Book Organizer

A simple JavaScript-based project that filters and sorts a list of books based on their release year.

## 🧠 Objective

This project demonstrates how to:

- Store structured data using an array of objects
- Filter an array based on a condition
- Sort an array using a custom comparator function

## 🚀 Features

- Maintains a list of books with their title, author, and release year
- Filters out books released **after 1950**
- Sorts the filtered books in **ascending order** by release year

## 🧩 User Stories Fulfilled

- ✅ An array named `books` with objects that have `title`, `authorName`, and `releaseYear`
- ✅ At least **three** book entries
- ✅ A callback function `sortByYear` that:
  - Returns `-1` if first book was released earlier
  - Returns `1` if first book was released later
  - Returns `0` if years are equal
- ✅ A `filteredBooks` array containing only books **released on or before 1950**
- ✅ The `filteredBooks` array is sorted using `sortByYear`

## 🧾 Sample Code

```javascript
// Array of book objects
const books = [
  { title: "To Kill a Mockingbird", authorName: "Harper Lee", releaseYear: 1960 },
  { title: "1984", authorName: "George Orwell", releaseYear: 1949 },
  { title: "The Great Gatsby", authorName: "F. Scott Fitzgerald", releaseYear: 1925 },
];

// Sort callback function
function sortByYear(book1, book2) {
  if (book1.releaseYear < book2.releaseYear) return -1;
  if (book1.releaseYear > book2.releaseYear) return 1;
  return 0;
}

// Filter and sort books
const filteredBooks = books.filter(book => book.releaseYear <= 1950);
filteredBooks.sort(sortByYear);

console.log("Filtered and Sorted Books:", filteredBooks);
```

## 📂 Output

```bash
Filtered and Sorted Books: [
  { title: 'The Great Gatsby', authorName: 'F. Scott Fitzgerald', releaseYear: 1925 },
  { title: '1984', authorName: 'George Orwell', releaseYear: 1949 }
]
```

## 🛠️ How to Run

1. Copy the code into a `.js` file (e.g. `bookOrganizer.js`)
2. Run it using Node.js:

```bash
node bookOrganizer.js
```

## 📝 License

This project is open-source and free to use for educational purposes.

```
