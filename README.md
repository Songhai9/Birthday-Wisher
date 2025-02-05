# Birthday Wisher

A simple Python project that sends personalized birthday wishes via email. The project uses data from a CSV file and pre-written letter templates to automate the birthday greeting process.

## Overview

The script reads a list of birthdays from a CSV file (`birthdays.csv`). When the current date matches a birthday, the program selects a random letter template from the `letter_templates` directory, replaces the placeholder with the birthday person's name, and sends an email using SMTP.

## How It Works

1. **Load Environment Variables:**  
    The script reads email credentials from a `.env` file.

2. **Read Birthdays:**  
    Birthday data is stored in `birthdays.csv`. The script checks if today is any individual's birthday.

3. **Select a Template:**  
    If the birthday date matches, a random letter template from `letter_templates/letter_1.txt`, `letter_templates/letter_2.txt`, or `letter_templates/letter_3.txt` is selected.

4. **Personalize the Letter:**  
    The selected template has a placeholder `[NAME]` that is replaced with the actual name from the CSV file.

5. **Send an Email:**  
    The script sends the personalized birthday email using Gmail's SMTP server.

## Setup and Installation

1. **Install Dependencies:**

    Ensure you have Python installed and then install the required packages:

    ```bash
    pip install pandas python-dotenv
    ```

2. **Configure Environment:**

    Create a `.env` file in the root directory with your email credentials:

    ```env
    MY_EMAIL=your_email@gmail.com
    MY_PASSWORD=your_password
    ```

4. **Prepare Birthday Data:**

    Update `birthdays.csv` with the names, email addresses, and dates of birth of the recipients.

## Running the Project

Run the script using Python:

```bash
python main.py
```

## Notes
- Customize the letter templates in the `letter_templates` folder to suit your style.
