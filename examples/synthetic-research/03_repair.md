# Synthetic Research Note — Round 3

Date: 2025-03-02

For the specific update x_new = x - eta * f'(x) = (1 - 2*eta)*x, when x != 0 the loss strictly decreases if 0 < eta < 1.

This bound concerns this exact quadratic model and update rule. It does not assert convergence for every nonlinear function or adaptive optimizer.
