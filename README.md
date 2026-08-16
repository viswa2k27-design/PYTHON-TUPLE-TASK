# PYTHON-TUPLE-TASK[main.py](https://github.com/user-attachments/files/31120900/main.py)
# #LIST


given_numbers = [10, 501, 22, 37, 100, 999, 87, 351]


Even_Numbers: [10,22,100]
Odd_Numbers: [501, 37, 999, 87, 351]

given_list = [10, 501, 22, 37, 100, 999, 87, 351]

even_numbers = []
odd_numbers = []

for num in given_list:
    if num % 2 == 0:
        even_numbers.append(num)
    else:
        odd_numbers.append(num)

print("Even Numbers:", even_numbers)
print("Odd Numbers:", odd_numbers)

# #TO FIND THE PRIME NUMBER
LIST = [10, 501, 22, 37, 100, 999, 87, 351]

prime_numbers = []

for number in LIST:
    if number > 1:
        is_prime = True

        for i in range(2, number):
            if number % i == 0:
                is_prime = False
                break

        if is_prime:
            prime_numbers.append(number)

print("Prime Numbers:", prime_numbers)
print("Count of Prime Numbers:", len(prime_numbers))

# #TO FIND HAPPY NUMBERS

list = [10, 501, 22, 37, 100, 999, 87, 351]

happy_numbers = []

for number in list:
    n = number
    seen = set()

    while n != 1 and n not in seen:
        seen.add(n)

        total = 0

        while n > 0:
            digit = n % 10
            total = total + digit ** 2
            n = n // 10

        n = total

    if n == 1:
        happy_numbers.append(number)

print("Happy Numbers:", happy_numbers)
print("Count of Happy Numbers:", len(happy_numbers))

#
#
#
# #SUM OF THE FIRST AND LAST DIGIT OF AN INTEGER

numbers = int(input("Enter a number: "))

last_digit = numbers % 100000

while numbers >= 100000:
    number = numbers // 100000

first_digit = numbers

sum = first_digit + last_digit

print("First digit:", first_digit)
print("Last digit:", last_digit)
print("Sum is :", sum)

# #IN THIS WE HAVE TO FIND ALL COMBINATION ₹1, ₹2, ₹5, AND ₹10 THAT ADDS UP TO ₹10.

for one in range(11):
    for two in range(6):
        for five in range(3):
            for ten in range(2):

                total = (one * 1) + (two * 2) + (five * 5) + (ten * 10)

                if total == 10:
                    print(
                        "₹1:", one,
                        "₹2:", two,
                        "₹5:", five,
                        "₹10:", ten
                    )

#

# #TO FIND THE DUPILCATES IN THE LISTS
#
list_alpha = [100, 2000, 300, 457, 50457]
list_beta = [2000, 30, 457, 50457, 80]
list_gamma = [50457, 457, 911, 100, 2000]





list_alpha = [100, 2000, 300, 457, 50457]
list_beta = [2000, 30, 457, 50457, 80]
list_gamma = [50457, 457, 911, 100, 2000]

duplicates = set(list_alpha) & set(list_beta) & set(list_gamma)

print("Duplicates found in three lists:", duplicates)



# #FIRST NON REPEATING ELEMENTS IN GIVEN LIST

LIST = [300,650,457,300,650,1250,1250]

for number in LIST:
    if LIST.count(number) == 1:
        print("FIRST NON REPEATING ELEMENT:", number)
        break


#CODE TO FIND MINIMUM ELEMENT

numbers = [1, 2, 3, 4, 5, 6, 7]

minimum = numbers[0]

for number in numbers:
    if number < minimum:
        minimum = number

print("MINIMUM ELEMENT IS:", minimum)

# #FOR THE GIVEN VALUE 59
#
numbers = [10, 20, 30, 9]
target = 59

for i in range(len(numbers)):
    for j in range(i + 1, len(numbers)):
        for k in range(j + 1, len(numbers)):

            if numbers[i] + numbers[j] + numbers[k] == target:
                print("Triplet:", numbers[i], numbers[j], numbers[k])



# #SUM EQUALS TO ZERO

numbers = [4, 2, -3, 1, 6]

found = False

for i in range(len(numbers)):
    total = 0

    for j in range(i, len(numbers)):
        total = total + numbers[j]

        if total == 0:
            print("Sub-list with sum zero found")
            print(numbers[i:j + 1])
            found = True
            break

    if found:
        break
