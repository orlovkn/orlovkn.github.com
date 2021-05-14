https://www.programiz.com/python-programming/class


# =======================



user = {'name': 'Alex', 'age': 32, 'can_run': True}

for key, value in user.items():
    if key in 'age':
        print(f'ваш возраст: {value} года')


# =======================

while True:
    response = input('say smth: ')
    if response == 'bye':
        break

# =======================

def example(*args, **kwargs):
    total = 0

    for items in kwargs.values():
        total +=items
    return sum(args) + total

print(example(1,2,3,4,5, num1 = 4, num2 = 5, num3 = 12))

# =======================

some_list = ['a', 'b', 'c', 'a', 'm', 'm']

duplicates = []
for value in some_list:
  if some_list.count(value) > 1:
      if value not in duplicates:
        duplicates.append(value)

print(duplicates)

# =======================

class PlayerCharacker:
    def __init__(self, name):
        self.name = name

    def run(self):
        print('run, ', self.name)


player1 = PlayerCharacker("Ron")
player1.run()
print(player1.name)

# =======================

class MyNewClass:
    '''This is a docstring. I have created a new class'''
    pass

# =======================

class Typo:

    def get_typo(self, text):
        return "{}, some text".format(text)

import typo

typo = typo.Typo()
text = typo.get_typo("вамвамва вамук укаука")

print(text)

# =======================

