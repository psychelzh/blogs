---
title: My understanding on RDBMS
author: Liang Zhang
date: '2018-07-12'
categories:
  - Learning
  - Work
tags:
  - RDBMS
  - Tech
slug: my-understanding-on-rdbms
---

# RDBMS

It is a little late for me to dive into the **database** world. When I was at my master years, I have heard about `MySQL`, but never tried to learn about it. The datasets I had encountered with were relatively small in those days, and the request for a database management system was not so urging. Now when I began to appreciate the interesting logics and designing behind the database management system, I began to regret learning it so late.

Relational database management system (RDBMS) is at the center of **database** world. This fancy and interesting system, first advocated by [Codd](https://en.wikipedia.org/wiki/Edgar_F._Codd), makes data tidy, structured and comprehensible.

Relations can be viewed as maps between sets. In mathematics, a map can be injective, surjective or bijective. In database, the relation can be one-to-one, one-to-many (or many-to-one) and many-to-many. One-to-one and one-to-many (or many-to-one) relation can be easily mirrored by using two sets with a map between them, but the many-to-many relation is tricky. Strictly, all the many-to-many relations are indirect, with two underlying direct relations. In this way, a many-to-many relation can be mirrored by using three sets with two maps among them, and the third set is a junction set.

Could a relational database be a proper framework for all the data in our world? This philosophical question is hard to answer. In my view, however, it is correct but it is intimidating to design such relations for certain datasets, which I cannot figure out currently.
