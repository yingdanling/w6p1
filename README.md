# Practical 6.1: Animation in Maya
In the first lecture this week we learned about some key principles of animation in 3D environments, and how we can work with them in Maya. In this practical, you’re going to put that learning into action and do some of the things that were shown in the lecture. 

By the end of this practical, you’ll be able to bring objects and even characters to life – making scenes that are dynamic and realistic. In particular you’ll be able to:

- Create an animated piece of scenery
- Rig your first character
- Combine all of these skills to create an animated character!

In this practical, you’ll be using Maya. This is already installed for you on our lab machines. However, if you’d like to continue to work with it on your personal machine, you can get a free educational license here:

https://www.autodesk.com/education/edu-software/overview?sorting=featured&filters=individual

You can find some assets you'll be using during this practical in this template Git repository. The best way to access these is to create a new respository from the template in your account and clone it onto the machine you're working on.

## Task 1: Unlocking the Airlock
In this task we’re going to create our first simple animation: the lock mechanism opening on a sliding airlock door. To get started, open the airlock.fbx model in Maya. You can do this by dragging it into a new scene. Once you’ve opened the model press ‘6’ on your keyboard to see the textured display.

Take a look at the model; you’ll see it’s an airlock that could be included in a space station scene. If you open the outliner (Windows > Outliner) you’ll see there are three main elements of the model:

-	The surrounding walls (airlock_chamber)
-	The doors (door_left, door_right)
-	Some lock bolts that can move independently (bolt_left, bolt_right)

*Tip: in case you’ve not seen the Maya Outliner before, it’s just like the hierarchy view in Unity. You can use it to see all of the elements in your scene and how they relate to each other in terms of parent and child relationships – its really useful!*

In the first task, you should use what you learned in the lecture to animate the lock bolts so that they move outwards over a period of 10 frames. The finished result should look something like this:

https://www.youtube.com/watch?v=oXExEj6YUYE

Some quick tips to help you achieve this task:

-	Consider animating just one of the bolts first – keep it simple
-	You can use ‘S’ to quickly set a key on an object
-	Set the position on the timeline when you want the key to happen before you manipulate the object to the position you want to be in
-	If the timeline is too long, you can change its length by clicking on the little running person in the bottom right of the UI

## Task 2: Opening the Pod Bay Doors
Now the door is unlocked, we need to open it up so players can pass through. In this task, use the same approaches you applied to animate the bolts to animate the doors. The doors should open between frames 10 and 90, and the bolts should move with the doors in the open position. The finished result should look something like this:

https://www.youtube.com/watch?v=zDTr4n1BlmQ

Getting the bolts to move with the doors is the tricky aspect of this task. However, you can achieve this quite easily if you select both the bolt and the door (either in the scene or the outliner) and manipulate and key them together.

You can apply the principles you’ve learned in the last two tasks to animate a whole range of objects in your scenes. Remember, you can key pretty much anything in Maya. Therefore, don’t just limit your animations to translational movement.

# Task 3: Rigging Your First Character
Animating the 3D models that make up the scenery of your 3D environments is crucial for a realistic effect in many cases. However, when we think of 3D animation, its common to want to animate the characters in our scenes too. In the remainder of this practical we’re going to learn how to rig and animate a human character.

To get started, open up the zombie.fbx file from the practical resources folder in a new Maya scene. You should see a 3D model of a Zombie. If you don’t see the textures on the model, press ‘6’. In this task, we’re going to create a skeletal rig that’ll let us animate the complex mesh of this character using some simpler geometry. This rig will also have the kind of human inverse kinematics model we discussed in the lecture applied to it – so some of the hard work of making realistic human movements will be done for us!

Rigging a human character in Maya is actually quite simple – if you just want a basic human that behaves in a fairly standard way. All you need to do is follow these steps using Maya’s “Quick Rig” tool:

1. Select the mesh of the 3D character that you would like to rig (in this case the Zombie)
2. Choose “Skeleton >> Quick Rig” from the menu
3. Make sure that “one click” is selected at the top of the dialog box that appears
4. Press the “auto-rig” button and wait until the rigging process completes

