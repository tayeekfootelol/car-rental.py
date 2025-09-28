vehicles = {
    1: ("Sedan", 50),
    2: ("SUV", 80),
    3: ("Truck", 100),
    4: ("Coupe", 60),
    5: ("Van", 75)
}

trace_table = []

for i in range(10):
    print(f"\n--- Iteration {i+1} ---")
    vehicle_choice = int(input("Select a vehicle (1-5): "))
    duration = int(input("Enter rental duration (days): "))

    if vehicle_choice in vehicles:
        name, rate = vehicles[vehicle_choice]
        cost = rate * duration
        print(f"Vehicle: {name}, Duration: {duration} days, Cost: ${cost}")
        trace_table.append((vehicle_choice, name, duration, cost))
    else:
        print("Invalid vehicle selection.")
        trace_table.append((vehicle_choice, "Invalid", duration, 0))

print("\n--- Trace Table ---")
print(f"{'Iter':<5}{'Vehicle':<10}{'Name':<10}{'Days':<6}{'Cost':<6}")
for idx, (v_id, v_name, days, cost) in enumerate(trace_table, start=1):
    print(f"{idx:<5}{v_id:<10}{v_name:<10}{days:<6}{cost:<6}")
