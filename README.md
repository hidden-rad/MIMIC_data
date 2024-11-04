# MIMIC-CXR / JPG data
## Download the MIMIC data we are targeting

## Step-by-Step Instructions

### 1. Open the Terminal.

### 2. Navigate to the directory where you want to save the file.
	> 	
 		cd /path/to/your/directory

### 3. Prepare a urls.txt file. The urls.txt file should contain the URL for each directory you want to download. For example, the
	>
		https://physionet.org/files/mimic-cxr/2.1.0/files/p17/p17938416/
		https://physionet.org/files/mimic-cxr/2.1.0/files/p17/p17167982/
		...

### 4. Use the wget command to download only the directories in the urls.txt. Use the following command
	> 
  		wget -r -N -c -np --user 'username' --ask-password -i urls.txt

### 5. Command descriptions:
		-r: download recursively.
		-N: Download only files newer than those already downloaded.
		-c: Continue interrupted downloads.
		-np: Do not ascend to the parent directory.
		--user: username (  ).
		--ask-password: Ask for password.
		-i urls.txt: Use the list of URLs in the urls.txt file.

### 6. wget will ask you to enter a password. wget will download the directories listed in urls.txt after you enter the password.

### 7. If you want to download JPG files, change 'mimic-cxr' to 'mimic-cxr-jpg' in step '3.'.
	>
		https://physionet.org/files/mimic-cxr/2.1.0/files/p17/p17938416/
		https://physionet.org/files/mimic-cxr/2.1.0/files/p17/p17167982/
		...
		-------------------------------------------------------------------------------------------------------------------------------------
		https://physionet.org/files/mimic-cxr-jpg/2.1.0/files/p17/p17938416/
		https://physionet.org/files/mimic-cxr-jpg/2.1.0/files/p17/p17167982/
		...
