# Open Source Tools And Scripting Assignment #2

Data for this assignment has been downloaded from [Kaggle](https://www.kaggle.com/). The downloaded data, on [Trending YouTube Video Statistics and
Comments](https://www.kaggle.com/datasets/datasnaek/youtube), includes data gathered from videos on YouTube that are contained
within the trending category each day, from 2008 to 2018.

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

# Question 2

## Overview

This task required creating a Bash script called `analyse` that reads `trending_videos_clean.csv` and performs statistical analysis on the dataset.

The script is executed using:

```bash
./analyse trending_videos_clean.csv
```

## Analysis Performed

The script calculates and displays:

- The most frequent `video_id`
- The mean number of views
- The `video_id` with the maximum dislikes
- The video with the highest engagement rate
- The video with the least net sentiment rate

## Formulas Used

### Engagement Rate

```text
(likes + dislikes) / views
```

### Net Sentiment Rate

```text
(likes - dislikes) / views
```

## Tie Handling

If multiple videos share the same result for a calculation, the script prints all matching videos in a clear format.

## Running the Script

Give execute permission:

```bash
chmod +x analyse
```

Run the script:

```bash
./analyse trending_videos_clean.csv
```