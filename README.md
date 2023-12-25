import tkinter as tk

def calculate():
    try:
        result = eval(entry.get())
        output_label.config(text="Result: " + str(result))
    except Exception as e:
        output_label.config(text="Error: " + str(e))

# تنظیمات اصلی پنجره
root = tk.Tk()
root.title("ماشین حساب ساده")

# ورودی و لیبل نمایش نتیجه
entry = tk.Entry(root, width=30)
entry.pack(padx=10, pady=10)

output_label = tk.Label(root, text="", font=("Arial", 12))
output_label.pack(padx=10, pady=5)

# دکمه محاسبه
calculate_button = tk.Button(root, text="محاسبه", command=calculate)
calculate_button.pack(padx=10, pady=5)

# بستن پنجره
close_button = tk.Button(root, text="بستن", command=root.destroy)
close_button.pack(padx=10, pady=5)

# اجرای برنامه
root.mainloop()
