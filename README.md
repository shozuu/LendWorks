# LendWorks

A peer-to-peer rental marketplace platform that enables users to rent and lend items to each other securely.

## About

LendWorks is a web application that connects item owners (lenders) with people who need temporary access to those items (renters). The platform facilitates the entire rental lifecycle from listing creation to payment processing, with built-in verification, scheduling, and dispute resolution systems.

### Key Features

-   **Peer-to-Peer Rentals**: Users can list items for rent or browse and rent items from others
-   **User Verification**: Multi-layer verification including email, ID verification, and liveness detection
-   **Secure Payments**: Admin-verified payment system with deposit handling
-   **Scheduling System**: Flexible pickup and return scheduling with time slot management
-   **Proof Documentation**: Photo-based handover and return proof system
-   **Dispute Resolution**: Structured dispute handling for damaged item claims
-   **Admin Dashboard**: Comprehensive tools for platform management

### Rental Workflow

1. Lender creates a listing (pending admin approval)
2. Renter submits a rental request
3. Lender approves the request
4. Renter submits payment (rental fee + deposit)
5. Admin verifies payment
6. Pickup scheduling and item handover
7. Active rental period
8. Return scheduling and item return
9. Lender confirms item condition
10. Admin processes lender payment and deposit refund

## Tech Stack

-   **Backend**: Laravel (PHP)
-   **Frontend**: Inertia.js with Vue/React
-   **Styling**: Tailwind CSS
-   **Database**: MySQL

## Requirements

-   PHP 8.1+
-   Composer
-   Node.js and npm
-   MySQL

## Installation

1. Clone the repository:

    ```bash
    git clone <repository-url>
    cd LendWorks
    ```

2. Install PHP dependencies:

    ```bash
    composer install
    ```

3. Install JavaScript dependencies:

    ```bash
    npm install
    ```

4. Create environment file:

    ```bash
    cp .env.example .env
    ```

5. Configure your database in `.env`:

    ```
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=lendworks
    DB_USERNAME=your_username
    DB_PASSWORD=your_password
    ```

6. Generate application key:

    ```bash
    php artisan key:generate
    ```

7. Run database migrations:

    ```bash
    php artisan migrate
    ```

8. Create storage symlink:

    ```bash
    php artisan storage:link
    ```

9. Start the development server:

    ```bash
    php artisan serve
    ```

10. In a separate terminal, compile assets:
    ```bash
    npm run dev
    ```

The application will be available at `http://localhost:8000`.

## Project Structure

```
app/
├── Http/
│   ├── Controllers/       # Request handlers
│   │   └── Admin/         # Admin-specific controllers
│   ├── Middleware/        # Request middleware
├── Models/                # Eloquent models
├── Notifications/         # Notification classes
├── Policies/              # Authorization policies
├── Services/              # Business logic services
└── Traits/                # Reusable traits

resources/
├── css/                   # Stylesheets
├── js/                    # Frontend JavaScript
└── views/                 # Blade/Inertia views

routes/
├── web.php                # Web routes
└── auth.php               # Authentication routes
```

## Testing

Run the test suite using Pest:

```bash
php artisan test
```
