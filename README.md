# Python_individual_task2
```py
class Client:
  number_of_clients = 0
  def __init__(self, id, name):
    self.id = id
    self.name = name
    self.transactions = []
    Client.number_of_clients += 1

  def add_transaction(self, transaction):
      self.transactions.append(transaction)

class Item:
  def __init__(self, id, name, price):
        self.id = id
        self.name = name
        self.price = price

class Transaction:
  def __init__(self, id, items):
        self.id = id
        self.items = items

def print_clients():
  for client in clients:
    print(client.name)

clients = []
clients.append(Client('12222', 'Peteris'))
clients.append(Client('23333', 'Gunars'))
clients.append(Client('34444', 'Jautrite'))

items = []
items.append(Item('1001', 'Table', 70))
items.append(Item('2002', 'Chair', 35))
items.append(Item('3003', 'Wardrobe', 140))


clients[0].add_transaction(Transaction('1', [items[0], items[2]]))
clients[1].add_transaction(Transaction('2', [items[1], items[0]]))
clients[2].add_transaction(Transaction('3', [items[2], items[1]]))


print(f'Shop has {Client.number_of_clients} clients:')
print_clients()

for client in clients:
  print(f'Client {client.name} has bought:')
  for transaction in client.transactions:
    for item in transaction.items:
      print(item.name)
```

