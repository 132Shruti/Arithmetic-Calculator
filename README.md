from string import *
x = input('Enter number:')
for i in x:
    if i not in digits:
        raise ValueError('Invalid input!')
x = int(x)
output = ''
operator = ['+','-','*' ,'%','=']
while True:
    y = input('Enter operator:')
    if y not in operator:
        raise ValueError ('Invalid operator!')
    if y == '=':
        print(output)
        break
    z = (input(('Enter number:')))
    for i in z:
        if i not in digits:
            raise ValueError('Invalid input!')
    z = int(z)
    if len(output) >= 1:
        if y == '+':
            output = str(int(output)+ z)
        if y == '-':
            output = str(int(output)- z)
        if y == '*':
            output = str(int(output)* z)
        if y == '%':
            output = str(int(output)% z)
    else:
        if y == '+':
            output = output + str(x + z)
        if y == '-':
            output = output + str(x - z)
        if y == '*':
            output = output + str(x * z)
        if y == '%':
            output = output + str(x % z)
print('Calculator Task Completed')
