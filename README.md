# Ex-06: Copy Files with Timestamp

# AIM:

To copy all files from a source folder to a destination folder and rename them by appending a timestamp to the file names.

# INPUT:

- Source folder path (e.g., C:\SourceFolder)

- Destination folder path (e.g., C:\DestinationFolder)

# PROCEDURE (UiPath Steps):

1. Assign → Define sourceFolder and destinationFolder.

2. Assign → files = Directory.GetFiles(sourceFolder) → Get all files from the source folder.

3. For Each → Loop through each file in files (TypeArgument: String).

4. Assign → timestamp = DateTime.Now.ToString("yyyyMMdd_HHmmss") → Generate timestamp.

5. Assign → fileName = Path.GetFileNameWithoutExtension(item) → Extract file name.

6. Assign → extension = Path.GetExtension(item) → Extract file extension.

7. Assign → newFilePath = Path.Combine(destinationFolder, fileName & "_" & timestamp & extension) → Build new file path.

8. Copy File → From: item, To: newFilePath → Copy the file with the new name.


# OUTPUT:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8bab9659-bed8-42d6-b6a1-31dc20041641" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ba8b9481-52f2-4565-9194-fcd3ea728bf5" />

# RESULT:
Thus, all files are successfully copied from the source folder to the destination folder and renamed with timestamps.
