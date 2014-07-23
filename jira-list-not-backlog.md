## JIRAのリストはスクラムのプロダクトバックログでははない

[原文(投稿日：2014/07/22)へのリンク](http://www.infoq.com/articles/jira-list-not-backlog)

まず初めに、この記事はJIRAが素晴らしいツールではないというものではない。この広く一般的に用いられているツールは、他のツール（Trac、Redmine、VersionOne、Rallyなど）と同様に*書き留めておきたいと思ったすべてのリスト*の作成を支援し、スクラムに取り組む新しい人々に*Todoリスト*である真のスクラムプロダクトバックログを誤らせ、混乱させることについて言及している。例えば、あるグループがスクラムの導入を開始した際に“プロダクトバックログがあるか？”と尋ねると、常にその答えは“えぇ、JIRA/...[^1]のリストがあるよ！"なのである。

[^1]:訳者注 JIRA以外のTrac, Redmine, VersionOne, Rallyなどを…で示していると思われる。

そのため、この記事では、特定のツールではなく、スクラムプロダクトバックログの*内容*について記述する。

例として、実際の話(大規模スクラムへの移行の一部分 -- LeSS)やJIRAのリストからスクラムプロダクトバックログへと、*508のJIRAの項目だったものから、23のプロダクトバックログ項目に*抽出するテクニックについて共有する。つまり、1/20へ縮小である。あなたのグループが同様の抽出工程を行い、項目数が劇的に縮小されるのを目撃していないのであれば、あなたのグループはプロダクトバックログにあるべき項目を誤解している可能性がある。

## プロダクトバックログはどのように見えなければならないのか

プロダクトバックログは顧客主導のフィーチャーの順序付きのリストで、アイテムまたはPBIsと呼ばれている。

広く知れ渡っている誤解と反して、スクラムプロダクトバックログに“ストーリー”は含まれ*ない*。スクラムでの著名のアイディアの一つは、それが“ストーリー”のようなプラクティスに関して規範的では*ない*ことだ。*スクラムガイド*[Schwaber & Sutherland, July 2013 / Definition of Scrum]を引用する:

*スクラムは製品を構築するためのプロセスでもテクニックでもなく、むしろ、様々なプロセス、テクニックを利用できるフレームワークと言える。スクラムは改善できるように製品マネジメントと開発プラクティスの相対効果を明確にする。*

いずれにしても、アジャイル開発の*ストーリー*は、*対話（ストーリー=“カード、対話、確認”）による要件*の*振る舞い*であり、リストそれ*自体*ではない。

Therefore, in Scrum the approach to requirements and how they are expressed as PBIs can be any way that a group finds useful, and may of course evolve. Regardless of how PBIs are written, the bottom line is that it emphasizes the things of value to the users. Again to quote *The Scrum Guide*:

*The Product Backlog lists all features, functions, requirements, enhancements…*

A well-refined Product Backlog will have enough “ready” (small, well-understood, ...) work near the top of the (ordered) list to keep the Team(s) fed for at least one Sprint, although when the cycle time to properly refine ready or actionable a PBI is relatively long, you may want to aim for *two* Sprints worth of “ready” PBIs. Lower-ordered PBIs are less refined and often more coarse-grained, reducing the lean wastes of work-in-process and over-processing.

Therefore, even for big products, in a good Product Backlog most PBIs (those beyond the small “ready” set near the top) will be vague and coarse-grained placeholders. This makes working with even a “large” Product Backlog relatively tractable.

## Initial Product Backlog Refinement Technique, Starting With a Big ‘JIRA’ List

To make things concrete, here is a real-life example of distilling a JIRA list into a Scrum Product Backlog.

To easily filter the 508 JIRA issues, we started by printing them out on paper, four per page, and cutting them up. This quickly gives us physical objects we can manipulate as we group and filter to find the PBIs.

We happened to have four people available, only one of which was familiar with the product. To accelerate learning, we had our expert guide us. To sort the signal from the noise in our initial attempt at a product backlog, we applied a novel technique to quickly bucket the items so we could focus on the real PBIs. We use a technique similar to affinity clustering to sort the JIRA issues into PBI, bugs, tasks and various other buckets as required.

1. The initial cycle consisted of having our expert select an issue, consider it out loud and place it in a bucket (category), thus demonstrating his reasoning to us as he did the work. After a handful of issues were considered and categorized, we had some initial buckets and a vague idea of the criteria and reasoning process the product expert was using.

2. We set a timer for five minutes while we all worked in parallel. Initially we were careful to place our issues adjacent to the buckets, rather than in them. At the end of the timebox our product expert reviewed the issues tentatively queued for each bucket. Correct assignments were promoted into the bucket, and errors were debugged out loud so we could all learn about some criteria or misunderstanding that applied.
3. We repeated these five minute cycles and observed that each cycle our throughput went up and our error rate went down. In the end we were able to sort the entire JIRA list in about two hours, leaving us with 23 genuine Product Backlog Items.

![画像](http://www.infoq.com/resource/articles/jira-list-not-backlog/en/resources/1fig1.jpg)

## Clearing the Fog of Development

As the bucket categories emerged and classified more issues, we noticed several interesting things. For instance, we uncovered issues in JIRA that the Team had lost track of, that should have been closed, or were otherwise orphaned.

Our all-time favorite discovery was a JIRA issue labeled, “create a JIRA issue”!

Let the issues guide your choice of buckets. In our case we had “requirements” (the real PBIs), “support requirements” (tangential issues, not actually PBIs), “tasks”, “fitnesse tasks”, “tech improvements”, “to be investigated”, “?” (complete nonsense), and “defects” (bugs).

In terms of distribution, we found that the vast majority of issues were defects (bugs). Individual tasks (presumably tasks for some Sprint) comprised the next largest bucket we found -- and Sprint tasks do not belong in a Product Backlog. Some issue were to investigate something, usually related to some apparent failure. Actual customer requirements and technical improvements were roughly the same count, with the remaining buckets even smaller.

Imagine being a Product Owner and having to wade through 50 bugs or Sprint task issues before finding something that looks like a customer requirement. While all these issues are important to someone, separation of concerns is a valuable technique to keep the Product Backlog tractable and interesting to the Product Owner.

As mentioned in the introduction, when the fog was fully cleared, the original list of 508 issues boiled down to 23 relevant Product Backlog items of customer-centric new requirements.

We have done many of these list-filtering workshops when first moving to LeSS, and a reduction down to 5 or 10% of the original list size is not uncommon. That said, there is a high standard deviation; we have also worked on LeSS transitions where 90% of the original pre-Scrum list of items were true high-quality requirements and made their way without change into the new Product Backlog.

As an example of the wide deviation, during another session where the list (nominal Product Backlog) was taken from a spreadsheet, after applying this filtering technique, the “Normal Features” bucket was relatively high, north of 20%. But that’s still a lot of noise.

![画像](http://www.infoq.com/resource/articles/jira-list-not-backlog/en/resources/1fig2.jpg)

## In Scrum, Where to Record Product Defects?

A common question in Scrum is, “Where to record defects?” In small-scale one-team Scrum with only a few defects, recording them in the Product Backlog is a simple and sensible solution, and classic Scrum advice. But when first transitioning to LeSS, in a large product with many teams and years of pre-Scrum legacy defects building up in the JIRA list, recording them in the Product Backlog is not tenable; there are just too many.

In the case study we are describing, we discovered more than half of the total of 508 issues were defects. So as is common in such cases, our alternate solution was to keep the record of defects in JIRA.

## And Where to Record Technical Improvements or Engineering Tasks?

As with the defects issue, a common question in Scrum is, “Where to record technical improvements and/or engineering tasks?” In one-team Scrum on a small product with a few improvements, and a seasoned Product Owner, keeping them in the Product Backlog is a reasonable option.

But context is king here: Once again, similar to the situation regarding defects, when (1) you are in a large-scale Scrum context and there are a ‘hundred’ miscellaneous improvements in the original ‘JIRA’ list that swamp the small set of customer requirements, and (2) there is a new Product Owner just joining from the business side who has no interest in getting drawn into “techy issues” and is only grudgingly getting involved in this new role, and is fearful of being expected to do traditional IT project manager problem solving, then you have to be sensitive to the situation in terms of making an attractive Product Backlog that speaks to the things that the novice business-side Product Owner cares about, and be careful to not “put them off” during this transition step.

So our solution was to keep the very large list of technical improvements and engineering tasks in JIRA.

## A Happier Business-Side Product Owner

As you know, one of the major changes in moving to Scrum is to engage a *business-side* Product Owner. What you may not know is that when Scrum is introduced to the business community or Product Management (from where a Product Owner will usually come), that community of people often privately (if not publicly) voice this concern:

*Why do we have to get involved in all that messy techy stuff? I’m not interested in doing project management of defects, engineering tasks, and so on. I just want to focus on the business features we need.*

And that concern is exacerbated in the large-scale case transitioning to LeSS, where there aren’t 4 existing defects and engineering tasks to manage, but 304! To expose a potential new business-side Product Owner to all this ‘noise’ is very off-putting for many of them.

So we like to separate the signal from noise, and introduce them to an attractive clean Product Backlog that contains things they really care about (the new features) without all the unattractive myriad technical issues they are concerned they will be sucked into having to manage, as a traditional project manager would.

Imagine the delight of a new business-side Product Owner to discover that instead of having to manage a list of 508 issues, they only need to focus on a list of 23 small and relevant-to-them items.

The hanging issue of managing the hundreds or thousands of remaining defects and engineering tasks in a young LeSS adoption with a new business-side Product Owner is an important issue, but outside the scope of this article. Please watch for an upcoming article" on Handling Defects & Technical Improvements in Large-Scale Scrum (LeSS).

## Simple Tools

Staying on the theme of attracting a new and nervous business-side Product Owner… What tool do they already know and are comfortable with? Probably not JIRA/Trac/..., but almost certainly a spreadsheet! (These days, probably a Google Docs spreadsheet). And it is the classic recommended tool for a Scrum Product Backlog. Therefore, consider keeping your practices simple and your changes simple for the new Product Owner by using a spreadsheet. We have seen LeSS adoptions involving hundreds of people and multiple sites quite effectively use a simple spreadsheet for the new Product Backlog. And be suspicious of claims that anything more complicated than a spreadsheet and wiki is needed -- even in large-scale cases.

Even simpler!... We even have Product Owners that (literally) tape one card per PBI on a wall and manage their Product Backlog that way.

The point is to keep the Product Backlog clean -- especially for the large-scale transition case with a new business-side Product Owner. Keep items of customer value in the Product Backlog and keep it accessible.