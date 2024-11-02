# Black-Scholes-Monte-Carlo-Simulation-for-Option-Pricing
This project implements the Black-Scholes model and Monte Carlo simulation for pricing European Call and Put options. It includes an interactive Jupyter Notebook with a GUI to input parameters, run simulations, and visualize stock price paths and option price convergence with confidence intervals.

## Features
- **Black-Scholes Model**: Calculates the price of European call and put options.
- **Monte Carlo Simulation**: Simulates stock price paths and estimates the option price with confidence intervals.
- **Interactive GUI**: Input key parameters like stock price, strike price, volatility, and more.
- **Visualizations**: Plotly-based visualizations of stock price paths and convergence of the Monte Carlo simulation.

## Theoretical Background
### Black-Scholes Model
The Black-Scholes model calculates the price of European options based on:
- Spot price  $S$ 
- Strike price  $K$ 
- Time to maturity $T$
- Risk-free interest rate $r$
- Volatility $\sigma$

The option price is given by:

$$
C(S, K, T, r, \sigma) = S N(d_1) - K e^{-rT} N(d_2)
$$


Where:

$$
d_1 = \frac{\ln(S/K) + (r + 0.5 \sigma^2) T}{\sigma \sqrt{T}}, \quad d_2 = d_1 - \sigma \sqrt{T}
$$

For put options, the price is:

$$
P(S, K, T, r, \sigma) = K e^{-rT} N(-d_2) - S N(-d_1)
$$

### Monte Carlo Simulation
Monte Carlo simulation estimates the option price by simulating random stock price paths and calculating the average payoff:

$$
\text{Payoff} = \max(S_T - K, 0) \quad \text{(for call option)}
$$

$$
\text{Payoff} = \max(K - S_T, 0) \quad \text{(for put option)}
$$

Where $S_T$ is the stock price at maturity.


### Put-Call Parity
Put-call parity is a financial principle that defines the relationship between the price of European call and put options with the same strike price and Time to maturity. It is expressed as:

$$
C + K e^{-rT} = P + S
$$


## Project Structure
- `black_scholes`: Calculates option prices using the Black-Scholes formula.
- `monte_carlo`: Simulates stock price paths and estimates option prices.
- `check_put_call_parity`: Validates put-call parity.
- **GUI Interface**: Interactive elements for user input and output display.

## Installation
To run the project, follow these steps:

1. Clone the repository:
   ```bash
   git clone  https://github.com/dereck1212/Black-Scholes-Monte-Carlo-Simulation-for-Option-Pricing.git
   
2. Install dependencies
   ```bash
   pip install numpy pandas plotly scipy ipywidgets ipython


3. Open the notebook file and interact with the GUI


## Example

Here’s a visualization of the graphical interface :

<img width="1325" alt="Screenshot 2024-09-23 at 14 29 52" src="https://github.com/user-attachments/assets/b53f2b66-4b32-41f8-b92e-6479a6820354">

Here’s a sample visualization of the resulting plots :

![newplot](https://github.com/user-attachments/assets/f475eebf-08cf-4ae1-8d1b-7fa65bc0d72d)



