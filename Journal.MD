i need to actually do the proper formatting at some point

6/13/2025

4 Hours

I began this project by searching for excuses to make an overly complicated combat robot. Combat robotics is my main hobby, but I have never ventured far outside of the meta out of fear of wasting time and money on an unsucessful bot. Hack Club's Highway program rewards projects that are extra complex with a higher budget and more points in the program. I saw this as the perfect opportunity to make a more complicated robot design. My previous experience in combat robotics comes from my 15lb robot, Dino, which I have placed 2nd and 3rd with at NRL Nationals over the last 2 years. Dino uses an eggbeater style weapon, which is very common and relatively simple. For this project I am going to use a more complicated weapon system, and maybe even a custom PCB, to make my project more complicated to warrant the higher budget and more points in Highway. This is something I have always wanted to do as well, as these more mechanically complex robots are always very fascinating, but Highway gave me the perfect justification to pull the trigger on it.

My first idea was to make a hammersaw, which uses a spinning weapon on an arm to attack the tops of other robots. However, the hammersaw has been very popular over the last year or two, especially in insectweights. This has led to the systems/parts needed to run a hammersaw being relatively well documented. I opted not to build a hammersaw as the well documented and convergant nature of hammersaw electronics/mechanics may cause me to not get the full points for Highway, which I would need to fund the build.

This led me to think about the most complicated robot designs I could think of, to make sure I could earn the full points and budget from Highway. My mind instantly went to ring spinners, which are typically very complicated due to the difficulty of constraining and powering such a thin blade. The advantage of this, however, is that you can build a robot where the blade sticks far enough out from your robot where you are able to reach your opponent while they have nowhere to target on your robot. I've always loved the idea of having a ring spinner, but I never quite fell in love with the idea of designing one, mostly due to the mechanical complexity. However, since I need complexity for this project, this is perfect as I am more comfortable adding mechanical complexity than electrical complexity.

