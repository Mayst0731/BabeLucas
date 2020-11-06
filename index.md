# Spider Lucas

## Create classes and modules for scraping

### Requirement
- Scraping categories
  + Input is 1 base url
  + Output1: All the category information(name,url,base_url)
  + Output2: All the category urls that may contain corresponding entry link for each category(category_urls)
- Scraping courses
  + Input is a url list(category_urls) from the above Output2.
  + Output1: All the course information(name,url,category,category_url)
  + Output2: All the course urls that may contain corresponding entry link for each course(course_urls)
- Scraping course details
  + Input is a url list(course_urls) from the above Output2.
  + Output1: All the course details(name,url,category,category_url,others)
  + Output2: All the course urls that may contain corresponding entry link for each faculties(faculty_urls)
  
    **1. Problem here is that course detail sometimes cannot collect from only one page.**
    
    **2. Some course details are from category page.**
    
    **3. Some course details needs to get to other pages correspondingly from other pages.**
    
    **4. Some of faculty details sould be get in this level, so it's better not to get faculty info for twice.**
  
- Scraping course faculties
  + Input is a url list(faculty_urls) from the above Output2.
  + Output: All the faculty details(name,title,company,others)
  
### Class method
- Send requests and parse web pages
- Manage scraping rules
- Output the next level urls
- Output current level information 
- Write current level information into json file


