# Open Source Tools And Scripting Assignment #2

# Question 1

## Overview

This task required creating a Bash script called `clean` that reads `trending_videos_unclean.csv`, performs error checking and data cleaning and outputs a cleaned CSV file named:

```bash
trending_videos_clean.csv
```

The script is executed using:

```bash
./clean trending_videos_unclean.csv
```

## Error Checks

The script checks for:

- Missing input file
- File not found
- Invalid file type
- Empty file
- Incorrect number of header columns

## Data Cleaning

The script performs the following cleaning operations:

- Removes the `ratings_disabled` column
- Removes rows with empty fields
- Removes duplicate rows
- Removes rows without a `video_id`
- Removes rows with zero likes or dislikes
- Removes the time portion from `publish_date`

## Running the Script

Give execute permission:

```bash
chmod +x clean
```

Run the script:

```bash
./clean trending_videos_unclean.csv
```