![](https://github.com/KyleDavis2200/Ring-Spinner/blob/main/Images/image_2025-06-13_215821910.png)
An example of a ring spinner robot.

The first thing I did was design a rough blade concept. Some aspects of this design, such as the blade thickness, were based off of other antweight robots, such as the scalar kit. The amount of support everywhere around the blade was approximated by eyeballing it. I may attempt to use FEA in the future, but generally eyeballing works well enough in combat robotics(its also very difficult to approximate combat robotics collisions with FEA), especially after being in the community long enough to "calibrate" your eyeballing. This concept allowed me to check the mass of the blade, which I could then use to make sure that it would be possible to fit the robot in the weight limit. At 159 grams, the blade was very heavy, but its reach meant that I could get away with budgeting less weight for armor, giving me confidence that it would be possible to fit it within the weight limit.

![](https://github.com/KyleDavis2200/Ring-Spinner/blob/main/Images/image_2025-06-13_205627015.png)
The first blade design.

This design also allowed me to get a rough interior diameter of six inches, which I can then use to begin laying out the rest of the robot's design. Ideally, I would decrease this diameter, but I first had to make sure I could fit my electronics in it. The next step is to find the bearings I am going to use. This will allow me to get an idea of how much space I have for the electronics, as everything else can move more freely than the bearings. My initial plan was to have bearings above and below the blade, which would have constrained it axially. I did not consider that this would provide no radial constrainment, leading to the need for even more bearings. This system would have needed at least 9 bearings, and at 4g per bearing this would not be optimal with already being tight on weight from the large weapon. Instead, I am going to opt to use flanged ball bearings, where I can get away with using only 6 or less bearings at a relatively similar weight to the ball bearings above. This approach has its own flaw however. The flange on the bearings is so small that it may not provide enough axial constrainment by itself. To supplement them, I am going to use washers between the flange and the weapon ring. Since the washer goes all the way around the bearing, it has much more surface area constraining it, and the higher diameter of the washer allows it to provide more surface area for the weapon. At this point I realized I am likely going to greatly exceed the speed ratings on these bearings, which is normal for combat robots as they are only used for very short periods of time, however not to this extent as I may exceed 100k rpm on these bearings. There's not really anything I can do about that though so it is what it is.

![](https://github.com/KyleDavis2200/Ring-Spinner/blob/main/Images/bearingsketch.png)
Current sketch of the internals of the robot.

The next step was to choose my drive system. To keep everything on the robot simple I am going to use a tangent drive system. This eliminates the need for gearboxes or gear reduction as the motor output shaft uses friction to drive the wheels. Repeat Robotics sells motors designed specifically for this usage in this weight class, so I will use those. I plan on coupling this with Lego wheels, as that seems to be a very standard pairing. However, if the diameter of these wheels ends up being significantly larger than the height of the rest of the robot, I may opt for smaller custom wheels instead. At this point I also modeled in a 4S 300mah LiPo battery and a Repeat 2822 weapon motor that would friction drive the ring through a TPU interface.

![](https://github.com/KyleDavis2200/Ring-Spinner/blob/main/Images/image_2025-06-13_223846387.png)
Current design progress.

Clearly, I had way too much room on the inside at this point, so I chose to shrink it until I knew I could just barely squeeze the wiring in. This was important as the weight was approaching 324 grams, leaving approximately 120 grams left for the entire frame, receiver, wheels, receiver, and ESCs, but by shrinking the space I gave myself on the inside, I can shrink the weapon too, saving more weight.

![](https://github.com/KyleDavis2200/Ring-Spinner/blob/main/Images/image_2025-06-13_224013040.png)
Current weight.

By shrinking the internal ring diameter down to 5.25", I was able to knock a significant amount of weight out of the weapon, and this would also reduce the amount of weight spent in the remainder of the frame as the frame too would now be smaller. 

![](https://github.com/KyleDavis2200/Ring-Spinner/blob/main/Images/image_2025-06-13_225553273.png)
Current internal layout.

I plan to proceed with this layout tomorrow as I model the frame, however I expect to encounter weight issues very shortly into my design process. My plan to save weight from there is to remove the rear bearing and reposition the remaining four bearings in a more square shape, allowing the battery to move further back and get rotated to fill up the created space. This would then allow me to shrink the robot more. This would save plenty of weight between the reduction in frame size, weapon size, and bearing count. I initially wanted to have five bearings as it would allow me to have three bearings supporting against the axial forces of upwards impacts and two against the axial forces of downwards(or, more likely, upwards impacts while inverted) impacts, however two of each would likely be plenty.

6/14/2025

3 Hours

Well, after thinking about it some more, I realized I should just got to the four bearing setup. This would save some weight and allow me to compact the robot more, which is always ideal. I would like to use extra weight for armor or for a fork on the back of the robot(unconventional for a ring spinner but counters the counter to the weapon). I also realized that the Repeat 2822 weapon motor that I planned on using would have been too big, sticking out past the top plate, and would have caused the robot to not be invertible. Instead, I replaced it with two 2205 drone motors, which should provide more than enough power. A single one of these motors could probably spin up the weapon, just barely, but due to the size of the weapon more motor is ideal. 

![](https://github.com/KyleDavis2200/Ring-Spinner/blob/main/Images/image_2025-06-14_181452156.png)
This was the setup that I arrived at.

I still felt like there was a bit more space to be squeezed out. One of the flaws with this setup is I needed to find space for belts to power the front wheels, and I didn't leave much space for this. My next step was to look into using tracks instead of wheels, as these would allow me to save more internal space as I can use two small pulleys for each the front and back of the tracks, creating a more rectangular profile, saving space on the inside of the robot.

![](https://github.com/KyleDavis2200/Ring-Spinner/blob/main/Images/image_2025-06-14_190412500.png)

This layout, with the space gained from the treads, was much more comfortable. Each track weighed approximately 6.5 grams, which seemed bearable. Next, I made a sketch of the side of the robot, which would guide my extrusion thicknesses in the next step.

![](https://github.com/KyleDavis2200/Ring-Spinner/blob/main/Images/image_2025-06-14_202731101.png)
Oops! All weapon (: !
