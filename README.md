# bankmanagement

Description
The package bankmanagement is used to:

  - account: Create a Account and modify their transactions
  - balance: Transactions methods
  - user: Create a User and modify his accounts

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install bankmanagement

```bash
pip install bankmanagement
```

## Example

```python
from datetime import date
from bankmanagement import NaturalPerson, CheckingAccount

user = NaturalPerson("Rua A, 123", "12345678900", "João Silva", date(1990, 1, 1))
acc = CheckingAccount.new_account(1, user) 
# acc = CheckingAccount(1, user) 
# user.add_account(acc)

acc.deposit(1000000000)
acc.withdraw(200)
acc.withdraw(300)
acc.withdraw(50)
print(acc.string_statement()) # String statement
print(acc.statement) # List statement
```

## Author
FlowCreeper

## License
[MIT](https://choosealicense.com/licenses/mit/)