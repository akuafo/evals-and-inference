Humanloop seems like a really interesting framework and platform.  It blends a few useful features such as a no-code platform for non-technical people to engineer prompts and the ability for technical staff to integrate those into deployment pipelines.  They are ycombinator backed and I heard a podcast with one of the founders and it seems they are getting some traction with significant companies.

My personal interest in Human Loop is whether it's useful for managing, versioning, and evaluating prompts.

Here is what happened when I tried to use it.

I installed the SDK locally in a python project.  In their web dashboard, I created a 'project' with a model config and deployed it, and then ran the python locally.  I kept getting mysterious pydantic errors.  But I was able to run the code and get a response which consisted of an openai chat completion relayed through humanloop so they can track it.  Thus far, the documentation was pretty confusing and the samples weren't structured consistently.  Also they pointed to some really complex examples like a vercel chat app which seems to be a very complicated way to learn how it works.

Next, I tried creating two different model configs with different system prompts:  one in the voice of a pirate and the other as a poet.  I created an 'Experiment' to compare them and modified my code to call that experiment.  That was successful in that it randomized and I got varying chat responses based on the two different system prompts.

Then I went to the humanloop dashboard but could not see anywhere with the results of my experiment.  I can only see the log.  There is a premium feature called 'Evaluations' which may or may not be related and is blocked unless you contact their sales team.

My guess is that they are focused on working with a few big customers and new features and too busy to worry about the self-service model.  And, hmmm, the founders are on twitter and literally just relocated from the UK to SF.  Seems they are earlier stage than I realized but looks like good potential.

Next step:  Try again.
