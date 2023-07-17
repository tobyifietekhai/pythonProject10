class Account:
    def __init__(self, account_number, account_holder, balance=0.0):
        self.account_number = account_number
        self.account_holder = account_holder
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount
        print(f"Deposited {amount} into Account {self.account_number}. Current balance: {self.balance}")

    def withdraw(self, amount):
        if self.balance >= amount:
            self.balance -= amount
            print(f"Withdrew {amount} from Account {self.account_number}. Current balance: {self.balance}")
        else:
            print("Insufficient balance.")

    def get_balance(self):
        print(f"Account {self.account_number} balance: {self.balance}")


class Bank:
    def __init__(self):
        self.accounts = []

    def create_account(self, account_number, account_holder, initial_deposit=0.0):
        account = Account(account_number, account_holder, initial_deposit)
        self.accounts.append(account)
        print(f"Account {account_number} created successfully.")

    def get_account(self, account_number):
        for account in self.accounts:
            if account.account_number == account_number:
                return account
        print(f"Account {account_number} not found.")
        return None


# Usage example
bank = Bank()

# Create accounts
bank.create_account(1001, "John Doe", 1000.0)
bank.create_account(1002, "", 500.0)

# Deposit money
account1 = bank.get_account(1001)
account1.deposit(500.0)

# Withdraw money
account2 = bank.get_account(1002)
account2.withdraw(200.0)

# Get balance
account1.get_balance()
account2.get_balance()

