# week-3-asssignment-
def calculate_discount(price, discount_percent):
  """
  Calculates the final price after applying a discount if it's 20% or higher.

  Args:
    price: The original price of the item (float or int).
    discount_percent: The discount percentage (float or int, e.g., 20 for 20%).

  Returns:
    The final price after discount, or the original price if the discount is less than 20%.
  """
  
  if discount_percent >= 20:
    # Calculate the discount amount
    discount_amount = price * (discount_percent / 100)
    # Calculate the final price by subtracting the discount
    final_price = price - discount_amount
    return final_price
  else:
    # If the discount is less than 20%, return the original price
    return price

original_price_str = input("Enter the original price of the item: ")
discount_percent_str = input("Enter the discount percentage: ")

  original_price = float(original_price_str)
  discount_percent = float(discount_percent_str)


  final_price = calculate_discount(original_price, discount_percent)

  print(f"The final price is: {final_price:.2f}") # Format to 2 decimal places

except ValueError:

  print("Invalid input. Please enter numeric values for price and discount percentage.")

