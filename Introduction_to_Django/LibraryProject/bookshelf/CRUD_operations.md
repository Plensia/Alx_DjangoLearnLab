CRUD Operations for Bookshelf App
Create
Command:
from bookshelf.models import Book
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)

Output:
Book object (1984)

Retrieve
Command:
from bookshelf.models import Book
book = Book.objects.get(title="1984")
print(book.title, book.author, book.publication_year)

Output:
1984 George Orwell 1949

Update
Command:
from bookshelf.models import Book
book = Book.objects.get(title="1984")
book.title = "Nineteen Eighty-Four"
book.save()
print(book.title)

Output:
Nineteen Eighty-Four

Delete
Command:
from bookshelf.models import Book
book = Book.objects.get(title="Nineteen Eighty-Four")
book.delete()
print(Book.objects.all())

Output:
<QuerySet []>
