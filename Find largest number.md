print('\tFinding Largest Number')

def largest_num(a, b, c):

    if a > b and a > c:
        return f"\nLetter A is the largest with a value of {a}"

    elif b > a and b > a:
        return f"\nLetter B is the largest with a value of {b}"

    else:
        return f"\nLetter C is the largest with a value of {c}"


a = int(input("\nFirst Number: "))
b = int(input("Second Number: "))
c = int(input("Third Number: "))

result = largest_num(a, b, c)
print(result)
