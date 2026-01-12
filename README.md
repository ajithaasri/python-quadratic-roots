# python-quadratic-roots

# Python program to find the roots of a quadratic equation

import math

# Input coefficients
a = float(input("Enter the first coefficient (a): "))
b = float(input("Enter the second coefficient (b): "))
c = float(input("Enter the third coefficient (c): "))

if a != 0.0:  # Check if it is a quadratic equation
    # Calculate discriminant
    d = (b ** 2) - (4 * a * c)

    if d == 0.0:
        print("The roots are real and equal.")
        r = -b / (2 * a)
        print("The roots are:", r, "and", r)

    elif d > 0.0:
        print("The roots are real and distinct.")
        r1 = (-b + math.sqrt(d)) / (2 * a)
        r2 = (-b - math.sqrt(d)) / (2 * a)
        print("The root1 is:", r1)
        print("The root2 is:", r2)

    else:
        print("The roots are imaginary.")
        rp = -b / (2 * a)
        ip = math.sqrt(-d) / (2 * a)
        print("The root1 is: {} + i{}".format(rp, ip))
        print("The root2 is: {} - i{}".format(rp, ip))

else:
    print("Not a quadratic equation.")

OUTPUT:

Enter the first coefficient (a): 1
Enter the second coefficient (b): -3
Enter the third coefficient (c): 2
The roots are real and distinct.
The root1 is: 2.0
The root2 is: 1.0
