# Zomnified Blogs Dataset
# Description

This repository contains the dataset used in our research on Zombified Blogs, which investigates suspicious posts on abandoned blogs.

All datasets are malicious posts and associated analyses collected in the Large-scale Collection of Historical Data.

## Directory Tree

<pre>
.
├── README.md
├── bitcoin_transaction_results
│   ├── 113mmANKkj7LCDjAw376rb1sm37gWABJyT.json
│   ├── ...
│   └── 3PsvkezhBJv1Uu4Rqj2Xw9EWEhx5UXVgtd.json
├── fraud_bitcoin_wallet_addresses
│   ├── blogspot.com.txt
│   ├── jugem.jp.txt
│   ├── sblo.jp.txt
│   ├── seesaa.net.txt
│   ├── ss-blog.jp.txt
│   └── wordpress.com.txt
├── malicious_detection_post_urls
│   ├── blogspot.com.txt
│   ├── jugem.jp.txt
│   ├── sblo.jp.txt
│   ├── seesaa.net.txt
│   └── ss-blog.jp.txt
├── malicious_post_texts
│   ├── blogspot.com
│   │   ├── 13ansjuradoloisfoot.blogspot.com.json
│   │   ├── ...
│   │   └── zenamap.blogspot.com.json
│   ├── jugem.jp
│   │   ├── 0166.jugem.jp.json
│   │   ├── ...
│   │   └── zoomin-surf.jugem.jp.json
│   ├── sblo.jp
│   │   ├── 1adsen.sblo.jp.json
│   │   ├── ...
│   │   └── vingt-trente.sblo.jp.json
│   ├── seesaa.net
│   │   ├── 11toefl.seesaa.net.json
│   │   ├── ...
│   │   └── wagonr1770.seesaa.net.json
│   ├── ss-blog.jp
│   │   ├── amway37ch.blog.ss-blog.jp.json
│   │   ├── ...
│   │   └── t9658880.blog.ss-blog.jp.json
│   └── wordpress.com
│       ├── allaboutbhagyashreen.wordpress.com.json
│       ├── ...
│       └── yongyumk381.wordpress.com.json
├── malicious_post_urls
│   ├── blogspot.com.txt
│   ├── jugem.jp.txt
│   ├── sblo.jp.txt
│   ├── seesaa.net.txt
│   ├── ss-blog.jp.txt
│   └── wordpress.com.txt
├── malicious_urls
│   ├── blogspot.com.txt
│   ├── jugem.jp.txt
│   ├── sblo.jp.txt
│   ├── seesaa.net.txt
│   ├── ss-blog.jp.txt
│   └── wordpress.com.txt
├── passive_dns_results
│   ├── 000.amz00loan.net.json
│   ├── ...
│   └── zzhaoqn.cn.json
├── submission_email_addresses
│   ├── blogspot.com.txt
│   ├── jugem.jp.txt
│   ├── sblo.jp.txt
│   ├── seesaa.net.txt
│   └── ss-blog.jp.txt
├── initial_phishing_email_titles.txt
└── notification_text.txt
</pre>


## Directory Descriptions

- **bitcoin_transaction_results/**: Transaction history of reported fraud among bitcoin wallet addresses included in the body of malicious posts on Zombified Blogs.
  - `[BitcoinWalletAddress].json`: Each JSON file contains the transaction results for the corresponding Bitcoin wallet address. The key of `total_recieved` represents the total amount received by the Bitcoin wallet address and `total_sent` represents the total amount transferred by the Bitcoin wallet address.
- **fraud_bitcoin_wallet_addresses/**: List of Bitcoin wallet addresses included in malicious posts on Zombified Blogs found on various blog services.
  - `[BlogService].txt`: Each TXT file contains the transaction results for the corresponding Bitcoin wallet address. Each TXT file contains the bitcoin wallet address found on that blog service. These files consist of one line per Bitcoin wallet address.
- **malicious_detection_post_urls/**: List of URLs of Zombified Blogs posts that have been detected by VirusTotal (i.e., blogs that were legitimately used in the past have been flagged as malicious by the anti-virus).
  - `[BlogService].txt`: Each TXT file consists of one URL per line with the URL of the blog post that was determined to be malicious.
- **malicious_post_texts/**: List of text of malicious posts from Zombified Blogs found on each blog service.
  - **blogspot.com/**:
      - `[BlogDomainName].json`: Each JSON file contains information related to the text of the malicious posts. The key of `post_link` is the URL of the malicious post, `post_title` is the title of the post, post_text is the raw body of the post, `cleaned_post_text` is the formatted body of the post, and `lang` is the result of language identification of the post body.
  - **jugem.jp/**, **sblo.jp/**, **seesaa.net/**, **ss-blog.jp/**, **wordpress.com/**: Follow the same structure as `blogspot.com/`, containing respective data.
- **malicious_post_urls/**: List of URLs of malicious posts on Zombified Blogs found on each blogging service.
  - `[BlogService].txt`: Each TXT file consists of one line of the URL of the malicious post on each blog service.
- **malicious_urls/**: List of external malicious URLs of malicious posts found on Zombified Blogs.
  - `[BlogService].txt`: Each TXT file consists of one line of malicious URLs that lead to external sites detected in each blog service.
- **passive_dns_results/**: List of passive dns results related to malicious URL domain names that lead externally in malicious posts.
  - `[DomainName].json`: Each json file shows the number of name resolutions per IP address associated with the domain name. The key of `domain` is the corresponding domain name, `count` is the number of name resolution, `first_seen` is the date and time of the first observation, `last_seen` is the date and time of the last observation, ip_address is the IP address associated with the domain, and `type` is either IPv4 or IPv6.
- **submission_email_addresses/**: List of submission email addresses of Zombified Blogs identified in the experiment.
  - `[BlogService].txt`: Each TXT file consists of one email address per line, with the submission email address extracted from Zombified Blogs on each blog service.

- `initial_phishing_email_titles.txt`: List of phishing email titles that created the initial search query for the proposed method.

- `notification_text.txt`: Text of the email notifying the existence of malicious posts on each blog service.

- `README.md`: This readme file.
