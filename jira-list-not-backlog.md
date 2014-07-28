## JIRAの一覧はスクラムのプロダクトバックログではない

[原文(投稿日：2014/07/22)へのリンク](http://www.infoq.com/articles/jira-list-not-backlog)

まず初めに、この記事は素晴らしいツールであるJIRAを非難するものではない。*書き留めておきたいと思ったすべての一覧*の作成を支援する他の同類のツールに比べて、JIRAが広く知れ渡っているツールのため言及しているのだ。スクラム初心者たちが真のスクラムのプロダクトバックログ*において*正しくなく、混乱に陥っていることも合わせて伝えたい。次に述べるように、スクラムを始めるグループに「プロダクトバックログがあるか？」と尋ねると、いつも決まってその答えは、「えぇ、JIRA/...[^1]の一覧があるよ！」だ。

[^1]:訳者注 JIRA以外のTrac, Redmine, VersionOne, Rallyなどを…で示していると思われる。

そのため、この記事は特定のツールではなく、スクラムプロダクトバックログに*何が含まれる*べきなのかを記述する。

例として、本当の話（大規模スクラムを小規模スクラムに移行の一部分）とJIRAの一覧をスクラムのプロダクトバックログへ、元々は*508のJIRAのアイテムが23のプロダクトバックログのアイテム*にした*蒸留する*技法を共有する。つまり、20:1の縮小だ。もし、あなたのグループが同様の蒸留プロセスを行い、項目数の劇的な縮小を観測しないのであれば、プロダクトバックログには何が含まれるべきなのか、誤解している可能性がある。

## プロダクトバックログはどのように見えなければならないのか

プロダクトバックログは顧客主導のフィーチャの順序付きの一覧で、アイテム（またはPBI）と呼ばれている。

広く知れ渡っている誤解と反して、スクラムプロダクトバックログに「ストーリー」は含まれ*ない*。スクラムにおける著名な考えの一つは、スクラムは（「ストーリー」のような）プラクティスに関して規範的では*ない*ことだ。*スクラムガイド*[Schwaber & Sutherland, July 2013 / Definition of Scrum]を引用する：

*スクラムはプロダクトを構築するプロセスや技法ではなく、さまざまなプロセスや技法を取り入れることのできるフレームワークである。これらのプロダクト管理や開発プラクティスの相対的な有効性を明確にし、改善を可能にするのである。*

いずれにしても、アジャイル開発の*ストーリー*は、*対話（ストーリー=「カード、対話、確認」）による要求*の*振る舞い*であり、一覧それ*自体*ではない。

それゆえに、スクラムにおける要求へのアプローチはどのようにグループで使われるPBIに表現されるのか、もちろん進化していくのかもしれないのだ。PBIにどのように記述されるかに関わらず、要点はそれがユーザーに対する価値を重要視していることである。*スクラムガイド*を再び引用する：

*プロダクトバックログは、フィーチャ・機能・要求・要望をすべて一覧にしている。*

よい正確なプロダクトバックログは、チームが作業する上で少なくとも1スプリント分として十分な「準備完了（Ready）」（小さく、よく理解されている等）なストーリーを並び順の上に並べられた一覧である。スプリント期間が比較的長い場合は、適切に準備完了（Ready）または実行可能なPBIを絞り込むこと。*2*スプリント分の「準備完了（Ready）」なPBIを目指すのが良いだろう。並び順が下のPBIは不正確で、多くの場合、粒度が粗く、仕掛品ややり過ぎといった中身のないムダを削減する。

そのため、大きなプロダクトでさえも、よいプロダクトバックログでもっとも優れたPBI（並び順の上部に小さな「準備完了（Ready）」が記述されている）は漠然としていて、粒度の粗い仮置きである。このため、「大きな」プロダクトバックログでさえも比較的扱い易い。

## 巨大な「JIRA」一覧から始めるプロダクトバックログへの洗練された初期化技法

物事を具体的にするために、ここにJIRAの一覧をスクラムのプロダクトバックログに蒸留する実際の例がある。

簡単に508個のJIRAの課題をフィルタリングするために、4個毎に1枚の紙に印刷し、それを切り離した。これはすぐに操作できる物体のため、PBIを見つけるのにために不要なものを取り除くことができる。

対応できるものは四人しかおらず、その内、プロダクトに精通しているものは一人だけだった。学びを速めるために、専門家の指導を受けた。プロダクトバックログの最初の試みにおいて、信号をノイズと分類し、真のPBIに集中でき、素早くアイテムをバケツに入れるまったく新しい技法を適用した。JIRAの課題をPBIやバグ、タスク、必要に応じてその他のバケツに分類するためにAffinityクラスタリングに類似した技法を使用する。

1. 最初のサイクルにおいて、専門家が課題を1つ選択する。そして、声に出してからそれを検討する。それから、バケツ（カテゴリー）の中にそれを置く。このように、作業をし、根拠を示す。一握りの課題が検討され、カテゴライズされた後には、私たちはいくつかの最初のバケツと受入基準の漠然とした考えとプロダクトの専門家の論理のプロセスを得ることができた。
2. 全員が並行して作業する間、タイマーを5分に設定した。まず最初に、バケツの隣に課題を置く様に注意した。タイムボックスの終わりに、プロダクトの専門家は各バケツに仮置きされた課題をレビューした。正常な課題はバケツに進み、誤りは全員が受入基準や誤解を学べるように声に出して除去された。
3. これを5分サイクルで繰り返し行い、スループットが向上した各サイクルを観測したところ、誤り率が下がった。結局は、2時間ほどですべてのJIRAの一覧を23個の真のプロダクトバックログに分類できた。

![画像](http://www.infoq.com/resource/articles/jira-list-not-backlog/en/resources/1fig1.jpg)

## 開発の霧を取り除く

バケツとしてカテゴリーが明確になり、多くの課題が分類されると、いくつかの興味深いことに気付いた。例えば、チームがどれくらい課題を完了したのか、していないのか分からなくなっているというJIRAでの課題を明らかにした。

不動の人気の発見は「JIRAの課題を発行しよう！」というJIRAのラベル付けされた課題だ。

あなたの選択したバケツに課題を突っ込もう。このケースでは、「要求（真のPBI）」、「要求をサポートする（ほとんど関係ない課題、実際にはPBIではない）」、「タスク」、「適当なタスク」、「技術な改善点」、「要調査」、「？（完璧に無意味）」、「欠陥（バグ）」に分類した。

割り当ての結果、課題の大多数が欠陥（バグ）であることが分かった。個々のタスク（おそらくスプリントのためのタスク）は次の最大のバケツに含まれた。スプリントのためのタスクはプロダクトバックログに含まれない。いくつかの課題は何らかの調査で、たいてい見かけ上の失敗に関連していた。実際の顧客の要求や技術な改善点はだいたい同じ数で、残りのバケツはこれ以下だった。

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