Tip: To find the Skeleton menu you’ll need to choose “Rigging” from the drop down box at the top left of the Maya UI

Once you’ve done this, you should now see that your character has a yellow skeleton in alignment with its main body parts. If you can’t see the skeleton, make sure that “X-Ray Joints” is selected in the “Shading” menu at the top of the scene view.

You should also see some little red circles and squares around some of the main parts of the character’s body (e.g. hands, hips, head, feet). These are called controllers, and we can manipulate the character by moving and rotating these.

Have a go at manipulating these controllers to put the character in some different poses (e.g. bending over, crouching, waving). When doing this you should notice two things that make animating characters a lot easier than it could be:

- The inverse kinematics model moves the skeleton in a way that respects the mechanical constraints of the human body (in most cases!)
- The controllers are hierarchical, meaning that if you, for example, move the hips, the shoulders will move too.

At this point, save a back up of your rigged character. It’ll make it easier to create animations from scratch over the next two tasks.

## Task 4: Animating Your First Idle Character
Now we’ve got a character and we can move it around, the next thing we want to do is apply some animations to it! This can be done in Maya using the same key frame approach we used in the previous tasks, except we apply the key frames now to the controllers (i.e. little red circles and squares).

In this task, you should use this approach to create an “idle animation” for the zombie. An idle animation is basically an animation that pretty much all characters have, which moves them around slightly when they’re doing nothing (i.e. being idle). People don’t ever really stand deadly still, and so applying an idle animation to your characters is essential for making them look lifelike (or whatever is the equivalent for a Zombie!).

To create an idle animation, simply apply some subtle movements to some of the different parts of the body using key frame animation. You might consider:

-	Making the shoulders sway left and right
-	Rotating the head a little
-	Moving the hands a little bit
-	Moving the hips forward and backwards

Don’t overdo these movements, or else you’ll end up with a bad dancing animation! Having said this, an idle animation for a zombie can be a bit more pronounced than for a “living” human, so be creative and see how you can make it look. 3 seconds (~120 frames) might be a good length for an idle animation.

*Tip: you’ll want to make you idle animation a seamless loop. One quick way to achieve this is to put key the character in the same pose at the start and end of your animation. To do this, put the character in a pose and then press S with both 0 and 120 frames selected on the timeline.*

See if you can come up with something more convincing than me – shouldn’t be difficult I’m not very good at animations!

https://www.youtube.com/watch?v=UwpKw-pbeJ4

## Task 5: Your First Walk Cycle
Now we’ve done some basic animation, let’s try and create a type of animation called a walk cycle. A walk cycle animation can be run on a loop when we have a character that is walking around in Unity. 

To create your walk cycle, see if you can animate a character through some of the following positions shown in these diagrams.

![williams_walk](https://user-images.githubusercontent.com/2250660/199253021-aee133ef-c52f-4bd2-8d6d-09d46741d422.png)

Some tips when trying to do this:

-	Don’t try and create a seamless loop this time. Just try and create a single step animation that looks good. Once you’ve got one step, them you can try another.
-	It can help to use one of the side views in Maya when doing this task. Recall, you can switch between views in Maya by pressing the spacebar when your mouse is over the scene view.
-	You can import the image (also in resources) and make in the background of your view to trace over using “View > Image Plane > Import Image”.
-	Animate your character such that they remain in the same position throughout (i.e. they don’t actually walk anywhere). Walking animations that do include character movement (called progressive) are also common to create, but for now let’s keep things simple. 

The walk cycle that’ll come from these diagrams may look quite realistic. Can you see if you can change it to make it look more like a Zombie?

The diagrams in this task are from the Animator’s Survival Kit, which is an excellent reference book should you wish to pursue character animation further. You can get it reasonably cheaply second hand on Amazon (https://www.amazon.co.uk/Animators-Survival-Kit-Richard-Williams/dp/0571238343/).

## Additional Optional Tasks

-	The character we used in this practical was from Adobe Mixamo (https://www.mixamo.com). This is a great resource with loads of characters, and also loads of animations you can download should you wish to not focus on animation in your own practice. Why not take a look around and see what you can find on there?
-	In this practical, we used an existing character model. Why not see if you can model your own and rig it. 

