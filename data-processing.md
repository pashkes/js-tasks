
## Написать функции:
**Соблюдать понятные и подходящие имена для функций и переменных**

Следить за форматированием и чистотой кода

1. Получить массив клиентов у которых ```phoneNumber``` пустой
2. Получить массив имен клиентов `['Hayyim', 'Jsandye', 'Hashim', ...]`
3. Получить массив свойств, на вход функция должна принимать имя свойства, на выходе список значений этого свойства, значение в списке должны быть уникальными
4. Получить массив клиентов у которых phoneNumber уникальный
5. Проверить на наличие в списке заблокированных клиентов ```isBlocked``` Если хотя есть хотя бы один заблокированный, вернуть true, иначе false
6. Получить массив `firstName` которые заблокированные
7. Подсчитать сколько человек с каким полом, вернуть обʼект вида  `{ male: 1, female: 1, nonBinary: 1}`, на вход функция должна принимать страну и подсчитывать количество только для конкретной страны
8. Посчитать сумму `deposit` и сгрупировать по странам 
`{ [countryName]: number }`
9. Вывести массив с двух стран, с минимальным количеством `deposit` и максимальным
10. Отсортировать клиентов от наименьшего  `deposit` до максимального. И наоборот
11. Написать функция которая принимает два числа, тоесть диапазон чисел, например от 10 до 100, на выходе должен быть список с отфильтрованными `deposit` согласно диапазону, отсортировать от наименьшей суммы

```
    const clients = [{
      "id": 1,
      "firstName": "Eva",
      "lastName": "Baglow",
      "email": "ebaglow0@nydailynews.com",
      "gender": "Female",
      "deposit": "$428.42",
      "isBlocked": false,
      "country": "Poland",
      "phoneNumber": null
    }, {
      "id": 2,
      "firstName": "Lexis",
      "lastName": "McAster",
      "email": "lmcaster1@bloglines.com",
      "gender": "Female",
      "deposit": "$587.14",
      "isBlocked": false,
      "country": "Ukraine",
      "phoneNumber": "939-776-1971"
    }, {
      "id": 3,
      "firstName": "Inger",
      "lastName": "Oxtaby",
      "email": "ioxtaby2@fda.gov",
      "gender": "Non-binary",
      "deposit": "$519.77",
      "isBlocked": false,
      "country": "Poland",
      "phoneNumber": "907-434-8606"
    }, {
      "id": 4,
      "firstName": "Tamar",
      "lastName": "Mabbitt",
      "email": "tmabbitt3@studiopress.com",
      "gender": "Female",
      "deposit": "$224.46",
      "isBlocked": true,
      "country": "Poland",
      "phoneNumber": "907-434-8606"
    }, {
      "id": 5,
      "firstName": "Cathee",
      "lastName": "Lorking",
      "email": "clorking4@delicious.com",
      "gender": "Female",
      "deposit": "$110.13",
      "isBlocked": false,
      "country": "Ukraine",
      "phoneNumber": "824-575-2391"
    }, {
      "id": 6,
      "firstName": "Jo-anne",
      "lastName": "Loyndon",
      "email": "jloyndon5@hibu.com",
      "gender": "Female",
      "deposit": "$817.72",
      "isBlocked": true,
      "country": "Poland",
      "phoneNumber": "357-569-1131"
    }, {
      "id": 7,
      "firstName": "Amelia",
      "lastName": "Upstone",
      "email": "aupstone6@squidoo.com",
      "gender": "Bigender",
      "deposit": "$223.74",
      "isBlocked": false,
      "country": "Ukraine",
      "phoneNumber": "874-340-3986"
    }, {
      "id": 8,
      "firstName": "Codie",
      "lastName": "Fairs",
      "email": "cfairs7@si.edu",
      "gender": "Female",
      "deposit": "$684.27",
      "isBlocked": false,
      "country": "Sweden",
      "phoneNumber": "861-205-3712"
    }, {
      "id": 9,
      "firstName": "Winston",
      "lastName": "Hubery",
      "email": "whubery8@merriam-webster.com",
      "gender": "Male",
      "deposit": "$787.43",
      "isBlocked": false,
      "country": "Sweden",
      "phoneNumber": "468-208-9169"
    }, {
      "id": 10,
      "firstName": "Nisse",
      "lastName": "Leonardi",
      "email": "nleonardi9@intel.com",
      "gender": "Female",
      "deposit": "$546.84",
      "isBlocked": false,
      "country": "Poland",
      "phoneNumber": "564-155-7531"
    }, {
      "id": 11,
      "firstName": "Erhart",
      "lastName": "Dasent",
      "email": "edasenta@prweb.com",
      "gender": "Male",
      "deposit": "$534.78",
      "isBlocked": true,
      "country": "Sweden",
      "phoneNumber": "707-658-8037"
    }, {
      "id": 12,
      "firstName": "Sybille",
      "lastName": "Domoney",
      "email": "sdomoneyb@washington.edu",
      "gender": "Female",
      "deposit": "$691.88",
      "isBlocked": false,
      "country": "Ukraine",
      "phoneNumber": "820-575-2866"
    }, {
      "id": 13,
      "firstName": "Valentino",
      "lastName": "Boothby",
      "email": "vboothbyc@amazon.co.jp",
      "gender": "Male",
      "deposit": "$476.72",
      "isBlocked": true,
      "country": "Poland",
      "phoneNumber": "423-267-0805"
    }, {
      "id": 14,
      "firstName": "Corabel",
      "lastName": "Bastard",
      "email": "cbastardd@chron.com",
      "gender": "Female",
      "deposit": "$995.94",
      "isBlocked": true,
      "country": "Ukraine",
      "phoneNumber": "649-590-0339"
    }, {
      "id": 15,
      "firstName": "Elliot",
      "lastName": "Davidovitz",
      "email": "edavidovitze@wordpress.org",
      "gender": "Male",
      "deposit": "$848.51",
      "isBlocked": true,
      "country": "Sweden",
      "phoneNumber": null
    }, {
      "id": 16,
      "firstName": "Lexine",
      "lastName": "Lidgard",
      "email": "llidgardf@about.com",
      "gender": "Non-binary",
      "deposit": "$839.06",
      "isBlocked": false,
      "country": "Ukraine",
      "phoneNumber": "649-590-0339"
    }];
```
