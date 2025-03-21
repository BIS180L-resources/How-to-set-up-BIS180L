# How-to-set-up-BIS180L

## ~ Four weeks before class

### Apply for or renew JetStream Allocation

Can only apply for renewal 30 days before expiration

Julin will apply for renewal on ~ Feb 21, 2025

### Update Jetstream image

Optional.  Can use last years if desired.  Instructions are [here](https://github.com/BIS180L-resources/BIS180L-VM_Image_Setup)

TODO: make sure that manila shares are mounted on default image
Create instructor image that has write access to Manila shares.

### Create a Manila share and get it mounted on the image

Manila shares are used to share data with all Jetstream instances in the class.  

Since I plan to renew the Jetstream allocation we should just be able to use the Manila shares from last year, rather than setting up new ones.

### Set up a [GitHub Classroom](https://classroom.github.com/classrooms)

GitHub Classroom is used to manage student assignments and repos

### Website

The website is hosted by [GitHub Pages](https://pages.github.com/)

There is a [repo for the website](https://github.com/jnmaloof/BIS180L_web)

#### Orientation

The website is built using [Jekyll](https://jekyllrb.com/).  Info on hosting Jekyll pages on github is [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll)

I recommend having Jekyll running on your local machine so that you can preview changes before pushing

Important info on the website is in the [website repo README](https://github.com/jnmaloof/BIS180L_web/blob/gh-pages/README.md)

#### Beginning of year website prep
1. Create a new branch [yyyy]_archive, where yyyy represents the previous year _Julin last completed 1/31/2025_
2. Pull that branch to the archive site fork (or ask Julin to) _Julin last completed 1/31/2025_
3. Move all lab posts from `_posts` to `_drafts` 
4. Update the welcome posts if needed
5. Update dates in `course_scheudle.md`
6. Block comment out the table in `Assignments.md`,then you can move the start of that as you go
7. __DELETE THE LINKS__ in `Assignments.md`.  You will need new ones, corresponding to your classroom for this year.

### Canvas

I am only using Canvas for the gradebook and to make announcements

### Slack

I set up two Slack channels each your for the course under the UCD Slack umbrella.  One for announcements and one for student questions.

## ~ Several days to one week before classes start

Create instances for each student.

Go to the [Jetstream exosphere web page](https://jetstream2.exosphere.app/)

Click on the `UC Davis BIS180L Genome Biology` allocation

Click on `Create` and select `Instance`

Click on `By Image`

Enter `180L` in the search bar

Choose `BIS180L-build-2025-image`

Choose `Create Image`

Fill out the form:
1. If you are creating multiple instances, click `Random Name` (we will rename them later).
2. Select "m3.quad"
3. Choose `Custom disk size` and select 1000 GB
4. How Many instances: I'd do 10-15 at a time and repeat until you have as many as you need (once each set is running)
5. Enable web desktop: **YES**

After instances are running, click on each instance, rename it with student first name and last initial.  Copy the IP address (or ssh logon info) and passphrase and send to the student through the Canvas messaging portal.

Note: it may be more efficient to do the renaming via the [Horizon interface](https://docs.jetstream-cloud.org/ui/horizon/intro/) or even via [the command line](https://docs.jetstream-cloud.org/ui/cli/overview/)

## For each assignment

If you update a question, remember to update the template

## knitting

__IF you update a .md that has a corresponding .Rmd UPDATE THE .RMD ALSO__ Otherwise it will get cloberred the next time someone knits the .Rmd

To knit .Rmd files for rendering on the website you MUST use the ` jekyll_knit_BIS180L.R` script.  See info in the [website repo README](https://github.com/jnmaloof/BIS180L_web/blob/gh-pages/README.md)

## Grading

### Installations

1. You need a [git CLI](https://github.com/cli/cli#installation) installed on your computer.
2. Install the [classrooom extension](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/using-github-classroom-with-github-cli#using-the-github-classroom-extension-with-github-cli)
```
gh auth login
gh extension install github/gh-classroom
```

### To grade an assignment
1. For each assignment go to [Github Classroom](https://classroom.github.com/classrooms)
2. Click on the Assignment you want to grade
3. Click on Download
4. If you follow the marking scheme below, then you can use the [grade tallying script](https://github.com/BIS180L-resources/BIS180L_GradingAssignments/blob/master/Grade_Compiler.R).

`**JM** -2 Need to use colors in your plot`

Make sure your marks have blank lines above and below

### instances

can re-size boot drive in Horizon interface

## To-dos

Update reading assignments to use second edition of R for data Science

