# Boxin_API


BOXIN API DOCUMENTATION

URL:   http://18.218.40.173:8080/bgip/*

Upload API:

Rest EndPoint:   */drive/upload

method: POST

Sample Request:

{
  "userName":"muthahar",
  "folderName":"folder123",
  "parentFolderId":"0",
  "link":"folder_link",
  "bucketPublicId":"optional",
   "fileList": [
        {
            "fileName": "file_1",
            "bucketPublicId": "s3bucketId1",
       
            "size": 3,
            "link": "Download Link for file"
		 },
        {
            "fileName": "file2",
            "bucketPublicId": "s3bucketId2",
         
            "size": 4,
             "link": "Download Link for file"
        }
    		]
}







Sample Response:

{
    "type": "folderRequest",
    "created": "2017-10-24T16:19:00",
    "id": "59ef1ab177c86fb23d53d86f",
    "userName": "muthahar",
    "favourite": false,
    "folderName": "folder123",
    "link": "folder_link",
    "parentFolderId": "0",
    "fileList": [
        {
            "created": "2017-10-24T16:19:00",
            "id": "59ef1ab177c86fb23d53d870",
            "userName": "muthahar",
            "bucketPublicId": "s3bucketId1",
            "favourite": false,
            "fileName": "file_1",
            "folderId": "59ef1ab177c86fb23d53d86f",
            "link": "Download Link for file",
            "size": 3
        },
        {
            "created": "2017-10-24T16:19:00",
            "id": "59ef1ab177c86fb23d53d871",
            "userName": "muthahar",
            "bucketPublicId": "s3bucketId2",
            "favourite": false,
            "fileName": "file2",
            "folderId": "59ef1ab177c86fb23d53d86f",
            "link": "Download Link for file",
            "size": 4
        }
    ]
}


Get Folder Info:
Rest End Point:   */drive/folder/59ef1ab177c86fb23d53d86f
method: GET
Sample Response:
{
    "type": "folderResponse",
    "created": "2017-10-24T10:49:00",
    "id": "59ef1ab177c86fb23d53d86f",
    "userName": "muthahar",
    "favourite": false,
    "folderName": "folder123",
    "link": "folder_link",
    "parentFolderId": "0",
    "fileList": [
        {
            "created": "2017-10-24T10:49:00",
            "id": "59ef1ab177c86fb23d53d870",
            "userName": "muthahar",
            "bucketPublicId": "s3bucketId1",
            "favourite": false,
            "fileName": "file_1",
            "folderId": "59ef1ab177c86fb23d53d86f",
            "link": "Download Link for file",
            "size": 3
        },
        {
            "created": "2017-10-24T10:49:00",
            "id": "59ef1ab177c86fb23d53d871",
            "userName": "muthahar",
            "bucketPublicId": "s3bucketId2",
            "favourite": false,
            "fileName": "file2",
            "folderId": "59ef1ab177c86fb23d53d86f",
            "link": "Download Link for file",
            "size": 4
        }
    ]
    "folderList": []
}

Home Drive API
Rest End Point:   */drive
method: GET
Sample Response:
{
    "type": "folderResponse",
    "userName": "muthahar",
    "favourite": false,
    "parentFolderId": "0",
    "fileList": [
        {
            "created": "2017-10-20T09:20:00",
            "id": "59e9bfcc77c807c918844066",
            "userName": "muthahar",
            "favourite": false,
            "fileName": "file1",
            "folderId": "0",
            "size": 3
        }
    ],
    "folderList": [
        {
            "created": "2017-10-20T08:55:00",
            "id": "59e9ba1d77c87156ae235e51",
            "userName": "muthahar",
            "favourite": false,
            "folderName": "sampleFolder1",
            "link": "folder download link",
            "parentFolderId": "0"
        }
               
    ]
}






Create New Folder/ Empty Folder

Rest Endpoint:   */drive/newFolder
method: GET
Sample Request:

{
  "userName":"muthahar",
  "folderName":"Sample Folder",
  "link":"folder_link",
  "bucketPublicId":"optional"
  
}



Sample Response:

{
    "type": "folderBean",
    "created": "2017-10-24T14:31:00",
    "id": "59ef4ed5e4b019db028813ec",
    "userName": "muthahar",
    "bucketPublicId": "optional",
    "favourite": false,
    "jy": "Sample Folder",
    "link": "folder_link",
    "parentFolderId": "0"
}









