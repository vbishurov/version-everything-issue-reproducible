# Issue - Corrupting files on error

The updates.xml file is **not** the first file to be updated in the files array. The updates.xml file **has a comment as the first element before the root element**.

- This causes an error when running version-everything
- And it causes the manifest.json to be completely emptied out

# Steps to reproduce

0. Check manifest.json is not empty
1. Run npm i
2. Run npm version patch
3. See manifest.json is empty
