# Trading_Setup_Analysis-SILVER_BULLET
Проєкт аналізує торгову стратегію "SILVER BULLET" для основних американських індексів (SP500 та NAS100). Основна мета — побачити, які результати могла б принести торговля по цій стратегії на дистанції 3 роки (2021, 2022, 2023), а також знайти приховані закономірності для оптимізації торговлі в майбутньому

## Джерело даних
- Дані були зібрані вручну під час бектесту ринку індексів (SP500 та NAS100).
- Зберігаються у форматі CSV і доступні в папці `Data`.

## Структура даних
- `date`
- `session`: Торгова сесія (Лондонська сесія 3-4am UTC-4 NY, Нью-Йоркська 10-11am UTC-4 NY).
- `time`: Час входу в трейд.
- `pair`: Торговий актив.
- `rr`: Співвідношення ризик/прибуток.
- `result`: Результат угоди (TakeProfit/StopLoss/BreakEven).
- `direction`: Напрямок угоди (Long/Short).
- `profit`: Прибуток.
- `loss`: Збиток.
- `liquidity`: Ліквідність, яку зняла ціна безпосередньо перед входом (сформована до Торгової сесії чи під час неї).
- `screen`: Cкріншот угоди.
- `swp_bfr_ott`: Чи відбувся свіп ліквідності до початку Торгової сесії.

## Використані інструменти
- **Google Sheets**: Для зберігання, сортування та очищення даних про угоди.
- **Google Looker Studio**: Для створення дашборду, який відображає результати торговлі в різних торгових сесіях, ефективність стратегії на дистанції та загальну прибутковість.

## Візуалізації
На дашборді в Google Looker Studio можна переглянути:

- Ключові метрики (відсоток прибуткових угод, кількість трейдів, середнє співвідношення ризик/прибуток, загальний профіт). 
- Прибуток та Збиток по місяцям.
- Прибуток та Збиток по дням тижня.
- Кількість трейдів по місяцям.
- Відсотковий розподіл по результатам трейдів (прибуток/збиток/беззбиток).
- Розподіл за ліквідністю. 
- Розподіл трейдів по напрямку (long/short).

[Переглянути дашборд](https://lookerstudio.google.com/reporting/5afb8ce2-f730-4e19-9141-bc2b835bedc8)

## Інструкція
1. Завантажте дані про трейди з папки `Data`.
2. Відкрийте дашборд у Google Looker Studio за посиланням вище, щоб переглянути візуалізації.
3. Можна самостійно фільтрувати угоди по рокам, активу або торговій сесії для більш детального аналізу.

## Файли
- **data/trading_data.csv**: Основний файл з даними про всі угоди.
- **dashboard/dashboard_screenshot.png**: Знімок дашборду.
- **dashboard/dashboard_instructions.md**: Інструкція з користування дашбордом.

## Висновки
- Чітко вираженої сезонності стратегія немає (немає такого, що в якісь певні місяці року стратегія працює дуже погано, а в якісь дуже добре). Місяці спаду або зростання змінюються з року в рік, що свідчить про їхню залежність від глобальних циклів ринку.
- SP500 показує вищий відсоток прибуткових угод, але дає менше трейдів, ніж NAS100.
- В понеділок спостерігається більше збиткових угод у порівнянні з іншими днями тижня.
- Немає істотної різниці, чи була ліквідність сформована до чи під час торгової сесії.
  
## Контакти
- [LinkedIn профіль](https://www.linkedin.com/in/hlib-inozemtsev-670ba8124/)
- [GitHub репозиторій]()
