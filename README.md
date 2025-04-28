# week-3-asssignment-
def calculate_discount(price, discount_percent):
  """Calculates the final price after applying a discount if it's 20% or higher.

  Args:
    price: The original price of the item.
    discount_percent: The discount percentage (e.g., 20 for 20%).

  Returns:
    The final price after discount, or the original price if the discount is less than 20%.
  """
  if discount_percent >= 20:
    discount_amount = price * (discount_percent / 100)
    final_price = price - discount_amount
    return final_price
  else:
    return price

# --- Code to prompt user and print result ---

original_price_str = input("Enter the original price of the item: ")
discount_percent_str = input("Enter the discount percentage: ")

try:
  original_price = float(original_price_str)
  discount_percent = float(discount_percent_str)
  final_price = calculate_discount(original_price, discount_percent)
  print(f"The final price is: {final_price}")
except ValueError:
  print("Invalid input. Please enter numeric values for price and discount percentage.")
