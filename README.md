### 1. Запрос для вставки данных минимум о двух книгах в коллекцию `books`

db.books.insertMany([
  {
    title: "The Great Gatsby",
    description: "A classic novel set in the Jazz Age",
    authors: "F. Scott Fitzgerald"
  },
  {
    title: "To Kill a Mockingbird",
    description: "A novel about racial injustice in the Deep South",
    authors: "Harper Lee"
  }
])

### 2. Запрос для поиска полей документов коллекции books по полю title

db.books.find({ title: "The Great Gatsby" })

### 3. Запрос для редактирования полей description и authors коллекции books по _id записи

db.books.updateOne(
  { _id: "60d5f4838e7d6c0a7c8e4769" },  
  {
    $set: {
      description: "An updated description of the book",
      authors: "Updated Author Name"
    }
  }
)

