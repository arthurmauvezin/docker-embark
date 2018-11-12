# Docker embark

This bash script build and push many images from Dockerfile implementing specified tags.
After building and pushing, the script delete pushed images.

## Usage
To use this script, you need to add to commented lines to your Dockerfile as following
```dockerfile
# REPOSITORIES=repository-first,my-personal-repo
# TAGS=1,1.2,1.2.0,1.2.0-alpine
```

Then, execute the following line
```bash
docker-embark [PATH_TO_DOCKERFILE]...
```

This will build and push then delete 8 images named:
* repository-first:1
* repository-first:1.2
* repository-first:1.2.0
* repository-first:1.2.0-alpine
* my-personal-repo:1
* my-personal-repo:1.2
* my-personal-repo:1.2.0
* my-personal-repo:1.2.0-alpine

## Installation
On Linux environment execute install.sh script.
```
git clone https://github.com/arthurmauvezin/docker-embark.git
cd docker-embark 
chmod +x install.sh
./install.sh
```

## Example
Type:
```bash
docker-embark .
docker-embark path/to/dockerfile
```

