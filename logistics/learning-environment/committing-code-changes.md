# 📤 Committing Code Changes

### Objectives

* [ ] Understand the need for a Version Control System.
* [ ] Explain the difference between committing to the `main` branch and a separate branch.
* [ ] Be able to commit any changes to your Github account **through** CodeSandbox.

## Instructions

From time to time, you might have certain changes in your code you would want 'saved' in a safe storage space or repository. This allows for retrieval in the future, as well as version-controlling.

Version Control is a way of managing code changes across time, and using a Version Control System (VCS) like Git enables a developer to avoid a problem like this:

![Can you already feel the pain? (Source: Technofy)](<../../.gitbook/assets/image (13).png>)

> "Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later.&#x20;
>
> You can read more about Git [here](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control).

### Saving your changes on CodeSandbox

* [ ] After you've made changes to your files, remember to save them onto your sandbox. In the backend, CodeSandbox remembers the saved changes, and tracks these changes.

![An unsaved/changed file will have a circle icon denoting its state - Ctrl + S (Windows) / Cmd + S (Mac) to save your changes!](<../../.gitbook/assets/image (10) (1).png>)

* [ ] You can see these changes being reflected on the `Changes` accordion under the GitHub tab.
* [ ] Fill in the Summary and a short description of the changes that you would like to commit. Remember to encapsulate what the commit entails - is it to fix certain bugs, build certain features, or code commenting.

![After documenting the details of the changes, commit the changes to a new branch and start a Pull Request](<../../.gitbook/assets/image (9) (1).png>)

* [ ] In order to commit a snapshot of the saved files (in this case, `script.js` and `index.html)`, there are two ways to achieve this:\
  \
  1\. **Committing directly to the main branch** - this overrides the state of your original file directory. Since you are the owner of your own repository, you do have the right to merge any commits that you, or anyone interfacing with your repository, into the `main` branch. Do this if you are certain that your changes are final and your code is non-breaking!
* [ ] For your **day-to-day code changes and edits**, you may commit directly to the main branch.\
  \
  2\. **Creating a branch (with a random hash) and initiating a Pull Request (PR)** - in a typical software development workflow, developers make changes on development branches and get their code approved via a PR, or a **Pull Request**. This ensures that code is peer-reviewed and tested before merging with `main` - typically the production branch.\
  \
  When starting your **project submissions**, we would want students to create a new branch so that our SLs can review and feedback on the code before you merge your code into `main`. We will touch on code review later. We will be detailing the steps to achieve (2) below:

![Opening the PR will direct you to the commit's GitHub page, where you can document feedback and discussions on code](<../../.gitbook/assets/image (14) (1).png>)

{% hint style="info" %}
There is no need to fret about understanding in detail what branching is. The MCU multiversal timeline is a good starting analogy.\
\
The sacred timeline in the MCU ([Earth-199999](https://marvel.fandom.com/wiki/Earth-199999)) is what we call the `main`timeline. Every other branch or divergence from this `main` timeline is a basic branch (also a duplicate) of the main timeline, but with some additional changes. They operate in isolation, and conflicts only emerge when conflicting characters converge in the same place (as seen in Loki), and developers settling code conflicts might want to 'prune' these variances.
{% endhint %}

### Code Review

* [ ] Once a PR is made, you can open up the PR on GitHub, which the code is stored on, and review any changes or feedback. At this juncture, you might want to submit this link to your SL on Slack and request a review.&#x20;

{% content-ref url="submitting-your-work.md" %}
[submitting-your-work.md](submitting-your-work.md)
{% endcontent-ref %}

* [ ] Code Review is a back-and-forth process of `Commit` > `Feedback` > `Review`. After your SL completes the feedback, you can make code changes again in CodeSandbox, and repeat the cycle until there are no bugs or incomplete code.

![A typical code review process on GitHub](<../../.gitbook/assets/image (11) (1).png>)

* [ ] Once you are satisfied with the commits, you can then merge the Pull Request into `main` (remember what we mentioned previously about merging with `main!`)

![Include clear intent of what the merge request is for](<../../.gitbook/assets/image (15) (1).png>)

* [ ] After you have confirmed the merger, you can then safely delete the branch that was created for your code changes.

![Once merged, you can safely delete that branch](<../../.gitbook/assets/image (8).png>)

* [ ] That's it! The whole development to production workflow is as simple as that. To recap:\
  \
  1\. As a developer, you **develop features / fix bugs** within the codebase (could be yours or a company/team)\
  \
  2\. Remember to **save your files** at regular time intervals\
  \
  3\. At meaningful junctures, you would want to **make a code commit** into the codebase/repository. This provides a snapshot in term (or versioning) so that you or your teammates can reference it in the future.\
  \
  4\. Your code commits would likely **be subjected to review** by a senior developer or by the repository owner (in the case of [contributions to Open Source projects](https://opensource.guide/how-to-contribute/))\

* [ ] 5\. Code review process takes place! It is an **iterative process** of `Commit` > `Feedback` > `Review` until a satisfactory state is achieved (typically complete with code testing)\
  \
  6\. Changes are **merged into production**, and in this case the `main` branch. The branch timeline can now be removed.\
  \
  7\. Rinse and repeat!
