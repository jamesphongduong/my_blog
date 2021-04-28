---
layout: post
title: Database - ACID
date: 2021-04-28 10:00:18 +1000
categories: tech
---

**ACID** is a set of standards that database transactions should follow to ensure data validity.

# Atomic

Transactions are atomic, managing a set of operations as a _single_ operation, so it either succeeds or fails completely.

For example, imagine a bank transfer from account A to account B. The two operations are:

1. Withdraw funds from account A
2. Deposit funds into a account B

It makes sense that this group of operations should either succeed or fail completely, to ensure the fund amounts remain in a consistent state, i.e. funds are neither lost or created if any of the operations failed.

# Consistent

Transactions are consistent, respecting the requirements defined.

A example requirement is all user emails in a database are unique.

# Isolated

Transactions are isolated, ensuring concurrent transactions leaves the database in the same state as if the transactions were ordered sequentially.

# Durable

Transactions are durable and successfully commited transactions are saved permanently, even in the case of system failures. This is done by saving all transctions to non-volatile memory (not just RAM).
