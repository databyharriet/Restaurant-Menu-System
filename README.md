# Restaurant Menu System

## Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Installation](#installation)
4. [Code Explanation](#code-explanation)
5. [How to Run](#how-to-run)
6. [Example Output](#example-output)
7. [How to Contribute](#how-to-contribute)
8. [License](#license)

## Overview
This project is a simple Python-based restaurant menu system that allows customers to order from a menu, specify the number of plates they wish to order, and calculates the total cost dynamically. The system offers three categories of food: **Normal**, **Swallow**, and **Soup**, each with its respective price. It also tracks the time of each purchase.

## Features
- **Multiple Categories**: The system allows customers to choose from three food categories: Normal, Swallow, and Soup.
- **Cost Calculation**: Automatically calculates the total cost based on the number of plates ordered.
- **Order Summary**: Displays an order summary with the items selected, quantities, and the total cost.
- **Timestamp**: Tracks the time of the purchase.
- **User-Friendly**: Prompts the user to select food categories and quantity in a simple and intuitive manner.

## Installation
1. ## Installation
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/databyharriet/Restaurant-Menu-System.git

   ```
2. Make sure you have Python installed (version 3.x+). You can download Python from [here](https://www.python.org/downloads/).

3. Navigate to the project folder and run the Python script.

## Code Explanation
### 1. **Menu Initialization**
The menu is stored in dictionaries for each category (Normal, Swallow, Soup), containing the available items and their corresponding prices.

```python
normal = {'rice': 200, 'dodo': 150, 'beans': 100, 'kpomo': 300, 'salad': 250}
swallow = {'garri': 400, 'semo': 350, 'fufu': 450, 'amala': 500}
soup = {'egusi': 700, 'ewedu': 650, 'gbegiri': 600, 'ofe nsala': 750, 'ofe owerri': 800, 'oha': 850}
```

### 2. **Order Handling**
The program allows the user to select a category and meal, enter the quantity, and then calculates the cost. The process is repeated until the user types `'done'`.

```python
while True:
    category = input("What category would you like to order from (normal, swallow, soup) or type 'done' to finish: ").lower()
    
    if category == 'done':
        break
    ...
```

### 3. **Cost Calculation**
For each selected meal, the script calculates the cost based on the number of plates ordered.

```python
cost = num_plates * price_per_plate
total_cost += cost
```

### 4. **Order Summary**
At the end, the program displays the final summary of the order, including itemized costs and total cost.

```python
if order_list:
    print("\nYour final order:")
    for item, quantity, cost in order_list:
        print(f"{quantity} plates of {item}: {cost} Naira")
    print(f"Total cost: {total_cost} Naira at {purchasing_time}")
```

## How to Run
1. Clone or download the repository.
2. Open the `restaurant_menu.py` file.
3. Run the script in your preferred Python environment (e.g., Jupyter Notebook, Command Line Interface, or Python IDE).
4. Follow the prompts to interact with the menu and place your order.

```bash
python restaurant_menu.py
```

## Example Output

Here is an example of the interaction when running the script:

```plaintext
Menu Options:
Normal: {'rice': 200, 'dodo': 150, 'beans': 100, 'kpomo': 300, 'salad': 250}
Swallow: {'garri': 400, 'semo': 350, 'fufu': 450, 'amala': 500}
Soup: {'egusi': 700, 'ewedu': 650, 'gbegiri': 600, 'ofe nsala': 750, 'ofe owerri': 800, 'oha': 850}

What category would you like to order from (normal, swallow, soup) or type 'done' to finish: normal
Available options: {'rice': 200, 'dodo': 150, 'beans': 100, 'kpomo': 300, 'salad': 250}
Please choose your meal: rice
How many plates you wan order?: 2
You have successfully added 2 plates of rice to your order. Cost: 400 Naira.

What category would you like to order from (normal, swallow, soup) or type 'done' to finish: done

Your final order:
2 plates of rice: 400 Naira
Total cost: 400 Naira at 2025-04-08 12:00:00
```

## How to Contribute
Feel free to fork this repository, submit pull requests, or open issues for suggestions and improvements. Any contributions are welcome!

## License
This project is open-source and licensed under the MIT License.

```

