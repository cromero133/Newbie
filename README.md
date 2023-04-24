# Import required libraries
from fpdf import FPDF

# Invoice Generator for Internet Installments Completed

# Company Information
company_name = "Your Company Name"
company_address = "Your Company Address"
company_phone_number = "Your Company Phone Number"
company_email = "Your Company Email"

# Invoice Information
invoice_number = "1234"
invoice_date = "2023-04-24"
due_date = "2023-05-24"

# Client Information
client_name = "Client Name"
client_address = "Client Address"
client_phone_number = "Client Phone Number"
client_email = "Client Email"

# Installment Information
total_amount = 1000.00
num_installments = 5
amount_per_installment = total_amount / num_installments

# Payment Information
total_amount_paid = 500.00
installments_completed = 3
remaining_amount = total_amount - total_amount_paid

# Contractor Information
contractor1_name = "Contractor Name 1"
pay_rate1 = 50.00

contractor2_name = "Contractor Name 2"
pay_rate2 = 75.00

contractor3_name = "Contractor Name 3"
pay_rate3 = 60.00

# Create PDF object
pdf = FPDF()

# Add a page
pdf.add_page()

# Set up fonts
pdf.set_font("Arial", size=12)
pdf.set_font("Arial", style="B", size=16)

# Insert company information
pdf.cell(0, 10, txt=company_name, ln=1, align="C")
pdf.cell(0, 10, txt=company_address, ln=1, align="C")
pdf.cell(0, 10, txt=company_phone_number, ln=1, align="C")
pdf.cell(0, 10, txt=company_email, ln=1, align="C")
pdf.ln(10)

# Insert invoice information
pdf.cell(0, 10, txt="Invoice Number: " + invoice_number, ln=1)
pdf.cell(0, 10, txt="Invoice Date: " + invoice_date, ln=1)
pdf.cell(0, 10, txt="Due Date: " + due_date, ln=1)
pdf.ln(10)

# Insert client information
pdf.cell(0, 10, txt=client_name, ln=1)
pdf.cell(0, 10, txt=client_address, ln=1)
pdf.cell(0, 10, txt=client_phone_number, ln=1)
pdf.cell(0, 10, txt=client_email, ln=1)
pdf.ln(10)

# Insert installment information
pdf.cell(0, 10, txt="Total Amount: $" + str(total_amount), ln=1)
pdf.cell(0, 10, txt="Number of Installments: " + str(num_installments), ln=1)
pdf.cell(0, 10, txt="Amount per Installment: $" + str(amount_per_installment), ln=1)
pdf.ln(10)

# Insert payment information
pdf.cell(0, 10, txt="Total Amount Paid: $" + str(total_amount_paid), ln=1)
pdf.cell(0, 10, txt="Installments Completed: " + str(installments_completed), ln=1)
pdf.cell(0, 10, txt="Remaining Amount: $" + str(remaining_amount), ln=1)
pdf.ln(10)

# Insert contractor information
pdf.cell(0
