# MapReduce Grep Algorithm for Efficient Text Search

## Overview

This project implements a simplified version of the grep command-line utility using the MapReduce paradigm. The goal is to efficiently search for strings across multiple text files in a directory, making it suitable for handling large datasets. The implementation includes features like case-insensitive search and detailed match location reporting.

## Key Features

- **MapReduce Framework**: Utilizes parallel processing to distribute the search task across multiple processors, significantly reducing execution time.
- **Case-Insensitive Search**: Allows searching for strings regardless of character case.
- **Match Location Reporting**: Reports the exact line and character index of each match within the text files, along with surrounding context.
- **CSV Output**: The results are written to a CSV file for easy analysis.
- **Scalable**: Can be extended to handle files in subdirectories and support regular expression searches.

## Project Structure

- `map_reduce.py`: Contains the main MapReduce functions, including the mapper and reducer.
- `grep.py`: Implements the grep algorithm using MapReduce, with options for case-insensitive search.
- `output.csv`: The output file containing the search results with detailed match information.

## How It Works

1. **Data Preparation**: The text files are stored in a folder named `wiki`.
2. **Map Phase**: The files are split into chunks, and the search is performed in parallel across these chunks.
3. **Reduce Phase**: The results from each chunk are combined to produce the final output, which includes all matches and their locations.
4. **CSV Output**: The results are written to a CSV file with columns for the file name, line index, character index, and match context.

## Future Enhancements
1. **Subdirectory Search**: Extend the algorithm to search files in subdirectories.
2. **Regular Expression Support**: Allow users to search using regex patterns.
3. **User-Defined Options**: Enable users to customize search options, such as whole word matching and case sensitivity.
