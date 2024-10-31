## Лабораторная работа 2

Реализуем скрипт, используя несколько блоков функция

1. Функция `main` отвечает за считывание и преобразование входной строки в массив, вызов вспомогательных функций и вывод результата.

![image](https://github.com/user-attachments/assets/d7629cb4-5fae-406c-ac29-5505d2122b6a)


```
function main ()
{
    IFS="."
    read -r ip1 ip2 ip3 ip4 <<< $1
    arr=($ip1 $ip2 $ip3 $ip4)
    num=1
    for ((index=0;index<=3;index++))
    do
        bin=$(convertToBase ${arr[$index]} 2)
        ans[index]=$(addTo8 $bin)
    done
    
    for ip in ${ans[@]}
    do
        if [ $num -eq 4 ]; then
            echo $ip
        else
            echo -n $ip"."
        fi
        let "num += 1"
    done
}
```

2. Далее преобразуем числа из десятичной записи в двоичную.

![image](https://github.com/user-attachments/assets/a9b1e7c1-103d-43db-9b71-ee3fcdf7cb41)


```
function convertToBase () # (Val Base)
{
   val=$1
   base=$2
   result=""
   while [ $val -ne 0 ] ; do
        result=$(( $val % $base ))$result #residual is next digit
        val=$(( $val / $base ))
   done
   echo -n $result
}
```
3. Для вывода чисел в одном формате добавляем в их начало нули до 8.

![image](https://github.com/user-attachments/assets/8c0d590b-0651-403a-91eb-7df2415778b6)

```
function convertToBase () # (Val Base)
{
   val=$1
   base=$2
   result=""
   while [ $val -ne 0 ] ; do
        result=$(( $val % $base ))$result #residual is next digit
        val=$(( $val / $base ))
   done
   echo -n $result
}
```
4. Работа программы на разных данных.

![image](https://github.com/user-attachments/assets/719901f0-29ce-4d6c-8db2-f48d337647ab)

![image](https://github.com/user-attachments/assets/07aa6d3a-e5e0-42d4-a732-26ee8a616514)

### Вывод
Был изучен синтаксис bash для написания простых программ: условия, циклы, массивы, функции. Также были изучены основные особенности работы программ и запуска скриптов.
