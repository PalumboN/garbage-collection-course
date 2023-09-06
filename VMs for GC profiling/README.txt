1) Open the file based on your OS and architecture.


2) Open a terminal and run the VM passing an image file

# On MAC

./Pharo.app/Contents/MacOS/Pharo "<IMAGE_FILE>" --interactive

# On Linux

./pharo "<IMAGE_FILE>" --interactive


3) If you want to evaluate some Pharo code without opening the interactive world

<VM_FILE> "<IMAGE_FILE>" eval "<CODE>"

For example:

./pharo "./Pharo 11/Pharo 11.image" eval "1+1"


The result will be printed on the console.