# sem6

Задача1.

def get_sign(x):
    if x[0] in '+-':
        return x[0]

arr = ['в', '5', 'часов', '17', 'минут', 'температура', 'воздуха', 'была', '+5', 'градусов']

i = 0
while i < len(arr):
    sign = get_sign(arr[i])
    if arr[i].isdigit() or (sign and arr[i][1:].isdigit()):
        if sign:
            arr[i] = sign + arr[i][1:].zfill(2)
        else:
            arr[i] = arr[i].zfill(2)

        arr.insert(i, '"')
        arr.insert(i + 2, '"')
        i += 2

    i += 1

print(arr)
# ['в', '"', '05', '"', 'часов', '"', '17', '"', 'минут', 'температура', 'воздуха', 'была', '"', '+05', '"', 'градусов']



Задача2.

input_list = ['инженер-конструктор Игорь',
            'главный бухгалтер МАРИНА',
            'токарь высшего разряда нИКОЛАй',
            'директор аэлита']
answer = {}

for string in input_list:
    correct_name = string.split()[-1].capitalize()
    print(f"Привет, {correct_name}!")
    
    Задача3.
    
    input_list = [57.8, 46.51, 97, 90.88, 86.20, 87.30, 25.34, 33, 55.83, 77.37,
        56.55, 33.57, 99, 40, 59.31, 44.85, 53,]

store_id = id(input_list)
print(input_list)

print(f"{'a':-^100}")

end_word:str = ", " 

for i, num in enumerate(input_list):

    fix_price = str(f"{float(num):.2f}").split(".")

    if i == len(input_list) - 1:
        end_word = "\n"

    print(f"{fix_price[0]} руб {fix_price[1]} коп", end=end_word)


print(f"{'b':-^100}")

print(f"id before sort {store_id}")
input_list.sort()
print(input_list)
print(f"id after sort {id(input_list)}")

if store_id == id(input_list):
    print("In place")
else:
    print("Diff obj")


print(f"{'c':-^100}")

copy_of_list = input_list.copy()
copy_of_list.sort(reverse=True) 

print(copy_of_list)
print(store_id)
print(id(copy_of_list))

if store_id == id(copy_of_list):
    print("In place")
else:
    print("Diff obj")




print(f"{'d':-^100}")


print("five biger prices", input_list[-6:-1])
