We will see how Upload File process for selenium works here:
Here I am analysing upload.py

## Line 01: 
driver.get('http://the-internet.herokuapp.com/upload')
#### Explanation: 
Will get yhe file upload url

## Line 02: 
driver.find_element_by_id('file-upload').send_keys(file)
#### Explanation: 
file object is created by folllowing process- 
filename = 'some-file.txt'  || file = os.path.join(os.getcwd(), filename)
So, now i am sending this file object through send_keys method 

## Line 03: 
driver.find_element_by_id('file-submit').click()
#### Explanation: 
clicking the file_submit button

## Line 04: 
uploaded_file = driver.find_element_by_id('uploaded-files').text || assert uploaded_file == filename, "uploaded file should be %s" % filename
#### Explanation: 
Making Assertion
