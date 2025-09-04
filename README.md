
# Warvox

Current master branch is missing a Gem (rkelly) so this is added to the Gemfile during the image build.

[Warvox repo]

The default login for the WarVox web interface is admin/godsexlove ;-) 

## Running Warvox

Pull the old 9.6.0 postgres image

`docker pull postgres:9.6.0` 

Start the image in the background

`docker run -d --name=postgres postgres:9.6.0`

Run the warvox container, linking the progres container and opening up port 7777. 

`docker run -d -p 7777:7777 -ti --link postgres:db sans1241/warvox`

Now connect to http://127.0.0.1:7777

Username: admin

Password: godsexlove

[Warvox repo]: <https://github.com/rapid7/warvox/>
