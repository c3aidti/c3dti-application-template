# <repo_name>

Development tag-branch: [<dev/tag-branch/name>](https://github.com/c3aidti/planet/tree/<dev/tag-branch/name>)  
Test tag-branch: [<test/tag-branch/name>](https://github.com/c3aidti/planet/tree/<test/tag-branch/name>)  
Development tag: https://<dev_tag>-<tenant>.<domain>/static/console/  
Test tag: https://<dev-tag>-<tenant>.<domain>/static/console/

## Development Workflow
* The default branch for this repo is `develop`.  
* All development branches should be _created from_ and _merged to_ the desired `tag-branch`.
* A `tag-branch` is a Git branch that is associated with a C3 deployment location (tag).
* Pull requests from development branches **must be used** to merge changes into tag-branches.
* Upon creating (or updating with additional commits) a pull request to a tag-branch, a continuous deployment (CD) workflow will be initiated to provision the application with the proposed changes to that associated C3 tag.

### Procedure for Developers
1. Checkout the current development branch or create on from a the desired tag-branch, and push changes there.
2. Open a pull request comparing a development branch to the desired tag-branch.  This will trigger a workflow to provision your changes to the corresponding tag.
3. Monitor pull request status checks for status of the provisioner.
4. Additional changes to the c3 application pushed to the development branch will trigger a provisioner workflow as long as the pull request remains open.
5. Merge changes to the tag-branch on a regular basis to keep development and tag branches in sync.
