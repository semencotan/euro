# euro
from forex_python.converter import CurrencyRates

def convert_eur_to(target_currency, amount):
    c = CurrencyRates()
    rate = c.get_rate('EUR', target_currency)
    converted_amount = amount * rate
    return converted_amount

# Example usage:
euros = 100
target_currency = 'USD'
converted_amount = convert_eur_to(target_currency, euros)
print(f"{euros} Euros is equal to {converted_amount} {target_currency}")
