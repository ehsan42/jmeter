Load Testing Moodle

Prerequisite

Moodle

1. create a moodle course
2. Add a assigment, forum, quiz, downloadable file
3. create local users and enrol onto course
4. save local users username/password in a .csv file

Jmeter App
Download latest version on Jmeter https://jmeter.apache.org/download_jmeter.cgi

Jmeter Script
1. Open script in Jmeter
2. Add values in
    - User Defined variables
    - Student Data
3. Edit id values in Loop CONtroller for each HTTP Request
4. Save file
5. Run script through GUI to check for any errors
6. run the following command to run through the command line with your customised parameters
    - JVM_ARGS="-Xms4g -Xmx4g" (how much memory to assign to Jmeter)
    - Jt (number to ramp up)
    - Jr (number of threads)
    - Jd (time duration)
    - t (path to jmeter script) 
    
    JVM_ARGS="-Xms4g -Xmx4g" ./jmeter.sh -Jt=2000 -Jr=2000 -Jd=2400 -n -t moodle-course-browse.jmx
                
