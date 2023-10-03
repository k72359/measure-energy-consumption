# measure-energy-consumption
import random
import time

# Simulate energy consumption data
def generate_energy_data():
    return random.uniform(0, 10)  # Simulate values between 0 and 10 kWh

# Measure energy consumption over a period of time
total_consumption = 0
duration = 3600  # Duration in seconds (1 hour)

start_time = time.time()
while True:
    # Simulate energy consumption and accumulate total
    consumption = generate_energy_data()
    total_consumption += consumption
    
    # Print current consumption
    print(f"Current Consumption: {consumption:.2f} kWh")
    
    # Check if the desired duration has elapsed
    elapsed_time = time.time() - start_time
    if elapsed_time >= duration:
        break

# Print total consumption over the measurement period
print(f"Total Consumption: {total_consumption:.2f} kWh")
