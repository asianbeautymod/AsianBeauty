#remove user posts
 author:
     name: [Cherylcheryl, Mabeline1234, Sally19881988, kerry611, anotherabblogger]
 action: remove
---
 # Locked threads
 is_edited: false
 parent_submission:
     id: [2g3sqq, 34sij6]
 action: remove
---
 # Auto-remove words/phrases
 title+body: [nigger, cunt, faggot, slut, whore, bitch, asshole, rape, retard, q-depot, go-iaso, melodycosme, melody]
 action: remove
---
 #Reported Items
 reports: 5
 modmail: The above {{kind}} by /u/{{author}} has received 5 reports. Please investigate.
---
 #Heavily Reported Items - Removal
 reports: 5
 action: remove
 modmail: The above {{kind}} by /u/{{author}} was removed because it received 5 reports. Please investigate and ensure that this action was correct.
---
 #Disgused Links
 body (regex): "(\\[(?P<text>(http|www)\\S+)\\]\\((?!(?P=text))(http|www)\\S+\\))"
 action: remove
 modmail: The above {{kind}} by /u/{{user}} was removed because it contained a disguised link. Please investigate immediately.
---
 #URL Shortner Ban
 domain+body: [bit.ly, bit.do, tl.gd, adf.ly, is.gd, goo.gl, j.mp, t.co, tinyurl.com, qqurl.com, tiny.cc, lnkd.in, db.tt, qr.ae, bitly.com, cur.lv, ow.ly, adcrun.ch, ity.im, q.gs, viralurl.com, vur.me, bc.vc, twitthis.com, u.to, j.mp, buzurl.com, cutt.us, u.bb, yourls.org, crisco.com, x.co, prettylinkpro.com, viralurl.biz, adcraft.co, virl.ws, scrnch.me, filoops.info, vurl.bz, vzturl.com, lemde.fr, qr.net, 1url.com, tweez.me, 7vd.cn, v.gd, dft.ba, aka.gr, tr.im, tinyarrows.com, xn--hgi.ws, amzn.to, "➡.ws"]
 action: remove
 message: |
     Your [{{kind}}]({{permalink}}) in /r/{{subreddit}} was automatically removed because you used a URL shortener.

     URL shorteners are not permitted in /r/{{subreddit}} as they impair our ability to enforce link blacklists.

     Please re-post your {{kind}} using direct, full-length URL's only.
---
 #Link-only self post
 type: text submission
 body (regex, full-text): "(\\[.*\\]\\()?https?://\\S+\\)?"
