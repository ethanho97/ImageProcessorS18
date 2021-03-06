# Image Processor Final Project (Spring 2018)

**Final Project DUE:** Wednesday, May 02, 2018 05:00PM EST 

## Overview
The final project in this class will require our team to leverage the
industry-standard skills learned over this semester to design and
implement a software system to upload an image to a
web-server, perform image-processing tasks on the web-server, and then display
/ download your processed image. 

This final project was  open-ended to allow our group to tailor this to
their areas of interest.

The following proper professional software
development and design conventions taught in this class were used in the 
creation of the web-app:
* git feature-branch workflow
* continuous integration
* unit testing
* PEP8
* docstrings / Sphinx documentation

## Functional Specifications
### Front End
* Provides a front-end that will allow a user to select an image that will be 
  uploaded to the web-server,
  perform necessary preprocessing steps (convert image to base64 string), and 
  then issue a RESTful API request
  to your cloud service for further processing.
* Front-end has a choice of processing steps to perform on each
  uploaded image, including:
  + Histogram Equalization [default] (Pre- Processing: Grayscale Conversion)
  + Contrast Stretching
  + Log Compression
  + Reverse Video
  + Edge Detection (Pre- Processing: Grayscale Conversion)
* Front-end contains a text field for user to write their email to access their saved images
* Front-end has a gallery of all final processed images store for the user
* A table to provide usefull metadata for the user:
  + Upload Time
  + User Email
  + Process Requested
  + Image Size
  + Process Duration
  + Grayscale Conversion (Required in Histogram Equalization and Edge Detection)
* Front-end also provides:
  + A viewer window to compare the original and processed images.
  + A viewer window to compare the original and processed image histograms.
  + A button to download the image in the following format:
    - JPEG

### Back End
* A cloud-based web service that exposes a well-crafted RESTful API that will
  implement the image processing methods specified above.
  + Post-Request: Upload an image and determine what image processing function
  to run. As well as to handle user data allocation. 
  + Get-Request: Return a jason file with all metadata along with images (processed and original).
* A database is implemented to do the following:
  + Store previous user actions / metrics (metadata sepcified above). 
  + Store uploaded images and timestamps for a user
  + Store processed images (along with what processing was applied) and timestamps for a user

## Deliverables
- [x] A [README.md](README.md) describing the final performance and state of your
  project.
- [x] Recorded video demo of image processor in action:
  + demo.mp4
  + [Link in Youtube](https://www.youtube.com/watch?v=RqZUF4yWXjU)
- [x] All project code (in the form of a tagged GitHub repository named
  [ImageProcessorS18](https://github.com/martinli8/ImageProcessorS18/tree/master))
- [x] Link to deployed web service
  + [Link](http://imageprocessor.surge.sh/)
- [x] Final RFC link and PDF
  + [File](Engineering-RFC-TeamOne.pdf)

## Install App
* Installation instructions
  + Clone the repository
  `git clone https://github.com/martinli8/image_processor.git`
  + Move into repository folder (image_processor)
  `cd image_processor`
  + Move into React App folder (image_processor_viewer)
  `cd image_processor_viewer`
  + Install app dependencies 
  `npm install`
  + Run app
  `npm start`

## LICENSE
MIT License

Copyright (c) 2018 Davidrbr95, martinli8, ethanho97

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


## Grading

* RFC Document
* Git Repository
  + Issues/Milestones
  + Commits are discrete, logical changesets
  + Feature-branch workflow
* Software best practices
  + Modularity of software code
  + Handling and raising exceptions
  + Language convention and style (PEP8)
  + Sphinx documentation for all modules/functions
* Testing and CI
  + Unit test coverage of all functions (except Flask handler)
  + Travis CI passing build
* Cloud-based Web Service
  + RESTful API Design 
  + Validation Logic 
  + Returning proper error codes
  + Robust deployment on virtual machine 
  + Image processing functionality
* Proper use of a Database 
* Client software functionality
* Demo of the final working project
* Robust README