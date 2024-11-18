# How to get Task1 input data from the MIMIC database

- The MIMIC licensing procedure is described in https://github.com/hidden-rad/Task1. 

## Task 1. File description<br/>
- Task1_test_dcm.txt: MIMIC data list for downloading 'dicom image (x-ray)' and 'medical report' used in Task1_test.
- Task1_test_jpg.txt: MIMIC data list for downloading 'jpg image (x-ray)' and 'medical report' used in Task1_test.
- Task1_train_dcm.txt: MIMIC data list for downloading 'dicom image (x-ray)' and 'medical report' used in Task1_train.
- Task1_train_jpg.txt: MIMIC data list for downloading 'jpg image (x-ray)' and 'medical report' used in Task1_train.

# Instructions

1. Prepare a MIMIC licensed account.

2. Download a Task1_\*_\*.txt file depending on the extension of the image you want to use a txt file in "Task 1. File description".

3. Open a terminal, then set the path to save the data.
	>
		 cd /path/to/your/directory

4. Use the wget code to download the MIMIC data, where ${\textsf{\color{magenta}'username'}}$ is your account (ID) on Physionet, and ${\textsf{\color{magenta}'Task1_test_dcm.txt'}}$ is a file downloaded in step 2, for example. For other files in task 1, repeat the file name in the above "Task 1. File description".

	>
		wget -r -N -c -np --user 'username' --ask-password -i Task1.txt
	
	> 
	
		Command descriptions:
		-r: download recursively.
		-N: Download only files newer than those already downloaded.
		-c: Continue interrupted downloads.
		-np: Do not ascend to the parent directory.
		--user: Physionet username (  ).
		--ask-password: Ask for password.
		-i Task1.txt: List of Task1 target data file.

5. If you entered the code in step 4 correctly, you will be prompted to enter your password. Enter your Physionet password and the download will proceed, which may take a while depending on your connection.

