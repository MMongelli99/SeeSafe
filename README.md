# SeeSafe
Winner for the category *Best Healthcare Hack*: developed as a proof of concept to aid the visually impaired, as an alternative to a seeing eye dog or cane, this system takes visual data and determines if it is safe to move forward by determining if there are obstacles in front of the user. This project is a submission to TCNJ-HackDown-2021.

## Inspiration
I was eager to start learning about machine learning which I don't have a lot of experience with yet, and looking to build a useful healthcare hack, so I decided to develop a system to aid visually impaired people.

## What it does
The system takes visual data and determines if it is safe to move forward by determining if there are obstacles in front of the user. This would make it easier for the visually impaired to navigate, using their phone for instance, instead of needing other aid devices like a seeing eye dog or a cane to navigate unfamiliar spaces.

## How we built it
I learned a lot from a blog I found showing how to use computer vision to detect depth in a scene, and then added to those concepts to determine if it is safe for the user to continue on their path.

## Challenges we ran into
Time crunch, being unfamiliar with machine learning and computer vision software, and trying to tweak the system to suit my needs were all challenges I faced working on this project.

## Accomplishments that we're proud of
It's mainly a proof of concept, this would be implemented for live video from a mobile app if it were to be put to real world use, but here I demonstrate that it may be an interesting direction to take existing computer vision software.

## What we learned
I learned a bit about computer vision, image processing, image rectification, etc.

## What's next for SeeSafe
I'd like to develop it further so it can work in realtime on a phone, and preferably vibrate to let the user know if it s safe to walk forward so they can use it to navigate unfamiliar rooms.

## Walkthrough
### Rectification
- The system takes two images of the same room from slightly different angles. This gives a stereo view of the room (similar to our eyes) as opposed to a monocular view
- They are turned to grayscale and "rectified", meaning the computer tries to find common points between the two images
### Boundary Detection
- Detect the boundaries of the shapes found in the images to identify objects in the area
### Depth Map
- Using rectification to and boundary detection so the system can make sense of the room in a 3D sense, it then goes on to calculate the approximate depth of different parts of the image
- By averaging the depth value of the image, we can determine if the image appears to have depth or lack depth, indicating whether it is safe to walk forward or not

## Sources
https://www.andreasjakl.com/easily-create-depth-maps-with-smartphone-ar-part-1/

## Future Work
Accessibility is key to this project so in the future it would be good to make this algorithm work in realtime and preferably on a smartphone so the user can move around with ease, and the phone would vibrate when they are approaching an object they could collide with. Other computer vision algorithms may also be better suited to this problem. While researching resources for this project I saw one paper which was actually able to identify objects in the room and create a 3D cuboid representation of them. This would be helpful as it could probably be able to help one navigate a room more precisely, rather than simply calculating the average depth of the space in front of the user. However, the paper I found was rather dense for someone not familiar with computer vision, whereas the blogs I used to develop this project were much more beginner friendly.
