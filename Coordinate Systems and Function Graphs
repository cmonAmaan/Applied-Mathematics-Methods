# -*- coding: utf-8 -*-
"""
Homework 1 - Computational Math Methods
Author: Amaan
Date: January 30, 2023
Description: Numerical computations, function plotting, and coordinate conversions.
"""

import numpy as np
from matplotlib import pyplot as plt
if not os.path.exists("results"):
    os.makedirs("results")
### Problem 1: Numerical Computation
def compute_expression():
    """
    Purpose: Verify the result of the given mathematical expression.
    Inputs: None
    Outputs: Numerical result
    """
    a = 2 - np.log10(1 + 2**3.2)
    b = 2 + np.log(5.1 - np.abs(np.cos(9)))
    result = a / b
    print("Result of expression a/b:", result)

compute_expression()

### Problem 2: Plotting T(theta)
def plot_T_theta():
    """
    Purpose: Plot the function T(theta) = 1 / (0.2 + sin(theta)) for -2 <= theta <= 6.
    Inputs: None
    Outputs: Saves the plot as 'plot_T_theta.png'.
    """
    theta = np.linspace(-2, 6, 100)
    T = 1 / (0.2 + np.sin(theta))
    plt.figure()
    plt.plot(theta, T, color='blue')
    plt.xlabel("Theta")
    plt.ylabel("T(Theta)")
    plt.title("Plot of T(Theta)")
    plt.grid()
    plt.savefig("results/plot_T_theta.png")
    plt.show()

plot_T_theta()

### Problem 3: Cylindrical Coordinate Conversion
def cylindrical_coordinates(x, y, z):
    """
    Purpose: Converts Cartesian coordinates (x, y, z) to cylindrical coordinates.
    Inputs:
        x: numerical
        y: numerical
        z: numerical
    Outputs:
        r: radial distance
        theta: angle in radians
        z: height
    """
    r = np.sqrt(x**2 + y**2)
    theta = np.arctan2(y, x)
    return r, theta, z

x, y, z = 2, 1, 0
r, theta, z = cylindrical_coordinates(x, y, z)
print("Cylindrical Coordinates:")
print(f"r = {r}, theta = {theta}, z = {z}")

### Problem 4: Advanced Plotting
def advanced_plotting():
    """
    Purpose: Create advanced plots for g(x) and additional functions.
    Outputs: Saves plots as 'fig1_plot.png' and 'fig2_plot.png'.
    """
    # First plot
    x = np.linspace(-np.pi, np.pi, 200)
    g = np.sqrt(3)/np.pi * x * (np.pi - x) * (np.pi + x)
    fig1, ax1 = plt.subplots()
    ax1.plot(x, g, label='g(x)')
    ax1.plot(x, np.pi * g, color='red', linewidth=3, label='x/pi * g(x)')
    ax1.set_xlabel('x-axis')
    ax1.set_ylabel('y-axis')
    ax1.legend()
    plt.title('Plot of g(x)')
    plt.grid()
    fig1.savefig("results/fig1_plot.png")
    plt.show()

    # Second plot
    x2 = np.linspace(0, 2*np.pi, 200)
    sin_x = np.sin(x2)
    cos_x = np.cos(x2)
    cos2x_gx = np.cos(2*x2) * g[:len(x2)]
    fig2, ax2 = plt.subplots()
    ax2.plot(x2, sin_x, label='sin(x)')
    ax2.plot(x2, cos_x, label='cos(x)')
    ax2.plot(x2, cos2x_gx, color='magenta', linewidth=2, label='cos(2x) * g(x)')
    ax2.set_xlabel('x-axis')
    ax2.set_ylabel('y-axis')
    ax2.legend()
    plt.title('Plot of Trigonometric Functions')
    plt.grid()
    fig2.savefig("results/fig2_plot.png")
    plt.show()

advanced_plotting()
