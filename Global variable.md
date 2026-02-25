#GLOBAL VARIABLE

x = 300

def closest_num():
    

    print(f'\tFind the closest number to {x}')

    a1 = int(input('\nFirst Number: '))
    b2 = int(input(' Second Number: '))
    c3 = int(input(' Third Number: '))

    print('----------------------------')
    print(f'Value of First Number: {a1}')
    print(f'Value of Second Number: {b2}')
    print(f'Value of Third Number: {c3}')
    print('----------------------------')

    diff_a1 = abs(x - a1)
    diff_b2 = abs(x - b2)
    diff_c3 = abs(x - c3)

    smallest = min(diff_a1, diff_b2, diff_c3)

    if diff_a1 == diff_b2 == diff_c3:
        print('\nAll number is close to')

    elif smallest == diff_a1:
        print(f'\nFirst number ({a1}) is the "Closest" of them all')

    elif smallest == diff_b2:
        print(f'\nSecond number ({b2}) is the "Closest" of them all')

    else:
        print(f'\nThird number ({c3}) is the "Closest" of them all')

closest_num()
