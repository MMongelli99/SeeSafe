# SeeSafe
The system takes visual data and determines if it is safe to move forward by determining if there are obstacles in front of the user. This would make it easier for the visually impaired to navigate, using their phone for instance, instead of needing other aid devices like a seeing eye dog or a cane to navigate unfamiliar spaces.

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
  The system takes two images of the same room from slightly different angles. This gives a stereo view of the room (similar to our eyes) as opposed to a monocular view.
