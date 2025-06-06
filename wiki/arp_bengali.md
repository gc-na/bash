# [লিনাক্স] Bash arp ব্যবহার: নেটওয়ার্কে MAC ঠিকানা পরিচালনা

## Overview
`arp` কমান্ডটি নেটওয়ার্কে MAC ঠিকানা এবং IP ঠিকানার মধ্যে সম্পর্ক পরিচালনা করতে ব্যবহৃত হয়। এটি ARP (Address Resolution Protocol) টেবিল দেখার এবং সম্পাদনা করার জন্য ব্যবহার করা হয়, যা স্থানীয় নেটওয়ার্কে ডিভাইসগুলির মধ্যে যোগাযোগের জন্য গুরুত্বপূর্ণ।

## Usage
`arp` কমান্ডের মৌলিক সিনট্যাক্স হল:

```bash
arp [options] [arguments]
```

## Common Options
- `-a`: ARP টেবিলের সমস্ত এন্ট্রি দেখায়।
- `-d`: একটি নির্দিষ্ট IP ঠিকানা থেকে ARP এন্ট্রি মুছে ফেলে।
- `-s`: একটি নতুন ARP এন্ট্রি যুক্ত করে, যেখানে IP এবং MAC ঠিকানা উল্লেখ করতে হয়।
- `-n`: নাম সমাধান না করে শুধুমাত্র সংখ্যা দেখায়।

## Common Examples
নিচে কিছু সাধারণ উদাহরণ দেওয়া হল:

### ARP টেবিল দেখানো
```bash
arp -a
```

### একটি ARP এন্ট্রি মুছে ফেলা
```bash
arp -d 192.168.1.10
```

### একটি নতুন ARP এন্ট্রি যুক্ত করা
```bash
arp -s 192.168.1.20 00:1A:2B:3C:4D:5E
```

### সংখ্যা হিসেবে ARP টেবিল দেখানো
```bash
arp -n
```

## Tips
- ARP টেবিল নিয়মিতভাবে পরীক্ষা করা উচিত, বিশেষ করে যদি নেটওয়ার্কে নতুন ডিভাইস যুক্ত হয়।
- নিরাপত্তার জন্য, অজানা MAC ঠিকানা যুক্ত করা এড়িয়ে চলুন।
- ARP ক্যাশে পরিষ্কার করতে `arp -d` ব্যবহার করা যেতে পারে, যদি কোনো সমস্যা দেখা দেয়।