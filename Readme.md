Update your sed command by specifying a backup suffix or no backup with '' like this:

sh
Copy code
sed -i '' 's/eticket-fe.\*/eticket-fe:20/g' ./k8s/deployment.yaml
The empty '' after -i tells macOS's sed not to create a backup file.

Explanation:
-i '': This option tells sed to perform in-place editing without creating a backup file (specific to macOS sed).
The rest of the command remains the same.
Updated Jenkins Pipeline Step:
sh
Copy code

- sed -i '' 's/eticket-fe.\*/eticket-fe:20/g' ./k8s/deployment.yaml
  This should resolve the issue and allow the pipeline to run successfully.
