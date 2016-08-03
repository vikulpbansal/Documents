---
title: View-based Adaptive Streaming
layout: post
excerpt_separator: <!--more-->
---
Vikulp Bansal
============
**3rd Year Undergraduate Student**

**Department of Electrical Engineering**

**Indian Institute of Technology Kanpur**

*Email: [vikulp@iitk.ac.in](mailto:vikulp@iitk.ac.in)Homepage: [Click here](http://home.iitk.ac.in/~vikulp)*

<!--more-->
<hr>

# Cube map rendering and view based adaptive streaming of 360 degree video:

### Mentors:
  * Professor [Yao Wang](http://engineering.nyu.edu/people/yao-wang), Department of Electrical & Computer Engineering, New York University
  * Professor [Gaurav Sharma](http://www.grvsharma.com/research.html), Department of Computer Science & Engineering, IIT Kanpur

### Project Description:
##### Introduction:
Generally, 360 video files use equirectangular projection for rendering and processing. This equirectangular layout includes redundancy of information. The project aims at using cube-map representation instead of equirectangular projection for rendering (reducing redundancy significantly) and using Dynamic Adaptive Streaming over HTTP (DASH) for developing streaming techniques.
##### Rendering: 
Used Facebook API to convert equirectangular layout video into cube-map layout. Facebook has provided open source transform filter code for this conversion using ffmpeg. 3D JavaScript library three.js and OpenGL is used to implement browser based rendering of 360 videos. Various texture mapping algorithms including UV mapping are implemented to render video texture into cube map geometry and then morph it into a sphere using vertex normalization techniques.
##### DASH content generation: 
The original video files are encoded into H.264 format using x264. Video segments of different resolutions and MPD (Media Presentation Description) are generated using MP4Box.
##### View Based Adaptive Streaming: 
The segments generated from 360 video file are delivered to client for adaptive streaming. To implement view-based streaming of 360 videos, the horizontal plane was quantized into 12 bins (each bin corresponding to 30 degrees) and the vertical plane was quantized into 6 bins (each bin corresponding to 30 degrees) giving a total of 72 view ports. Segment corresponding to a view port is streamed using DASH, meeting with the demands of the user. This view based streaming shows user a particular view at a particular point of time and not the entire video. This method of streaming is efficient because it uses lesser bandwidth and changes quality of video according to bandwidth available for user.

##### Project Report:

[Click here](http://home.iitk.ac.in/~vikulp/RTEReport.pdf)

##### RTE Day Presentation: 

[Click here](http://home.iitk.ac.in/~vikulp/RTEPresentation.pdf)

##### Software/Libraries used:

Facebook transform filter, ffmpeg, DASH Encoder, Three.js, OpenGL, x264, MP4Box

##### Languages Used:

C, Javascript

##### Version Control System:

Git

### Skills:
  * 360 degree video Rendering
  * 360 degree video Streaming

# Logging dashboard using ELK stack:

### Mentor:

Professor [Manindra Agrawal](http://cse.iitk.ac.in/users/manindra/), Department of Computer Science & Engineering, IIT Kanpur

### Description of Tasks:

  * Implemented elasticsearch, logstash and kibana stack using gelf logging driver to forward logs from various servers. Used Docker containers to run services on local machines. Logs can be vsualized in kibana dashboard.
  * Deployed elk stack on kubernetes. Setup of nodes and pods for container clusters is done using service and replication controller files. Implemented them using kubectl command line interface. 

### Skills:
  * Kubectl command line interface for kubernetes
  * Data management using elasticsearch, kibana and logstash
