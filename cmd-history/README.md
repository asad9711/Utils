# Problem:
### Was developing for an application, and i had to do to and fro and between writing code and launching containers of the app to test. And everytime, after launching a container, i had to manually type the commands because i couldn't use bash cmd history, since the image got changed(because i was doing code changes in the app regularly), which i didn't find amusing.

# Solution ?
## Use docker volumes

- Created a docker volume
- Used that volume with the images, for the containers of which i wanted to use command history to easily access the long and hard to write commands


## How ?
Created a volume for this purpose
  ` docker volume create for-command-history`

Launched the container using that volume
  `docker run -v for-command-history:/root/.bash_history <image_name>`