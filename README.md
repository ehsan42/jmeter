Load Testing Moodle**

Moodle
1. Create a moodle course
2. Add activities (assigment, forum, quiz) and resource file
3. Create local users and enrol onto course and students
4. Save local users username/password in a .csv file

Jmeter App
Download latest version on Jmeter https://jmeter.apache.org/download_jmeter.cgi

Jmeter Script
1. Open the script in Jmeter app
2. Add values for
    - User Defined variables - BASE_URL_1
    - Student Data - filename
    - Loop Controller - add the moodle id for each HTTP Request
4. Save file
5. Run script through GUI to check for any errors

To run from command line, run the following adjusting the memory, ramp, threads, time and path
JVM_ARGS="-Xms4g -Xmx4g" ./jmeter.sh -Jt=2000 -Jr=2000 -Jd=2400 -n -t moodle-course-browse.jmx

    - JVM_ARGS="-Xms4g -Xmx4g" (how much memory to assign to Jmeter)
    - Jt (number to ramp up)
    - Jr (number of threads)
    - Jd (time duration)
    - t (path to jmeter script) 
    
   
                
