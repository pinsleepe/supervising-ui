# Supervising UI

This project has a web interface to label training data for machine learning task.
As of now it can allow you to easily label images with one or many labels


# Requires

1. flask
2. sqlite3

Install them using pip

# Quick Start

## Step1 : You need to feed training records

`find $HOME -name '*.jpg' > workdir/input.txt `

## Step 2: Create a settings file that contains labels

#### Example :

```
{
  "type": "image-labeling",
  "task": {
	"labels":[
		"class1",
		"class2",
		"class3",
		"class4"
	 ]
  }
}
```
place this file in a directory with name 'settings.json'
Example : `workdir/settings.json`

## Step 3: Start server

#### Usage

`python app.py -h`

```
usage: app.py [-h] [-i INPUT] -w WORK_DIR [-p PORT]

Web UI for Labeling images

optional arguments:
  -h, --help            show this help message and exit
  -i INPUT, --input INPUT
                        Path to to input file which has list of paths, one per
                        line. (Optional)
  -w WORK_DIR, --work-dir WORK_DIR
                        Work Directory. (Required)
  -p PORT, --port PORT  Bind port. (Optional
```

#### Example

`python app.py -i workdir/input.txt -w workdir -p 8080`

python app.py -i /media/monika/Transcend/katai_home/python_projects/graphs/input.txt -w /media/monika/Transcend/katai_home/python_projects/graphs/ -p 8080

Visit http://localhost:8080 on web browser


## Screenshots 
![Image](../master/screenshots/labeling-images.png?raw=true)



