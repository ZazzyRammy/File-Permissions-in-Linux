<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>File Permissions in Linux</title>
</head>
<body>
  <h1>File Permissions in Linux</h1>

  <h2>Project Description</h2>
  <p>
    In this project, I demonstrated my proficiency in managing file permissions using Linux commands. As a security
    professional responsible for maintaining system security, I examined and adjusted permissions to ensure authorized
    access and prevent unauthorized usage within the file system.
  </p>

  <h2>Check File and Directory Details</h2>
  <p>
    I used the command <code>ls -la /home/researcher2/projects</code> to list the contents and permissions of the
    projects directory. The output displayed the permissions for each file and subdirectory, including hidden files.
    Here is the output:
  </p>
  <pre>
total 32
drwxr-xr-x 3 researcher2 research_team 4096 Aug 17 18:59 .
drwxr-xr-x 3 researcher2 research_team 4096 Aug 17 19:31 ..
-rw--w---- 1 researcher2 research_team   46 Aug 17 18:59 .project_x.txt
drwx--x--- 2 researcher2 research_team 4096 Aug 17 18:59 drafts
-rw-rw-rw- 1 researcher2 research_team   46 Aug 17 18:59 project_k.txt
-rw-r----- 1 researcher2 research_team   46 Aug 17 18:59 project_m.txt
-rw-rw-r-- 1 researcher2 research_team   46 Aug 17 18:59 project_r.txt
-rw-rw-r-- 1 researcher2 research_team   46 Aug 17 18:59 project_t.txt
  </pre>

  <h2>Describe the Permissions String</h2>
  <p>
    The 10-character string in the output represents the file permissions for each entry. In this example, for the file
    project_k.txt, the permissions are rw-rw-rw-. This string is broken down as follows:
  </p>
  <ul>
    <li>The 1st character indicates the file type (d for directory, - for regular file).</li>
    <li>Characters 2-4 represent owner permissions (read, write, and execute).</li>
    <li>Characters 5-7 represent group permissions (read, write, and execute).</li>
    <li>Characters 8-10 represent other permissions (read, write, and execute).</li>
  </ul>

  <h2>Change File Permissions</h2>
  <p>
    To modify file permissions and remove write access for the group and others on the file project_k.txt, I used the
    following command:
  </p>
  <pre><code>chmod go-w /home/researcher2/projects/project_k</code></pre>

  <h2>Change File Permissions on a Hidden File</h2>
  <p>
    To ensure that the hidden file .project_x.txt is not writable by group and others, I utilized the following
    command:
  </p>
  <pre><code>chmod go-w /home/researcher2/projects/.project_x.txt</code></pre>

  <h2>Change Directory Permissions</h2>
  <p>
    To restrict access to the drafts directory to only the owner (researcher2), I used the following command:
  </p>
  <pre><code>chmod go-rwx /home/researcher2/projects/drafts</code></pre>

  <h2>Summary</h2>
  <p>
    In summary, I successfully managed file permissions to align with proper authorization requirements. I examined
    permissions using <code>ls -la</code>, modified permissions using <code>chmod</code>, and ensured that sensitive
    files and directories were secure while allowing appropriate access to authorized users. This experience strengthens
    my ability to maintain the security of systems and data.
  </p>
</body>
</html>
