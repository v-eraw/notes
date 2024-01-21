# Software Engineering @Google

1. Write test
2. Run test (frequently)
3. React to failure (quickly)

If part of the code is too difficult to test, it could be because there's too many responsibilities or difficult-to-manage dependencies.

Continuous Integration (CI) - DevOps best practice where code check ins are automatically built/tested before being deployed. Requires that tests are written for every new code snippet added.



How to work well on teams:

humility, respect, and trust

insecurity stems from having work that isn't finished seen by other people

but working alone/hidden is inefficient - collaboration + review is very important

get feedback as early as possible, test as early as possible, and think about security and production environments as early as possible.

helps disperse knowledge, increases bus factor, reduces times stuck in a hole/ misses or time wasted working on the wrong thing from being isolated and having no oversight&#x20;

second pair of eyes are very helpful "many eyes makes all bugs shallow" "many eyes make sure your project stays relevant and on track"

working alone is inherently riskier than working with others, you should be much more concerned about wasting huge swaths of your time toiling away on the wrong thing.

On the other side of the conversation, you need to learn to accept criticism as well. This means not just being humble about your skills, but trusting that the other person has your best interests (and those of your project!) at heart and doesn’t actually think you’re an idiot. Programming is a skill like anything else: it improves with practice. If a peer pointed out ways in which you could improve your juggling, would you take it as an attack on your character and value as a human being? We hope not. In the same way, your self-worth shouldn’t be connected to the code you write—or any creative project you build. **To repeat ourselves: you are not your code. Say that over and over. You are not what you make. You need to not only believe it yourself, but get your coworkers to believe it, too.**



How to do code reviews:

Try not to be abrasive or too blunt; be considerate.

A typical code review at Google goes through the following steps:

1. A user writes a change to the codebase in their workspace. This author then cre‐ ates a snapshot of the change: a patch and corresponding description that are uploaded to the code review tool. This change produces a diff against the code‐ base, which is used to evaluate what code has changed.
2. The author can use this initial patch to apply automated review comments or do self-review. When the author is satisfied with the diff of the change, they mail the change to one or more reviewers. This process notifies those reviewers, asking them to view and comment on the snapshot.
3. Reviewers open the change in the code review tool and post comments on the diff. Some comments request explicit resolution. Some are merely informational.
4. The author modifies the change and uploads new snapshots based on the feed‐ back and then replies back to the reviewers. Steps 3 and 4 may be repeated multi‐ ple times.
5. After the reviewers are happy with the latest state of the change, they agree to the change and accept it by marking it as “looks good to me” (LGTM). Only one LGTM is required by default, although convention might request that all review‐ ers agree to the change.
6. After a change is marked LGTM, the author is allowed to commit the change to the codebase, provided they resolve all comments and that the change is approved. We’ll cover approval in the next section.

After all, someone is trying to check in code to their project/directory. They are more concerned with questions such as: “Will this code be easy or difficult to maintain?” “Does it add to my technical debt?” “Do we have the expertise to maintain it within our team?”





A well-designed code review process and a culture of taking code review seriously provides the following benefits:

* Checks code correctness
* Ensures the code change is comprehensible to other engineers
* Enforces consistency across the codebase
* Psychologically promotes team ownership
* Enables knowledge sharing
* Provides a historical record of the code review itself

Be Polite and Professional

As pointed out in the Culture section of this book, Google heavily fosters a culture of trust and respect. This filters down into our perspective on code review. A software engineer needs an LGTM from only one other engineer to satisfy our requirement on code comprehension, for example. Many engineers make comments and LGTM a change with the understanding that the change can be submitted after those changes are made, without any additional rounds of review. That said, code reviews can intro‐ duce anxiety and stress to even the most capable engineers. It is critically important to keep all feedback and criticism firmly in the professional realm.

In general, reviewers should defer to authors on particular approaches and only point out alternatives if the author’s approach is deficient. If an author can demonstrate that several approaches are equally valid, the reviewer should accept the preference of the author. Even in those cases, if defects are found in an approach, consider the review a learning opportunity (for both sides!). All comments should remain strictly profes‐ sional. Reviewers should be careful about jumping to conclusions based on a code author’s particular approach. It’s better to ask questions on why something was done the way it was before assuming that approach is wrong.

Reviewers should be prompt with their feedback. At Google, we expect feedback from a code review within 24 (working) hours. If a reviewer is unable to complete a review in that time, it’s good practice (and expected) to respond that they’ve at least seen the change and will get to the review as soon as possible. Reviewers should avoid responding to the code review in piecemeal fashion. Few things annoy an author more than getting feedback from a review, addressing it, and then continuing to get unrelated further feedback in the review process.



Types of Code Reviews

All code reviews are not alike! Different types of code review require different levels of focus on the various aspects of the review process. Code changes at Google gener‐ ally fall into one of the following buckets (though there is sometimes overlap):

* Greenfield reviews and new feature development
* Behavioral changes, improvements, and optimizations
* Bug fixes and rollbacks
* Refactorings and large-scale changes

