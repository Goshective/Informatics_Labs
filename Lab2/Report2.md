## Лабораторная работа 2

Реализуемем скрипт, используя несколько блоков функция

1. Функция `main` отвечает за считывание и преобразование входной строки в массив, вызов вспомогательных функций и вывод результата.

![image](https://github.com/user-attachments/assets/457b9d31-6689-4f09-a1c6-bbbca0b40f8a)

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

![image](https://github.com/user-attachments/assets/0ca169c5-4493-49a9-999c-765e0ef4d43f)

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

### Вывод
Был изучен синтаксис bash для написания простых программ: условия, циклы, массивы, функции. Также были изучены основные особенности работы программ и запуска скриптов.
