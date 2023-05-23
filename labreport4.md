# Lab Report 4

## Logging into `ieng6`:

I ran the commands `<up><enter>` to go up 1 in the search history because the `ssh cs15lsp23id@ieng6.ucsd.edu` was 1 up in my history. I used this command to log into my `ieng6` account. It took me around 5 seconds to complete this step. Below is a picture of the sommand being run.

![Image](CSE15L_LAB4_1.png)

## Cloning the fork:

I ran the commands `<g><i><t><space><c><l><o><n><e><space><copy><paste><enter>` to copy and paste the link from my fork which was `https://github.com/mk7652/lab7` which made the command `git clone git@github.com:mk7652/lab7.git` so that I could clone my fork of the repository into my `ieng6` server. The timer is at around 10 seconds now. Below is a picture of the command being run.

![Image](CSE15L_LAB4_2.1.png)

## Running the Tester:

I used `<c><d><space><l><a><b><7><enter>` which was the command `cd lab7` to change the current directory to `lab7`. Then I ran `<bash><space><t><tab><enter>` to run the test. I used `<tab>` to auto fill the rest of the file name so the command looked like this: `bash test.sh`. The test said two tests ran one faliure. The timer is now at 54 seconds. Below is a picture of the tester being run.

![Image](CSE15L_LAB4_3.1.png)

## Editing the Code in VIM:

I used the command `<v><i><m><space><shift + l><tab><.><tab><enter><x><i><2><esc><:><w><q>` which allowed me to use vim to edit ListExamples.java by typing in `vim ListExamples.java` (again I used tab to auto fill). Then, when I entered vim, my cursor was already on the `1` of `index1` so I typed `x` to delete it. Then, I went into insert mode by typing `i` and then I typed `2` and to change `index` to `index2` then `esc` to leave insert mode. then I typed `:wq` to save my changes and return to commit mode. The timer is now at 1:35.

![Image](CSE15L_LAB4_4.png)

## Retesting the Code:

I then ran the tests again by using`<up><up><enter>` to go two up in my history where `bash test.sh` was. The two tests now pass. The timer is now at 1:45. Below is a picture of the tests being re-run.

![Image](CSE_LAB4_5.png)

## Commiting and Pushing:

Then, I ran the command `<g><i><t><space><a><d><d><space><.><enter>` which is `git add .` in the terminal. This added the changes from the current directory (referenced by `.`) which I made so that they can be commited. Then, I ran `<g><i><t><space><c><o><m><tab><enter>`, which was the command `git commit` in the terminal, which entered me into vim mode to commit my changes. This mode displays all of the details about the changes youa re going to commit. In this mode, I ran the commands `<i><h><i><esc><:><w><q>` which let me add a commit message by entering insert mode then save the file and exit vim using `:wq`. My commit message was `hi`. Then, I ran `<g><i><t><space><p><u><s><h><space><ctrl + c><ctrl + v><enter>` which looks like `git push git@github.com:mk7652/lab7.git` in the terminal. This command pushes my changes into my `lab7` repository. It is crucial to provide your own `ssh` link when you push or the push command will not work because it needs a destination to push to. You can find your own ssh url for a lab 7 by clicking on `lab7` in your repositories then click on `code` then click on the tab that says `ssh` and copy that link then paste it rigth after `git push`. Then, if you look in your `lab7` repository you will notice that `ListExamples.java` is updated with your changes. Pictures displaying the use of the `git commit` and `git push` commands are displayed below.  

![Image](CSE15L_LAB4_6.1.png)

![Image](CSE15L_LAB4_6.png)
