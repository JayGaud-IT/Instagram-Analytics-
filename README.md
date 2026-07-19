Instagram Analytics SQL Project 

Project Overview:

This project focuses on analyzing Instagram data using SQL to evaluate user behavior, post performance, and engagement trends. By building a structured relational database covering users, posts, engagement metrics, and traffic sources, meaningful insights were extracted to support data-driven decision-making for digital marketing and content strategies.

Various SQL techniques:including data retrieval, filtering, aggregation, advanced joins, subqueries, and window functions—were applied to identify high-performing content, platform growth channels, and active user segments.

Relational Database Schema & E-R Structure
The system architecture consists of 4 core tables mapped via structured relationships:

1. users Table
Stores primary account demographic and popularity records.

user_id (INT, Primary Key): Unique identifier for each user.

username (VARCHAR): Profile handle.

country (VARCHAR): Geographic location.

account_type (VARCHAR): Category of account (e.g., Business, Creator).

followers (INT): Total follower count.

created_at (DATE): Account registration date.

2. posts Table
Tracks content properties and upload metadata.

post_id (INT, Primary Key): Unique identifier for each post.

user_id (INT, Foreign Key): Maps back to the authoring user.

upload_date (DATE): Date of publication.

media_type (VARCHAR): Format type (e.g., Image, Reel, Video).

caption_length (INT): Character count of the post description.

hashtags_count (INT): Number of tags utilized.

content_category (VARCHAR): Genre of content (e.g., Tech, Education, Food).

3. engagement Table
Monitors raw interaction volumes and calculated retention rates.

engagement_id (INT, Primary Key): Unique identifier for the transaction record.

post_id (INT, Foreign Key): Maps to the specific piece of content.

likes / comments / shares / saves (INT): Interaction counts.

reach / impressions (INT): Visibility and discovery numbers.

engagement_rate (DECIMAL): Calculated percentage of user interactions relative to visibility.

4. traffic Table
Measures growth attribution metrics.

traffic_id (INT, Primary Key): Unique identifier for the traffic sequence.

post_id (INT, Foreign Key): Target post attracting visitors.

traffic_source (VARCHAR): Referral mechanism (e.g., Explore page, Hashtags, Profile Visits).

followers_gained (INT): Number of net new followers attributed to that traffic line.
