# movie-ticket-system-
from movies import show_movies
from booking import book_ticket

def main():
    while True:
        print("\n--- Movie Ticket Booking System ---")
        print("1. Show Movies")
        print("2. Book Ticket")
        print("3. Exit")

        choice = input("Enter choice: ")

        if choice == "1":
            show_movies()

        elif choice == "2":
            try:
                movie_id = int(input("Enter movie ID: "))
                seats = int(input("Enter number of seats: "))
                result = book_ticket(movie_id, seats)
                print(result)
            except ValueError:
                print("Invalid input!")

        elif choice == "3":
            print("Goodbye!")
            break

        else:
            print("Invalid choice!")

if __name__ == "__main__":
    main()
