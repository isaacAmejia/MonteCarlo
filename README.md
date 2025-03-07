# MonteCarlo
Overview
This project uses Monte Carlo simulation to optimize a hotel's overbooking strategy. By analyzing the variability in demand, cancellations, and overbooking costs, the goal is to determine the ideal number of reservations that will maximize revenue while minimizing the risks associated with overbooking penalties. The simulation models the potential demand for hotel rooms, calculates the resulting revenue, and identifies the best reservation strategy.

Key Components
Room Price: $120 to $285 per night.
Overbooking Cost: $150 per overbooked reservation.
Total Rooms Available: 300 rooms.
Reservations Possible: 310 reservations (indicating potential overbooking).
Cancellation Probability: 4% for each accepted reservation.
Demand Distribution: Ranges from 280 to 335 guests with associated probabilities.
The simulation runs 1,000 trials, calculating Guest Arrivals after cancellations and comparing it to the ideal occupancy of 300 guests to determine the maximum revenue.

Problem 1: Probability of Maximum Profit with 310 Reservations Accepted
Solution Overview
To determine the probability of the hotel generating maximum profit with 310 reservations accepted, the following steps were performed:

Set Fixed Variables:
Key variables such as Room Price, Overbooking Cost, Total Rooms Available, and Reservations Possible are set in the simulation. A VLOOKUP table generates demand based on the frequency distribution.

Reservation Limit Check:
An IF statement ensures that no more than 310 reservations are accepted, setting the Actual Accepted Reservations to either the actual demand or 310, whichever is lower.

Cancellation Simulation:
The BINOM.INV function simulates the number of cancellations, using a 4% cancellation probability. The number of cancellations is subtracted from the Actual Accepted Reservations to determine the Guest Arrivals.

Maximizing Revenue:
The hotel generates maximum profit when Guest Arrivals = 300. A data table with 1,000 trials tracks the occurrence of this condition. A COUNTIF statement checks how many times 300 guest arrivals occur, and the result is divided by 1,000 trials to calculate the probability of maximum revenue (P(Max Rev) = 6.8%).

Visualization:
A chart visualizes the number of times maximum revenue was achieved across 1,000 trials.

Problem 2: Best Reservation Limit to Maximize Revenue
Solution Overview
To determine the best reservation limit to achieve maximum revenue, the following steps were taken:

Revenue Calculation:
The revenue function is used to calculate revenue based on the number of accepted reservations and the actual number of guest arrivals.

2-Way Data Table:
A 2-way data table is created with reservations possible as the row input and revenue as the reference. Reservation limits are tested in intervals of 5, starting from 300 up to 335.

Averages and Charting:
The averages for each column in the data table are calculated, and a line chart is generated to visualize revenue as it changes with different reservation limits.

Optimal Reservation Limit:
The analysis suggests that the hotel generates the highest revenue when accepting 310 reservations.

Conclusion
This simulation provides valuable insights into revenue optimization and helps identify the most effective overbooking strategy for the hotel. By balancing the risks of overbooking and cancellations, this analysis aids in making data-driven decisions that maximize hotel profitability.

Skills Used
Monte Carlo Simulation
Excel Formulas & Functions: IF, BINOM.INV, COUNTIF, VLOOKUP
Data Analysis & Interpretation
Revenue Optimization
Scenario Analysis
Statistical Modeling
Visualization & Reporting
Data Sources
The simulation uses hypothetical data and fixed variables based on typical hotel operations. The probabilistic demand and cancellation rates are user-defined for the purpose of this simulation.
