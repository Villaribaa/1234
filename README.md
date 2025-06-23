# 1234
max_caunt = 3
password = 1234
print (f"У вас є {max_caunt} Cпроби")
for attempt_num  in range(max_caunt):
    try:
        a = int(input(f"Спроба {attempt_num+1}/{max_caunt}:Введіть пароль "))
    except ValueError:
        print("Будь ласка, введіть число.")
        print (f"Залишилось {max_caunt - (attempt_num +1)} спроб(и)")
        continue
    if a == password:
        print ("Ви ввели вірний пароль")
        break
    else:
        if attempt_num < max_caunt-1:
            print ("пароль введено невірно")
            print (f"Залишилось {max_caunt - (attempt_num +1)} спроб(и)")
else:
        print ("Це остання спроба і вона введена неверіно")
