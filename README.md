# Step 1: Upload your Excel file
from google.colab import files
uploaded = files.upload()

# Step 2: Import pandas
import pandas as pd

# Step 3: Read the Excel file
df = pd.read_excel("school_students_duplicates.xlsx")

# Step 4: Remove duplicates
df_cleaned = df.drop_duplicates()

# Step 5: Show results
print("Before removing duplicates:", len(df))
print("After removing duplicates:", len(df_cleaned))

# Step 6: Save the cleaned file
df_cleaned.to_excel("school_students_cleaned.xlsx", index=False)
print("✅ Cleaned file saved as school_students_cleaned.xlsx")
