# Match-names-and-faces
A program that makes users match names and faces.

The program is intended for teachers training to remember what their pupils are called.

At the core there is a metric for every student - the faceFactor.

Every student starts with a faceFactor of 0.5. As the teacher uses the progrm, this metric will change. 
-A succesful recognition will increase the faceFactor
-A miss will reduce the faceFactor.

A low faceFactor will thus imply that the teacher is having troiuble recognizing this particular student.

Students will a low faceFactor will be more likely to appear in the teacher training session.

Initla training ideas:

-Show 6 images and one name. Click the correct image.
-Show one image and 6 names. Click the correct name.

Initial algorithm for updating faceFactor:
Direct miss (you have the name, but miss the correct image or you have the image, but guess the incorrect name)
-faceFactor -= 0.1;
Indirect miss (The owner of image or name you clikced)
-faceFactor -= 0.05;
Hit (the user has chosen correctly)
--faceFactor += 1.0;

Initial algorithm for picking images:
-use faceFactor, number of rounds since last appearnce (or last hit/miss), some randomly generated number. 
Update the queue as faceFactors update.

I can easily write this program in Flash, but I'd like to try different technologies. I'd like to start with JavaFX.
A flash version (Animate CC with ActionScript 3.0) will be available by late august.

