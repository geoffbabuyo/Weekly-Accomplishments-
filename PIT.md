import tkinter as tk

def get_zodiac():
        month = int(month_entry.get())
    day = int(day_entry.get())
    
        if (month == 3 and day >= 21) or (month == 4 and day <= 19):
        result = "Aries"
    elif (month == 4 and day >= 20) or (month == 5 and day <= 20):
        result = "Taurus"
    elif (month == 5 and day >= 21) or (month == 6 and day <= 21):
        result = "Gemini"
    elif (month == 6 and day >= 22) or (month == 7 and day <= 22):
        result = "Cancer"
    elif (month == 7 and day >= 23) or (month == 8 and day <= 22):
        result = "Leo"
    elif (month == 8 and day >= 23) or (month == 9 and day <= 22):
        result = "Virgo"
    elif (month == 9 and day >= 23) or (month == 10 and day <= 23):
        result = "Libra"
    elif (month == 10 and day >= 24) or (month == 11 and day <= 21):
        result = "Scorpio"
    elif (month == 11 and day >= 22) or (month == 12 and day <= 21):
        result = "Sagittarius"
    elif (month == 12 and day >= 22) or (month == 1 and day <= 19):
        result = "Capricorn"
    elif (month == 1 and day >= 20) or (month == 2 and day <= 18):
        result = "Aquarius"
    elif (month == 2 and day >= 19) or (month == 3 and day <= 20):
        result = "Pisces"
    else:
        result = "Error! Invalid Date"
        
        result_label.config(text="You are a " + result)

root = tk.Tk()
root.title("Zodiac Finder")

# Month Input
month_label = tk.Label(root, text="Enter Birth Month (1-12):")
month_label.pack()

month_entry = tk.Entry(root)
month_entry.pack()

day_label = tk.Label(root, text="Enter Birth Day (1-31):")
day_label.pack()

day_entry = tk.Entry(root)
day_entry.pack()

submit_button = tk.Button(root, text="Submit", command=get_zodiac)
submit_button.pack()

result_label = tk.Label(root, text="")
result_label.pack()

root.mainloop()
