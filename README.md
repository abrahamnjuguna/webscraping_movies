

# Web Scraping and Data Extraction Lab

This repository contains a hands-on lab project focused on web scraping and data extraction using Python. By completing this lab, you will gain proficiency in scraping web data and extracting specific information using APIs, libraries like `requests`, and `BeautifulSoup`. The extracted data is processed, stored in a SQLite database, and exported as a CSV file for further use.

## Objectives

By the end of this lab, you will be able to:

- Use the `requests` and `BeautifulSoup` libraries to extract web page content.
- Analyze the HTML structure of a webpage to identify relevant data.
- Extract and organize the required information.
- Store the data in a SQLite database and export it as a CSV file.

## Dataset

The project scrapes the top 50 movies with the best average ratings from the following webpage:

[100 Most Highly-Ranked Films](https://web.archive.org/web/20230902185655/https://en.everybodywiki.com/100_Most_Highly-Ranked_Films)

### Extracted Information

- **Average Rank**: The movie's rank based on its average rating.
- **Film**: The title of the movie.
- **Year**: The year the movie was released.

## Project Files

- **`webscraping_movies.py`**: The main Python script for web scraping, data processing, and storage.
- **`Movies.db`**: SQLite database containing the extracted data.
- **`top_50_films.csv`**: CSV file with the extracted data.

## Prerequisites

- Python 3.x installed on your machine.
- Basic understanding of Python and libraries such as `pandas`, `requests`, `sqlite3`, and `BeautifulSoup`.

## Setup and Usage

Follow these steps to set up and run the project:

### 1. Clone the Repository

```bash
# Clone the repository to your local machine
git clone <repository_url>
cd <repository_directory>
```

### 2. Create and Activate a Virtual Environment

#### On Windows:

```bash
python -m venv env
env\Scripts\activate
```

#### On macOS/Linux:

```bash
python3 -m venv env
source env/bin/activate
```

### 3. Install Dependencies

Install the required Python libraries using `pip`:

```bash
pip install -r requirements.txt
```

### 4. Run the Script

Run the Python script to scrape the data and store it in the database and CSV file:

```bash
python3 webscraping_movies.py
```

### 5. Verify Outputs

- **CSV File**: The extracted data will be saved as `top_50_films.csv` in the project directory.
- **Database**: A SQLite database `Movies.db` will contain the data in a table named `Top_50`.

## Project Workflow

1. **Web Scraping**:

   - The script fetches the webpage's HTML content using `requests`.
   - Parses the HTML using `BeautifulSoup` to locate the required data in the `<tbody>` section of the table.

2. **Data Processing**:

   - Extracts movie data (rank, title, and year) and stores it in a `pandas` DataFrame.
   - Processes only the top 50 movies.

3. **Data Storage**:

   - Saves the processed data into a CSV file (`top_50_films.csv`).
   - Stores the data in a SQLite database (`Movies.db`).

## Requirements File

Below is a sample `requirements.txt` file for installing dependencies:

```


```

## Contribution

Feel free to contribute to this project by submitting issues or creating pull requests. For major changes, please discuss them in an issue first.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

