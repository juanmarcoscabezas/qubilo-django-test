# Django API Technical Test

## Objective
Create a Django API to manage `CreditAccount`, `Card`, and `Transaction` entities. The goal is to create basic CRUD (Create, Read, Update, Delete) operations for each entity.

## Entities

1. **CreditAccount**
   - Fields:
     - `account_number` (string, unique)
     - `balance` (decimal)
     - `credit_limit` (decimal)

2. **Card**
   - Fields:
     - `card_number` (string, unique)
     - `expiration_date` (date)
     - `credit_account` (ForeignKey to `CreditAccount`)

3. **Transaction**
   - Fields:
     - `transaction_id` (string, unique)
     - `amount` (decimal)
     - `transaction_date` (date)
     - `card` (ForeignKey to `Card`)

## Tasks

### 1. Set up the Django Project
- Create a new Django project and app.
- Install Django REST Framework for API development.

### 2. Create Models
- Implement models for `CreditAccount`, `Card`, and `Transaction` according to the fields described above.

### 3. Create Serializers
- Create serializers for `CreditAccount`, `Card`, and `Transaction` to handle input and output for the API.

### 4. Create Endpoints (API Views)
- Use Django REST Framework to implement CRUD endpoints for each model.
  - **CreditAccount**: `/api/credit-accounts/`
  - **Card**: `/api/cards/`
  - **Transaction**: `/api/transactions/`

### 5. Testing
- Write unit tests for the API using **pytest**.
- Ensure each endpoint is covered, and tests are implemented for all CRUD operations.

### 6. Docker (Optional)
- Provide a `Dockerfile` and `docker-compose.yml` to set up the development environment.

## API Specifications

### Endpoints

#### CreditAccount
- **GET** `/api/credit-accounts/`: List all credit accounts.
- **POST** `/api/credit-accounts/`: Create a new credit account.
- **GET** `/api/credit-accounts/{id}/`: Retrieve details of a specific credit account.
- **PUT** `/api/credit-accounts/{id}/`: Update a credit account.
- **DELETE** `/api/credit-accounts/{id}/`: Delete a credit account.

#### Card
- **GET** `/api/cards/`: List all cards.
- **POST** `/api/cards/`: Create a new card.
- **GET** `/api/cards/{id}/`: Retrieve details of a specific card.
- **PUT** `/api/cards/{id}/`: Update a card.
- **DELETE** `/api/cards/{id}/`: Delete a card.

#### Transaction
- **GET** `/api/transactions/`: List all transactions.
- **POST** `/api/transactions/`: Create a new transaction.
- **GET** `/api/transactions/{id}/`: Retrieve details of a specific transaction.
- **PUT** `/api/transactions/{id}/`: Update a transaction.
- **DELETE** `/api/transactions/{id}/`: Delete a transaction.

### Testing Instructions
1. Run the tests using `pytest`:
   ```bash
   pytest
