# CBR Currency API

Библиотека для работы с курсами валют ЦБ РФ.

## Установка

`pip install cbr-currency-api`

## Использование
```python
import asyncio
from decimal import Decimal
from crb_currency_api import CrbCurrencyAPI

async def main():
    api = CrbCurrencyAPI()
    rate = await api.get_currency_rate("USD")
    print(f"Курс USD: {rate}")

    result = await api.exchange("USD", "EUR", Decimal("100"))
    print(f"100 USD = {result} EUR")

asyncio.run(main())
```