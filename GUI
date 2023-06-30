import tkinter as tk

def calculate_egfr():
    try:
        age = int(age_entry.get())
        serum_creatinine = float(creatinine_entry.get())
        gender = gender_var.get()

        # Validate input values
        if age <= 0 or serum_creatinine <= 0:
            raise ValueError("Age and serum creatinine must be positive numbers.")

        # Apply appropriate medical guidelines
        if gender == "Male":
            adjustment_factor = 1.0
        else:
            adjustment_factor = 0.742

        # Calculate eGFR using Mayo Quadratic equation
        egfr = 186 * (serum_creatinine ** (-1.154)) * (age ** (-0.203)) * adjustment_factor
        result_label.config(text="Estimated Glomerular Filtration Rate (eGFR): {:.2f} mL/min/1.73m²".format(egfr))

    except ValueError as err:
        result_label.config(text="Error: {}".format(str(err)))

# Create the main window
window = tk.Tk()
window.title("eGFR Calculator")

# Create input labels and entry fields
age_label = tk.Label(window, text="Patient's Age:")
age_label.pack()
age_entry = tk.Entry(window)
age_entry.pack()

creatinine_label = tk.Label(window, text="Serum Creatinine (mg/dL):")
creatinine_label.pack()
creatinine_entry = tk.Entry(window)
creatinine_entry.pack()

gender_label = tk.Label(window, text="Patient's Gender:")
gender_label.pack()

gender_var = tk.StringVar()
gender_radio_male = tk.Radiobutton(window, text="Male", variable=gender_var, value="Male")
gender_radio_male.pack()

gender_radio_female = tk.Radiobutton(window, text="Female", variable=gender_var, value="Female")
gender_radio_female.pack()

# Create the Calculate button
calculate_button = tk.Button(window, text="Calculate", command=calculate_egfr)
calculate_button.pack()

# Create a label to display the result
result_label = tk.Label(window, text="")
result_label.pack()

# Start the main event loop
window.mainloop()
