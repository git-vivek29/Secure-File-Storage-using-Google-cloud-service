# Secure File Storage using Google cloud service

### In this project, the file is encrypted with AES encryption algorithm and uploaded to Google drive using Google cloud service such as drive API. The encrypted file is now safe on cloud storage, the file can be viewed only after the decryption which ensures security and prevents from the access of third party. User can download the encrypted file from cloud storage (Google Drive) and can decrypt it using cipher key.
### Architecture Diagram

![Architecture Diagram](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/ArchitectureDiagram.jpg "Architecture Diagram")

### Workflow of the system
#### First step is to set up the system i.e create Google Drive API and download the .json file. User must sign-in to the gmail account and perform the following steps:
#### Step 1: Go to APIs Console and make your own project. Here the name of project is Cloud Computing
![Create Project](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/1.CreateProject.PNG "Create Project")

#### Step 2: Search for ‘Google Drive API’, select the entry, and click ‘Enable’.
![Enabling Google Drive API](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/2.EnableGoogleDriveAPI.PNG "Enabling Google Drive API")

#### Step 3: Select ‘OAuth consent screen’ from the left menu, create user type as internal and enter the application name and save it.
![OAuth consent screen](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/3.OAuthConsentScreen.PNG "OAuth consent screen")

#### Step 4: Select ‘Credentials’ from the left menu, click ‘Create Credentials’, select ‘OAuth client ID’.
![Create Credentials](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/4.CreateCredentials.PNG "Create Credentials")

#### Step 5: Now, the product name and consent screen need to be set -> click ‘Configure consent screen’ and follow the instructions. Once finished:
1. Select ‘Application type’ to be a Web application.
2. Enter an appropriate name.
3. Input http://localhost:8080 for ‘Authorized JavaScript origins’.
4. Input http://localhost:8080/ for ‘Authorized redirect URIs’.
5. Click ‘Save’.

![Configure consent screen](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/5.ConfigureConsentScreen.PNG "Configure consent screen")

#### Step 6: Click ‘Download JSON’ on the right side of Client ID to download client_secret_<really long ID>.json.
![Download JSON file](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/6.Download_JSON_File.PNG "Download JSON file")
#### The downloaded file has all authentication information of your application. Rename the file to “client_secrets.json” and place it in your working directory.
![Rename and save JSON file](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/7.RenameJSON.PNG "Rename and save JSON file")

#### This completes the creation  and setting up of Google Drive API. Now run the script.py file in the command prompt.
1. Here when the code is executed for the first time it asks the user to create and confirm a password which will be used to enter the system every time and also for the decryption process.

![SettingUpPassword](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/8.SettingUpPassword.PNG "SettingUpPassword")

2. After this the system will reload. Again run the script.py python file which will then ask the password to enter.

![InitializingSystem](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/9.InitializingSystem.PNG "InitializingSystem")

3. The system provides four options.

![HomeScreen](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/10.HomeScreen.PNG "HomeScreen")

4. To encrypt the file press 1 and enter the filename you want to encrypt. Here the filename is  ‘my_profile.jpg’. After encrypting it replaces the original ‘my_profile.jpg’ with ‘my_profile.jpg.enc’ where .enc file is the encrypted file.

![Encryption](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/11.Encryption.PNG "Encryption")

![EncryptedFile](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/12.EncryptedFile.PNG "EncryptedFile")

5. To upload the file press 3 and enter the encrypted filename i.e ‘my_profile.jpg.enc’. It authenticates the user through Google Drive API and if the authentication flow is completed the file will be uploaded to the user’s Google Drive.

![UploadToGoogleDrive](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/13.UploadToGoogleDrive.PNG "UploadToGoogleDrive")

![Authentication](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/14.Authentication.PNG "Authentication")

![GoogleDrive](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/15.GoogleDrive.PNG "GoogleDrive")

6. To decrypt the file download the encrypted file and store it to the working directory and press 2 to decrypt it. The system will replace the encrypted file i.e ‘my_profile.jpg.enc’ with the original file  ‘my_profile.jpg’.

![Decryption](https://github.com/git-vivek29/Secure-File-Storage-using-Google-cloud-service/blob/main/Snapshots/16.Decryption.PNG "Decryption")

#### The proposed system can encrypt and upload any type of files such as text documents, images, multimedia files, JSONs, XMLs, spreadsheets, etc.

