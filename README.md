# Vehicle Service Management System

A Python and MySQL based Vehicle Service Management System that manages customers, vehicle servicing, spare parts inventory, smart service recommendations, and PDF bill generation.

## Features

- **Customer Management**: Add, view, search, and manage customer information with vehicle details
- **Service Booking**: Book vehicle services with mechanic assignment and status tracking
- **Service History**: Track complete service history for each vehicle
- **Spare Parts Inventory**: Manage spare parts stock with automatic low stock alerts
- **Smart Service Recommendations**: AI-driven service recommendations based on vehicle age (months) and mileage (KM)
  - Basic Service: For new vehicles
  - Oil Change: Every 6 months or 5,000 KM
  - Full Service: Every 12 months or 10,000 KM
  - Major Service: Every 24 months or 20,000 KM
- **PDF Bill Generation**: Auto-generate detailed service bills with parts used and GST calculation
- **Stock Management**: Real-time inventory tracking with warnings for low stock and out-of-stock items
- **Bill History**: Store and retrieve all service bills with complete details

## Technologies Used

- **Language**: Python 3.x
- **Database**: MySQL
- **PDF Generation**: ReportLab
- **Database Connector**: mysql-connector-python
- **Additional Libraries**:
  - `datetime` - Date and time operations
  - `os` - File operations

## Modules

### 1. **Customer Module**
   - `add_customer()` - Register new customers with vehicle information
   - `view_customers()` - Display all customers in the system
   - `search_customer()` - Search customers by phone or vehicle number
   - `update_km()` - Update current mileage of vehicles

### 2. **Service Module**
   - `book_service()` - Book new service appointments
   - `update_service()` - Update service status (Pending/In Progress/Completed)
   - `service_history()` - View complete service history for a vehicle

### 3. **Spare Parts Module**
   - `add_part()` - Add new spare parts to inventory
   - `view_parts()` - Display all available spare parts with stock details
   - `update_part_stock()` - Update inventory quantity with low stock alerts

### 4. **Smart Service Module**
   - `smart_service()` - Provides intelligent service recommendations based on:
     - Vehicle purchase date and current age
     - Current mileage
     - Service intervals

### 5. **Billing & PDF Module**
   - `generate_pdf_bill()` - Generate comprehensive service bills with:
     - Service charges
     - Spare parts details
     - GST calculation (18%)
     - Final amount
     - Automatic PDF file generation and display

### 6. **Main Menu**
   - `main()` - Interactive command-line interface for all operations
   - 13 menu options for easy navigation

## Database Tables

1. **customers** - Stores customer and vehicle information
2. **services** - Records service bookings and status
3. **spare_parts** - Maintains inventory of spare parts
4. **bills** - Stores billing information and history

## Installation

```bash
pip install mysql-connector-python reportlab
```

## Usage

1. Configure MySQL database connection in the script:
   ```python
   host="127.0.0.1",
   user="root",
   password="your_password",
   database="vehicle_service_db"
   ```

2. Create the required database tables

3. Run the application:
   ```bash
   python main.py
   ```

4. Select options from the interactive menu

## Key Features Highlight

✅ Complete customer lifecycle management  
✅ Automated service recommendations  
✅ Real-time inventory management  
✅ Professional PDF bill generation  
✅ Low stock alert system  
✅ Service history tracking  
✅ Simple and intuitive CLI interface  

## Future Enhancements

- Web-based UI using Flask/Django
- Email notifications for service reminders
- Advanced reporting and analytics
- Payment integration
- Customer portal for online booking
