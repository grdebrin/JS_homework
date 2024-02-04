# JS_homework
Homework JavaScript

1. Создать переменную “item_1”

       let item_1;
2. Присвоить переменной item_1 цифру 5.

       item_1 = 5;
3. Вывести в консоль item_1.

       console.log(item_1);
4. Создать переменную “item_2”

       let item_2;
5. Присвоить переменной item_2 цифру 3.

       item_2 = 3;
6. Вывести в консоль item_2.

       console.log(item_2);
7. Создать переменную “item_3”

       let item_3;
8. Присвоить переменной item_3 сложение item_1 и item_2.

       item_3 = item_1 + item_2;
9. Вывести в консоль item_3.

       console.log(item_3);
10. Создать переменную “item_4”

        let item_4;
11. Присвоить переменной item_4 строку “Yolochka”

        item_4 = "Yolochka";
12. Вывести в консоль item_4.

        console.log(item_4);
13. Вывести в консоль сложение item_3 и item_4.

        console.log(item_3 + item_4);
14. Вывести в консоль умножение item_3 и item_4.

        console.log(item_3 * item_4);
15. Создать переменную “item_5”

        let item_5;
16. Присвоить переменной item_5 переменную item_3

        item_5 = item_3;
17. Создать переменную item_6.

        let item_6;
18. Создать переменную item_6_type

        let item_6_type;
19. Присвоить переменной item_6 значение 15

        item_6 = 15;
20. Присвоить переменной item_6_type тип переменной item_6

        item_6_type = typeof item_6;
21. Вывести в консоль тип данных item_6

        console.log(`item_6 == ${item_6}, item_6_type == ${item_6_type}`);
22. Создать переменную item_7 и в ней преобразовать item_6 в String.

        let item_7 = String(item_6);
23. Создать переменную item_7_type

        let item_7_type;
24. Присвоить переменной item_7_type тип переменной item_7

        item_7_type = typeof item_7;
25. Вывести в консоль тип данных item_7

        console.log(`item_7 == ${item_7}, item_7_type == ${item_7_type}`);
26-33. Создать функцию checkAge
     
    const checkAge = function(age) {
    if (typeof age !== "number") {
    console.error("Error: Age should be a number.");
    return;
    }

    if (age < 18) {
    console.log(`You don't have access cause your age is ${age}. It's less than 18.`);
    } else if (age >= 18 && age < 60) {
    console.log("Welcome!");
    } else if (age >= 60) {
    console.log("Keep calm and look Culture channel");
    } else {
    console.log("Technical work");
    }
    };
34. Вывести в консоль результат работы функции с возрастами 17, 18, 61

        checkAge(17);
        checkAge(18);
        checkAge(61);
35. Преобразовать задание 34 с проверкой типа данных

        const checkAgeWithTypeCheck = function(age) {
        if (typeof age !== "number") {
        console.error("Error: Age should be a number.");
        return;
        }

        if (age < 18) {
        console.log(`You don't have access cause your age is ${age}. It's less than 18.`);
        } else if (age >= 18 && age < 60) {
        console.log("Welcome!");
        } else if (age >= 60) {
        console.log("Keep calm and look Culture channel");
        } else {
        console.log("Technical work");
        }
        };
36. Преобразовать задание 35 для строки '2'

        const checkAgeWithConversion = function(age) {
        if (typeof age !== "number") {
        if (!isNaN(Number(age))) {
        age = Number(age);
        } else {
        console.error("Error: Age should be a number.");
        return;
        }
        }

        if (age < 18) {
        console.log(`You don't have access cause your age is ${age}. It's less than 18.`);
        } else if (age >= 18 && age < 60) {
        console.log("Welcome!");
        } else if (age >= 60) {
        console.log("Keep calm and look Culture channel");
        } else {
        console.log("Technical work");
        }
        };
37. Преобразовать задание 36 для ввода через prompt

        const checkAgeWithPrompt = function() {
        const inputAge = prompt("Please enter your age:");
        const age = Number(inputAge);

        if (isNaN(age) || inputAge === "") {
        console.error("Error: Age should be a non-empty number.");
        return;
        }

        if (age < 18) {
        console.log(`You don't have access cause your age is ${age}. It's less than 18.`);
        } else if (age >= 18 && age < 60) {
        console.log("Welcome!");
        } else if (age >= 60) {
        console.log("Keep calm and look Culture channel");
        } else {
        console.log("Technical work");
        }
        };
38. Валидационный скрипт

        const validateString = function(str) {
        if (typeof str !== "string") {
        console.error("Error: Input should be a string.");
        return;
        }

        if (str.length < 5) {
        console.error("Error: Minimum 5 characters required.");
        return;
        }

        if (str.length > 64) {
        console.error("Error: Maximum 64 characters allowed.");
        return;
        }

        if (!/[a-zA-Z]/.test(str)) {
        console.error("Error: At least one letter is required.");
        return;
        }

        if (!/[A-Z]/.test(str)) {
        console.error("Error: At least one uppercase letter is required.");
        return;
        }

        if (!/\d/.test(str)) {
        console.error("Error: At least one digit is required.");
        return;
        }

        if (!/@/.test(str)) {
        console.error("Error: At least one @ symbol is required.");
        return;
        }

        console.log("String is valid.");
        };

        // Пример использования
        validateString("Abcdef1@"); // Валидная строка
   
