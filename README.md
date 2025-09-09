Map S3 Bucket as a Drive (Windows)

📌 Objective
Mount an AWS S3 bucket as a drive on Windows using rclone.

🛠️ Steps
1. Create S3 Bucket
Logged into AWS Console.
Created a new S3 bucket.

2. Install rclone (Windows)
Downloaded rclone for Windows from rclone.org

Verified installation:
rclone version

3. Configure rclone
rclone config
n → New remote
Name: mys3
Storage: s3

Provider: AWS
Entered AWS Access Key, Secret Key, and Region.
Left endpoint blank (default).
Accepted defaults for all other options.
Saved config.

4. Test Connection
rclone ls mys3:
✅ No error → connection successful.
Shows files if bucket has objects, nothing if empty.

5. Mount S3 as Drive
rclone mount mys3: X: --vfs-cache-mode full
mys3: → name of configured remote.
X: → appears as a drive in File Explorer.
Files copied into X: sync directly with the S3 bucket.

📸 Screenshots
rclone config setup.
Successful connection test.
File Explorer showing X: drive (S3 mounted).

🎯 Conclusion
Successfully mapped an AWS S3 bucket as a Windows drive using rclone.
Files in X: drive are stored directly in S3.
