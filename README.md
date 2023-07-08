# SeeSafe
Submission for hackathon TCNJ-HackDown-2021 category *Best Healthcare Hack*: a proof-of-concept app to aid the visually impaired. This system serves as a virtual seeing-eye dog, taking visual data and determining if it is safe to move forward by checking if there are obstacles in front of the user. 

## Inspiration
I was eager to start learning about machine learning which I don't have a lot of experience with yet, and looking to build a useful healthcare hack, so I decided to develop a system to aid visually impaired people.

## What It Does
The system takes visual data and determines if it is safe to move forward by checking if there are obstacles in front of the user. This would make it easier for people with visual impairments to navigate spaces.

## Description/Walkthrough
### Rectification
- The system takes two images of the same room from slightly different angles. This gives a stereo view of the room (i.e. binocular vision) as opposed to a monocular view, which enables the system to pereive depth
- The images are turned to grayscale and rectified, meaning the system tries to distinguish the common points and differences between the two images
### Boundary Detection
- Using rectification, the system detects the boundaries of the shapes found in the images to identify objects in the visual field
### Depth Map
- Rectification and boundary detection enable the system to make sense of the room in a 3D similar to how our eyes do (though the ssytem does not construct an actual 3D representation of the room)
- It then goes on to calculate the approximate depth of different parts of the image
- By averaging the depth value of the image, it determines if the image appears to *have* depth or *lack* depth, which serves as an indicator of whether it is safe to move forward

## How I Built It
Much of what I learned in this project I found on a blog showing how to use computer vision to detect depth in a visual field, and then built on to concepts to determine if it is safe for the user to continue forward.

## Challenges I Ran Into
Time crunch: being unfamiliar with machine learning and computer vision software, as well as trying to tweak it to suit my needs for this project, within the span of the competition was a challeng.

## Accomplishments
This project serves as a proof of concept that such a system is achievable. I've demonstrated that this could be an interesting direction to take existing computer vision software in a way that could benefit those who have trouble with their vision.

## What I Learned
This project exposed me to the process of setting up a computer vision system using image processing, image rectification, and machine learning.

## What's Next for SeeSafe
I'd like to develop it further so it can work in realtime on a phone, and preferably vibrate or make a sound to let the user know when they encounter an obstacle before they hit it.

## Sources
https://www.andreasjakl.com/easily-create-depth-maps-with-smartphone-ar-part-1/

## Future Work
Accessibility is key to this project, so in the future it would be good to make this algorithm work in realtime, preferably on a smartphone so the user can move around with ease and be alerted via vibration or sound when they are approaching an object they might be too close too. Other computer vision algorithms may also be better suited to this problem. While researching resources for this project I saw one paper which was able to identify objects in the room and create a 3D cuboid representation of the objects. This would be useful as it could help one navigate a room more precisely, rather than simply calculating the average depth of the space in front of the user. Unfortunately, I could not learn enough about how to reconstruct a system like that within the duration of the competition. However, the many blog posts I found on the subject of object detection via rectification and boundary detection were much more beginner friendly, and were able to guide me toward developing the system I wanted to create.

## Result
![image](https://github.com/MMongelli99/SeeSafe/assets/45768887/3cef6bc4-1134-43e5-ae29-723fc710cb2c)