---
 #Phone Number Removal
 title+body (regex): ["\\(?(\\d{3})\\)?([ .-])(\\d{3})([ .-])(\\d{4})","(\\d{5})([ .-])(\\d{6})","\\(?(\\d{4})\\)?([ .-])(\\d{3})([ .-])(\\d{3})","\\(?(\\d{2})\\)?([ .-])(\\d{4})([ .-])(\\d{4})","\\(?(\\d{2})\\)?([ .-])(\\d{3})([ .-])(\\d{4})","\\+([\\d ]{10,15})"]
 ~body+url (regex): "(\\[[^\\]]+?\\]\\()?(https?://|www\\.)\\S+\\)?"
 ~body+title+url (regex): ["(800|855|866|877|888|007|911)\\W*\\d{3}\\W*\\d{4}", "\\d{3}\\W*555\\W*\\d{4}", "999-999-9999", "000-000-0000", "123-456-7890", "111-111-1111", "012-345-6789", "888-888-8888", "281\\W*330\\W*8004", "777-777-7777", "678-999-8212", "999([ .-])119([ .-])7253","0118 999 811","0118 999 881", "867( -)?5309", "505\\W*503\\W*4455", "1024 2048"]
 action: remove
 modmail_subject: Doxxing Alert!
 modmail: |

     {{permalink}}

     The above {{kind}} by /u/{{author}} was removed because it contained a possible phone number. Please investigate immediately.

     If the user is doxxing, [ban them](/r/{{subreddit}}/about/banned) and [report them to the reddit admins](http://www.reddit.com/message/compose?to=%2Fr%2Freddit.com&subject=Doxxing%20Report:%20%2Fu%2F{{author}}&message=%2Fu%2F{{author}}%20posted%20a%20phone%20number:%20{{permalink}}) immediately.
 action: remove
---
 #Email Addresses
 title+body (regex): "[!#$%&'*+./0-9=?_`a-z{|}~^-]+@[.a-z-]+\\.(?:com|org|net)"
 ~title+body#whitelist: [roseroseshop@hotmail.com]
 action: remove
 modmail_subject: Doxxing Alert!
 modmail: |

     {{permalink}}

     The above {{kind}} by /u/{{author}} was removed because it contained a possible email address. Please investigate immediately.

     If the user is doxxing, [ban them](/r/{{subreddit}}/about/banned) and [report them to the reddit admins](http://www.reddit.com/message/compose?to=%2Fr%2Freddit.com&amp;subject=Doxxing%20Report:%20%2Fu%2F{{author}}&message=%2Fu%2F{{author}}%20posted%20an%20email%20address:%20{{permalink}}) immediately.
---
 #Credit Card Numbers
 title+body (regex): "\\b(?:4[0-9]{12}(?:[0-9]{3})?|5[12345][0-9]{14}|3[47][0-9]{13}|3(?:0[012345]|[68][0-9])[0-9]{11}|6(?:011|5[0-9]{2})[0-9]{12}|(?:2131|1800|35[0-9]{3})[0-9]{11})\\b"
 action: remove
 modmail_subject: Doxxing Alert!
 modmail: |

     {{permalink}}

     The above {{kind}} by /u/{{author}} was removed because it contained a possible credit card number. Please investigate immediately.

     If the user is doxxing, [ban them](/r/{{subreddit}}/about/banned) and [report them to the reddit admins](http://www.reddit.com/message/compose?to=%2Fr%2Freddit.com&amp;subject=Doxxing%20Report:%20%2Fu%2F{{author}}&message=%2Fu%2F{{author}}%20posted%20a%20credit%20card%20number:%20{{permalink}}) immediately.

---
#Autosorting for scheduled posts
 author: Automoderator
 set_suggested_sort: new
 type: submission
 title: ["ASK HERE! Daily Help, and Questions:", "Weekly Random Chat", "Rants, Raves, and Mini Reviews", "Glamday", "Weekly Deals"]
---
     #Website Blacklist
 domain+body+title: [q-depot.com, proud-tobe-asian.blogspot.jp]
 action: spam
---
     #Autoflair Posts
 title (includes): ["Question", "question"]
 moderators_exempt: true
 set_flair: ["Question", "question"]
---
 title (includes): ["PSA"]
 moderators_exempt: true
 set_flair: ["PSA","PSA"]
---
 title (includes): ["Review", "REVIEW", "review"]
 moderators_exempt: true
 set_flair: ["Reviews", "review"]
---
 title (includes): ["Swatch", "FOTD", "Face of the day"]
 moderators_exempt: true
 set_flair: ["Swatches & FOTD", "swatches-fotd"]
---
 title (includes): ["Haul", "haul", "hauls", "Hauls", "HAUL", "HAULS"]
 moderators_exempt: true
 set_flair: ["Hauls", "hauls"]
---
 title (includes): ["Fluff", "FLUFF", "fluff"]
 moderators_exempt: true
 set_flair: ["Fluff", "fluff"]
---
 title (includes): ["Discussion", "discussion", "DISCUSSION"]
 moderators_exempt: true
 set_flair: ["Discussion", "discussion"]
---
 title (includes): ["Glamday", "glamday", "GLAMDAY"]
 moderators_exempt: true
 set_flair: ["Glamday", "glamday"]
---
 title (includes): ["Discovery", "discovery", "DISCOVERY"]
 moderators_exempt: true
 set_flair: ["Discovery", "discovery"]
---
 title (includes): ["Roundup", "Weekly Roundup", "roundup", "ROUNDUP"]
 moderators_exempt: true
 set_flair: ["Roundup", "roundup"]
---
 title (includes): ["Deals", "deal", "deals", "Deal", "DEAL", "DEALS"]
 moderators_exempt: true
 set_flair: ["Deals", "deals"]
---
 title (includes): ["Meetups", "Meetup", "meetup", "meetups", "MEETUP"]
 moderators_exempt: true
 set_flair: ["Meetups", "meetups"]
---
 title (includes): ["Journal", "ABJournal"]
 moderators_exempt: true
 set_flair: ["Journal", "journal"]
---

 #Description reminder for external links
 type: link submission
 message: |
     Hello there! We have a [rule](https://www.reddit.com/r/AsianBeauty/wiki/rules#wiki_rules_and_guidelines) that all external link submissions must be accompanied by a comment describing the content of the link. Haul posts must also have a comment listing the contents of the haul. This is just a reminder to post a description comment or your post may be removed!
---
 moderators_exempt: true
 is_edited: false
 ~title:
     - "[Question]"
     - "[Questions]"
     - "[PSA]"
     - "[Review]"
     - "[Reviews]"
     - "[Swatch]"
     - "[Swatches]"
     - "[FOTD]"
     - "[Face of the day]"
     - "[Haul]"
     - "[Hauls]"
     - "[Fluff]"
     - "[Discussion]"
     - "[Glamday]"
     - "[Discovery]"
     - "[Roundup]"
     - "[Weekly Roundup]"
     - "[Deals]"
     - "[Deal]"
     - "[Meetups]"
     - "[Meetup]"
     - "[Journal]"
     - "[ABJournal]"
 action: remove
 comment: |
     Your submission has been removed because it did not contain a matching flair tag in the title. Please **resubmit** your post with an appropriate tag.

     These are the currently available tags:
     **[Question] [PSA] [Review] [Swatch] [FOTD] [Haul] [Fluff] [Discussion] [Glamday] [Discovery] [Roundup] [Deals] [Meetup] [Journal]**
     If you have questions, [send us a mailmail!](https://www.reddit.com/message/compose?to=%2Fr%2FAsianBeauty)
