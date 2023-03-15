## HW_2 Postman


http://162.55.220.72:5005/first
1. Отправить запрос.
2. Статус код 200
3. Проверить, что в body приходит правильный string.

http://162.55.220.72:5005/user_info_3
1. Отправить запрос.
2. Статус код 200
3. Спарсить response body в json.
4. Проверить, что name в ответе равно name s request (name вбить руками.)
5. Проверить, что age в ответе равно age s request (age вбить руками.)
6. Проверить, что salary в ответе равно salary s request (salary вбить руками.)
7. Спарсить request.
8. Проверить, что name в ответе равно name s request (name забрать из request.)
9. Проверить, что age в ответе равно age s request (age забрать из request.)
10. Проверить, что salary в ответе равно salary s request (salary забрать из request.)
11. Вывести в консоль параметр family из response.
12. Проверить что *u_salary_1_5_year* в ответе равно *salary*4* (salary забрать из request)


http://162.55.220.72:5005/object_info_3
1. Отправить запрос.
2. Статус код 200 
**pm.test("Status code is 200", function () {
    **pm.response.to.have.status(200);**
});**

3. Спарсить response body в json.
 **var respData = pm.response.json();**

4. Спарсить request *(!!GET -> значит url). !!!*
**var reqData = pm.request.url.query.toObject();**

5. Проверить, что name в ответе равно name s request (name забрать из request.)
**var respName = respData.name;**
**var reqName = reqData.name**

**pm.test("RESPnAME_eql_REQnAME", function () {
        pm.expect(respName).to.eql(reqName);
});**

6. Проверить, что age в ответе равно age s request (age забрать из request.)
**respAge = respData.age;
reqAge = reqData.age;

console.log(typeof respAge);
console.log(typeof reqAge);

pm.test("RESPaGE_eql_REQaGE", function () {
      pm.expect(respAge).to.eql(reqAge);
});**

7. Проверить, что salary в ответе равно salary s request (salary забрать из request.)
**var respSalary = respData.salary;
var reqSalary = +reqData.salary;

console.log(typeof respSalary)
console.log(typeof reqSalary)

pm.test("RESPsALARY_eql_REQsALARY", function(){
    pm.expect(respSalary).to.eql(reqSalary);
});**

8. Вывести в консоль параметр family из response.
**var respFamily = respData.family;
console.log(respFamily);**

9. Проверить, что у параметра dog есть параметры name.
var respDog = respFamily.pets.dog;
console.log(respDog);

pm.test("pm_Dog_have_name", function () {
    pm.expect(respDog).to.have.property("name");
});
10. Проверить, что у параметра dog есть параметры age.
pm.test("pm_Dog_have_age", function () {
    pm.expect(respDog).to.have.property("age");
});

11. Проверить, что параметр name имеет значение Luky.
var respDname = respDog.name;
var respDage = respDog.age;

pm.test("RESPdNAME_eql_Luky", function(){
    pm.expect(respDname).to.eql("Luky");
});
12. Проверить, что параметр age имеет значение 4.
pm.test("RESPdAGE_eql_4", function(){
    pm.expect(respDage).to.eql(4);
});

http://162.55.220.72:5005/object_info_4
1. Отправить запрос.
2. Статус код 200
3. Спарсить response body в json.
4. Спарсить request.
5. Проверить, что name в ответе равно name s request (name забрать из request.)
6. Проверить, что age в ответе равно age из request (age забрать из request.)
7. Вывести в консоль параметр salary из request.
8. Вывести в консоль параметр salary из response.
9. Вывести в консоль 0-й элемент параметра salary из response.
10. Вывести в консоль 1-й элемент параметра salary параметр salary из response.
11. Вывести в консоль 2-й элемент параметра salary параметр salary из response.
12. Проверить, что 0-й элемент параметра salary равен salary из request (salary забрать из request.)
13. Проверить, что 1-й элемент параметра salary равен salary*2 из request (salary забрать из request.)
14. Проверить, что 2-й элемент параметра salary равен salary*3 из request (salary забрать из request.)
15. Создать в окружении переменную name
16. Создать в окружении переменную age
17. Создать в окружении переменную salary
18. Передать в окружение переменную name
19. Передать в окружение переменную age
20. Передать в окружение переменную salary
21. Написать цикл который выведет в консоль по порядку элементы списка из параметра salary.


