## 1. Introduction  

In this course, we're going to learn how to extract the information from images and video. 
- position of a camera
- trajectory of the camera
- distances to the points in the scene. 

## 2. Overview 

### 2.1 Week-1
In the first week of this course, 
- we are going to study the geometry of perspective projection. 
    - how a camera is posed with respect to the environment 
    - how far are the objects. 
    
    
you can see two vanishing points,the intersections of parallel lines. 

And the line connecting the two vanishing points called the horizon tells you already whether you are tilted with respect to the ground floor or not. 


It gives you also some very good idea about where is the camera, where is that projection center from which all these points are seen, and from which the race to these points are going. 

### 2.2 Week-2 

- exploit this information in order to do some visual effects. 
    - put this Penn Engineering logo on this video, 
    - even if the camera is moving and 
    - with out having any information about the camera or about the dimensions of the soccer field. 
    
> the power of projected geometry. 

Just with very simple ideas,like the vanishing points. 
Like the correspondence of points in the scene, you can pretty much change your environment without having really metric information, like any information about distances. 

whether a goal was really behind the goal line or not. 
- with 2 picture 
- with projective geometry terms,
- with vanishing points, and 
- with projector formations, 
we're going to find whether the ball indeed was behind the goal line or in front. 

### 2.3 Week-3, 4

where am I? : how we reason about how we are in the three-dimensional scene by two-dimensional picture itself. 

So there are two methods to achieve this goal. 

#### A. 방법 1 

The first group of method, assume we know something about the 3D environment. 

For example, in this scene where we're standing in the street corner, we can recognize this road on the scene,and we can recognize this road for our own view as we move in the space. 

Once we can recognize this road in the scene, the road itself and the lane mark on the road itself, allow me to find vanishing points of the road in the image as shown here.
 
Once I have a vanishing point in the image, draw a line between the vanishing point to the optical center, that ray extended to the three-dimensional space is in fact parallel to the road in the three-dimensional space. 

As such,we have a way to orient ourself with respect to this road in the vanishing point direction, where we call z.
 
And the road surface might not be seen everywhere, but often times, we live in a man made structured world,where we have parallel lines on the ground planes, which we can recognize across multiple views. 

So long as we have those,we can identify our orientation with respect to each other,respect to this point in infinity. 

One point infinity allow me to estimate two degree of freedoms in rotation, and to estimate an entire three-dimensional rotational matrix, we can use two vanishing points. 

And this is a required finding in the three-dimensional world, two perpendicular direction in the three-dimensional space. 

And for those two directions, we found vanishing points in the images associated with them. 

Now we will have, again, as two vanishing points in an image, an optical center. 

We draw a ray from the optical center to vanishing point 1, optical center to vanishing point 2 in the image, and that two ray extend into 3D space are also perpendicular to each other. 

And in fact, align with those three-dimensional vanishing points in 3D. 

As such,we can orientate ourself fully in 3D. 

And quite often in man made environments,we have those perpendicular lines. 

For example, a building here,we have seen vanishing points in two different directions,one one facade, one on another facade. 

If you don't have vanishing points, we can still estimate our orientation with respect to a known object in the world. 

For example, if I have a planar surface on the ground and as soon as we can recognize four points on this planar object,we can navigate ourselves with respect to that four points, meaning that we know the orientation of the camera in 3D, as well as the position relative to each other. 

If you don't have the planar objects,in more general case, you might have a three-dimensional object that you know the shape of. 

And if you have known shape of three-dimensional objects, I can again, infer the position of my camera from the two-dimensional image alone by looking at the 3D to 2D correspondence. 

#### B. 방법 2 

The second method for computing camera **orientation** and camera **position** require no known objects in the three-dimensional scenes. 

All we need to do is taking **multiple picture** of the scene from different angles. 

So, illustrated here, two friends taking picture of the same building across the street from different view points, and if they were to share the picture between them, we can compute the relative three-dimensional rotation and translation between the two views. 

And the key idea here is that if Bobcan see Alice in his picture and vice versa,if they can see each other in each view, then we have some idea wherethey are relative to each other. 
In practice, this might not be done,okay \[COUGH\] sorry. 
In practice, when we took a pictureof the same object in the scene, we're going to be positioned in suchway that we can see each other. 
But still, we can invert this position, pretending the camera is large enough socalled peepholes. 
And that peephole is in fact the secondcamera person in the first person view. 
And this is done requiring us finding correspondence of at least eight points in the scenea cross two different views. 
And we do not need to know the three-dimensional shape, just simply a two-dimensional correspondense fora few selected points in the scene. 
Once we have those, we can computethe relative camera rotation and translation, in this case between Bob and Alice. 
As we have more images come into the play, we can estimate the entire three-dimensional scene structure, as well as the camera position forall the viewers. 
Not just from two views, Bob andAlice, but for multiple viewers. 
And this is done through a techniquecalled bundle adjustments. 
And this technique allow me to tweak the position of the three-dimensional points, as well as the camera position of all the viewers in the scene together in a nonlinear least square function. 
And this results a complete estimation of where am I across all the views, as well as a back product and structure in the scene, as illustrated here. 
This course provides you a set of tools that you can use for computing three-dimensional position of the camera as well. 
But this is not really a fun thing, unless you take your own cameras out of pockets and go out and take some pictures in your environment,in your cities, in your schools. 
And you can apply the technique we use directly on your own pictures. 
From that, you can really figure outhow you are relative to your friends, relative to yourself. 
And you can, in fact, compute 3Dstructures of your own schools and your buildings. 
So I hope you enjoy, and go out and take many pictures.