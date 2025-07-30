2025-07-09 15:37

##### Description:
Creating and running a python file in terminal

### Terminal:
`mkdir countdown`
`cd countdown`
`nano __main__.py`
inside the GUI of note
	`import time`
	
	for i in range(5,0,-1):
		print(i)
		time.sleep(1)
	print("Time's Up!")
	
Ctrl+O > enter > Ctrl + X to save and exit (or to write and exit)
`cd ..` This will put you back on the directory before you enter in the countdown directory
`python -m countdown`
Remember to input the name `__main__.py` correctly because python will try to find that specific file name to run
#### Note
This is just a baby example on how to use the python module to run in terminal, this however, can lead to creating a file inside the infected host to run and give them something they don't want

## Next Application(s)
[[Third Application]]