# Retrieve Indonesian Election 2024 Data

## 1. Introduction
This project gathers data result of Indonesia President and Vice President Election from the official website, and save it to the database (only support SQLite now).

DISCLAIMER:  
This project retrieves public (not confidential) data which can be checked at https://pemilu2024.kpu.go.id by everyone, with the purpose for educational only.

## 2. How to Run:
### 2.1. Using Docker
#### Steps:
1. Pull docker image from the repository.  
`docker pull minghermawan/pemilu-ppwp-2024`
2. Create a new folder for SQLite database and files output.  
3. Run docker with command format like below.  
`docker run -v (Output Folder):/home/out --env DB=(NO/sqlite) --env DB_FILENAME=(SQLite database filename) --env DEBUG=(YES/NO) --env SAVE_JSON_FILES=(YES/NO) --env SAVE_IMAGE_FILES=(YES/NO)`  
#### Example:
`docker run -v $PWD/out:/home/out --env DB=sqlite --env DB_FILENAME=ppwp2024.db --env DEBUG=YES --env SAVE_JSON_FILES=YES --env SAVE_IMAGE_FILES=YES minghermawan/pemilu-ppwp-2024`  
#### Explanation:
`-v` is to map between your output folder with output folder inside Docker.  
Example; if your new output folder path is /home/test/out at step 2, write `-v /home/test/out:/home/out`.  
`--env` is environment variable.  
#### Environment Variables:
- DB  
Set value is NO if you don't want to write output to the database.  
Set value is sqlite if you want to write output to SQLite database. (Only support SQLite database right now)  
If you set the value is sqlite, database file will be saved in the DB folder inside output folder.  
- DB_FILENAME (optional, effect only when you set the DB value is sqlite)  
Set SQLite database filename.  # Retrieve Indonesian Election 2024 Data

## 1. Introduction
This project gathers data result of Indonesia President and Vice President Election from the official website, and save it to the database (only support SQLite now).

DISCLAIMER:  
This project retrieves public (not confidential) data which can be checked at https://pemilu2024.kpu.go.id by everyone, with the purpose for educational only.

## 2. How to Run:
### 2.1. Using Docker
#### Steps:
1. Pull docker image from the repository.  
`docker pull minghermawan/pemilu-ppwp-2024`
2. Create a new folder for SQLite database and files output.  
3. Run docker with command format like below.  
`docker run -v (Output Folder):/home/out --env DB=(NO/sqlite) --env DB_FILENAME=(SQLite database filename) --env DEBUG=(YES/NO) --env SAVE_JSON_FILES=(YES/NO) --env SAVE_IMAGE_FILES=(YES/NO)`  
#### Example:
`docker run -v $PWD/out:/home/out --env DB=sqlite --env DB_FILENAME=ppwp2024.db --env DEBUG=YES --env SAVE_JSON_FILES=YES --env SAVE_IMAGE_FILES=YES minghermawan/pemilu-ppwp-2024`  
#### Explanation:
`-v` is to map between your output folder with output folder inside Docker.  
Example; if your new output folder path is /home/test/out at step 2, write `-v /home/test/out:/home/out`.  
`--env` is environment variable.  
#### Environment Variables:
- DB  
Set value is NO if you don't want to write output to the database.  
Set value is sqlite if you want to write output to SQLite database. (Only support SQLite database right now)  
If you set the value is sqlite, database file will be saved in the DB folder inside output folder.  
- DB_FILENAME (optional, effect only when you set the DB value is sqlite)  
Set SQLite database filename.  
- DEBUG  
When the value is YES, debug files will be created in the log folder inside output folder.  
- SAVE_JSON_FILES  
Set value is YES if you want to write output to JSON files. JSON files will be created in the json folder inside output folder.  
- SAVE_IMAGE_FILES  
Set value is YES if you want to save images files. Image files will be created in the image folder inside output folder.  
### 2.1. Using Python
#### Requirements:
1. Python (this project tested with Python 3.11.11)
2. Python Library:
   - aiohttp
   - aiofiles
   - python-dotenv
#### Run:
`python main.py --save-json-files=(YES/NO) --save-image-files=(YES/NO) --db=(NO/sqlite) --debug=$DEBUG --db-filename=(SQLite database filename);`
#### Parameters:
- `--save-json-files`  
Set value is YES if you want to write output to JSON files. JSON files will be created in the json folder inside output folder.  
- `--save-image-files`  
Set value is YES if you want to save images files. Image files will be created in the image folder inside output folder.  
- `--db`  
Set value is NO if you don't want to write output to the database.  
Set value is sqlite if you want to write output to SQLite database. (Only support SQLite database right now)  
If you set the value is sqlite, database file will be saved in the DB folder inside output folder.  
- `--debug`  
When the value is YES, debug files will be created in the log folder inside output folder.  
- `--db-filename--`  
Set SQLite database filename.  

- DEBUG  
When the value is YES, debug files will be created in the log folder inside output folder.  
- SAVE_JSON_FILES  
Set value is YES if you want to write output to JSON files. JSON files will be created in the json folder inside output folder.  
- SAVE_IMAGE_FILES  
Set value is YES if you want to save images files. Image files will be created in the image folder inside output folder.  
### 2.1. Using Python
#### Requirements:
1. Python (this project tested with Python 3.11.11)
2. Python Library:
-- aiohttp
-- aiofiles
-- python-dotenv
#### Run:
`python main.py --save-json-files=(YES/NO) --save-image-files=(YES/NO) --db=(NO/sqlite) --debug=$DEBUG --db-filename=(SQLite database filename);`
#### Parameters:
- `--save-json-files`  
Set value is YES if you want to write output to JSON files. JSON files will be created in the json folder inside output folder.  
- `--save-image-files`  
Set value is YES if you want to save images files. Image files will be created in the image folder inside output folder.  
- `--db`  
Set value is NO if you don't want to write output to the database.  
Set value is sqlite if you want to write output to SQLite database. (Only support SQLite database right now)  
If you set the value is sqlite, database file will be saved in the DB folder inside output folder.  
- `--debug`  
When the value is YES, debug files will be created in the log folder inside output folder.  
- `--db-filename--`  
Set SQLite database filename.  
