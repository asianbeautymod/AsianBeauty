#**Using the GitHub Web Application**

##How to change a file

1. Navigate to the [**repository**](https://github.com/asianbeautymod/AsianBeauty) in your browser. [Here’s what the page you’ll land on should look like.](http://imgur.com/a/m3JXa)

2. From here, click on the file you want to edit. Let’s say, for example, I want to add something to the sidebar - I would click on sidebar.md. For those who haven’t seen it before, the **.md extension** just means **markdown**, the same formatting style you use on Reddit. Clicking sidebar.md leads you to [a page that looks like this.](http://imgur.com/a/YMtGS)

3. Click the pencil icon in the upper right corner of the file. [It will look like this.](http://imgur.com/a/VZOHS)

4. Make your edits. You can preview your changes here if you’d like, but keep in mind that Reddit markdown is slightly different than regular markdown - for example,
"##New? Start Here!"
works on Reddit, but not in regular markdown. Maybe test out your markdown choices in Reddit.

5. When you’re finished editing, go down to the box below the file editor. You need to type in a concise message telling everyone what change(s) you made in the top bar. If you have a long message to type, make the top bar your “title” and the larger box your “long-form description”. Once you’re done, it’ll look [something like this.](http://imgur.com/a/oYXpD)
*You’ll notice that there are two radio buttons, and that one just says you can’t commit to master. This is because master is set up to disallow direct changes in order to protect it. Master should be what is currently on the sub. Any other branches are irrelevant until they’re merged into master via a pull request.*
You can name your branch if you’d like - just keep in mind that it can’t have any spaces in it. If it’s easier, just leave it at the default like above.

6. Click the “Commit changes” button. This will create a **branch** containing your changes to the file, but it will not create a **pull request** until you explicitly do so. You will land on [this page.](http://imgur.com/a/rYs1v) From here, you can either create a pull request or go back to your branch and keep going. I’m going to assume you want to change more than one file per pull request, but if you want to just put out the pull request for your branch, move down to step 10.

7. Let’s change another file - say, the subreddit title. Navigate back to the **repository** main page by clicking the AsianBeauty link at the top of the page. Then click on the Branches tab, and click on the name of the branch you’ve just created. Now click on subredditTitle.md and make your edits as before. I’m going to change our subreddit title to Omloop is Queen, because I can.

8. See what I’m doing here? I’m a troll who wants Laura Omloop back. If **master** wasn’t protected, our source of truth would become Omloop is Queen. While that may or may not be true, that’s not what the sub is about. [See how the changes look here.](http://imgur.com/a/e3voV)

9. Now, go to make your **commit** as before, but this time, instead of creating a new branch, you’re going to click the “Commit directly to the <your-branch-name> branch” **radio button**. Go ahead and click “Commit changes”.

10. Let’s make a pull request! Navigate back to the main repository page again. You’ll see a new bar has appeared asking you to compare and make a pull request using the branch you’ve created, [shown here.](http://imgur.com/a/BGZZn)

11. Click the green “Compare & pull request” button. Once here, you could just press the “Create pull request” button and you’d be done. You may want to add **reviewers** for your pull request first, though, to make your life easier. If you click on the “Reviewers” button in the page shown below, you can click whoever you want to be on your review and they’ll get a notification saying they’ve been asked to review your pull request. Once you’ve done that, you can add whatever description and title you like, click “Create pull request”, and [you’re done!](http://imgur.com/a/NdBSb)

**Also note that you can see exactly which changes you made to which files, line by line, to make sure that you’re not missing or adding anything you don’t want to have there before you open the pull request.**

##GitHubTerms:

Pull request

Master

Commit

Repository

Branch

Reviewers

Markdown
