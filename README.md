# 🛒 Supermarket Management System

A complete **PHP & MySQL-based supermarket management system**, designed to handle daily store operations such as managing products, suppliers, customers, employees, and invoices.  
This project demonstrates both **database design** and **backend logic** using PHP and SQL.

---

## 📂 Project Overview

This project was developed as part of my **Database and Web Design** program at KPT.  
It simulates a real-world supermarket system where the admin can:
- Manage products and stock
- Add and edit suppliers and customers
- Create and track invoices
- Record employee activity and logs
- Handle orders from customers and suppliers

---

## 🧱 Database Structure

**Database name:** `supermarket`  
**Total tables:** 9

| Table Name | Description |
|-------------|-------------|
| `fatura` | Stores customer invoices |
| `furnitoret` | Information about suppliers |
| `klientet` | List of supermarket customers |
| `porosingaklientet` | Orders placed by clients |
| `porosingaklientet_produkt` | Products included in each client order |
| `porosiperfurnitoret` | Orders made to suppliers |
| `produktet` | Product catalog with prices, stock, and supplier links |
| `punonjesit` | Employee information |
| `punonjesit_logs` | Records employee login and activities |

---

## 💾 Files Included

| File | Description |
|------|--------------|
| `supermarket.sql` | Full database schema and data dump |
| `config.php` | Database connection settings |
| `index.php` | Dashboard login or homepage |
| `dashboard.php` | Admin dashboard overview |
| `add_product.php` | Add new products |
| `update_stock.php` | Update product stock |
| `delete_product.php` | Remove product entries |
| `view_product.php` | View product details |
| `create_invoice.php` | Generate invoices for clients |
| `styles.css` | CSS design for interface |
| `supermarket.jpg` | Screenshot or logo of the system |


## 🧮 Example SQL Queries

**1. Total sales per customer**
```sql
SELECT k.emer AS klient, SUM(pcm.sasia * pr.cmimi) AS total
FROM porosingaklientet_produkt pcm
JOIN produktet pr ON pr.id = pcm.id_produkt
JOIN porosingaklientet pk ON pk.id_porosi = pcm.id_porosi
JOIN klientet k ON k.id_klient = pk.id_klient
🧰 Tools & Technologies

PHP 8.2+

MySQL / phpMyAdmin

HTML5 / CSS3

XAMPP / Apache Server

GitHub for version control
GROUP BY k.emer;
👩‍💻 Author

Glejda Silaj
📍 Albania
🎓 Database & Web Design Student Tirana collage of technology
💼 Interested in Web & Database Development

