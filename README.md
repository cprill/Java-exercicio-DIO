# Java API

## Exercício de Java RESTful API - DIO

### JASON
```
{
  "name": "Venilton",
  "account": {
    "number": "00000000-0",
    "agency": "0000",
    "balance": 1324.64,
    "limit": 1000.00
  },
  "features": [
    {
      "icon": "URL",
      "description": "Descricao da Feature" 
    }
  ],
  "card": {
    "number": "Xxxxx XxXXX XXXX 0000",
    "limit": 1000.00 
  },
  "news": [
    {
      "icon": "URL", 
      "description": "Descrig¢ao da Novidade"
    }
  ]
}
```

### Diagrama

```mermaid
classDiagram
    class User {
        -string name
        -Account account
        -Feature[] features
        -Card card
        -News[] news
    }

    class Account {
        -string number
        -string agency
        -float balance
        -float limit
    }

    class Feature {
        -string icon
        -string description
    }

    class Card {
        -string number
        -float limit
    }

    class News {
        -string icon
        -string description
    }

    User "1" *-- "1" Account
    User "1" *-- "N" Feature
    User "1" *-- "1" Card
    User "1" *-- "N" News
```
