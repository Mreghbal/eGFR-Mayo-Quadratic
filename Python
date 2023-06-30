def calculate_egfr(age, serum_creatinine, is_male):
    try:
        # Validate input values
        if age <= 0 or serum_creatinine <= 0:
            raise ValueError("Age and serum creatinine must be positive numbers.")
        
        # Apply appropriate medical guidelines
        if is_male:
            adjustment_factor = 1.0
        else:
            adjustment_factor = 0.742
        
        # Calculate eGFR using Mayo Quadratic equation
        egfr = 186 * (serum_creatinine ** (-1.154)) * (age ** (-0.203)) * adjustment_factor
        return egfr

    except ValueError as err:
        print("Error:", err)
        return None


# Example usage
age_input = int(input("Enter patient's age: "))
creatinine_input = float(input("Enter serum creatinine level (mg/dL): "))
gender_input = input("Enter patient's gender (M/F): ").upper()

if gender_input == "M":
    is_male_input = True
elif gender_input == "F":
    is_male_input = False
else:
    print("Invalid gender input. Please enter 'M' for male or 'F' for female.")
    exit()

egfr_result = calculate_egfr(age_input, creatinine_input, is_male_input)

if egfr_result is not None:
    print("Estimated Glomerular Filtration Rate (eGFR):", round(egfr_result, 2), "mL/min/1.73m²")
