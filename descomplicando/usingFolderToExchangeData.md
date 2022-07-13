md myData
touch foo
echo 'foobarbaz' > foo
cat foo
docker container run -ti --mount type=bind,src=/Users/GK47LX/source/dockertodo/descomplicando/myData,dst=/myData alpine 
cat bar
vi bar
docker container run -ti --mount type=bind,src=/Users/GK47LX/source/dockertodo/descomplicando/myData,dst=/myData alpine 
cd ..
