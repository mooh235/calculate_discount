python
# Step 1: Define the calculate_discount function
def calculate_discount(price, discount_percent):
    if discount_percent >= 20:  # Check if the discount is 20% or higher
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price  # Return the original price if the discount is less than 20%

# Step 2: Prompt the user for input and use the function
try:
    # Get the original price from the user
    price = float(input("Enter the original price of the item: "))
    
    # Get the discount percentage from the user
    discount_percent = float(input("Enter the discount percentage: "))
    
    # Calculate the final price using the function
    final_price = calculate_discount(price, discount_percent)
    
    # Print the result
    if final_price == price:
        print(f"No discount applied. The original price is: ${price:.2f}")
    else:
        print(f"The final price after applying the discount is: ${final_price:.2f}")
except ValueError:
    print("Please enter valid numeric values for the price and discount percentage.")
```

*Explanation:*
1. The `calculate_discount` function checks if the discount percentage is 20% or higher. If so, it calculates and applies the discount. Otherwise, it returns the original price.
2. The program prompts the user to input the price and discount percentage, ensuring valid numeric input with a `try-except` block.
3. The final price is printed, with a conditional check to differentiate whether the discount was applied or not.
