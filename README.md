def fizz_buzz():
    for n in range(1, 101):
        if n % 3 == 0 and n % 5 == 0:
            print("FizzBuzz")
        elif n % 3 == 0:
            print("Fizz")
        elif n % 5 == 0:
            print("Buzz")
        else:
            print(n)

fizz_buzz()
import math

def l2_norm(vector):
    return math.sqrt(sum(x ** 2 for x in vector))

# Example usage
print(l2_norm([3, 4]))  # Should print 5.0
def lp_norm(vector, p):
    return sum(abs(x) ** p for x in vector) ** (1 / p)

# Example usage
print(lp_norm([3, 4], 2))  # Should match l2_norm([3,4])

# Rewrite l2_norm using lp_norm
def l2_norm(vector):
    return lp_norm(vector, 2)
