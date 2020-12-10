Demo of using git-crypt to protect secrets in a repo

Steps:
  1. Run `git-crypt init`
  1. Create `.gitattributes` file to specify which files should be auto-encrypted
        ```
        secretfile filter=git-crypt diff=git-crypt
        *.key filter=git-crypt diff=git-crypt
        secretdir/** filter=git-crypt diff=git-crypt
        ```
  1. Add your GPG key: `git-crypt add-gpg-user BB89B185D63A1DD5`
