# May Chong?

## Scam or not?

Recently, I received this email.

<figure><img src="../../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

This looks like a poorly constructed email, one because I don't use OneDrive, and second, who is May Chong? Take note that I configured Microsoft Outlook to **never download images no matter what by default**. This would potentially block any form of scripting that may download viruses just from opening the mail.&#x20;

Let's take a look at the website using Curl.

<figure><img src="../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>

So the link uses an index.php and takes some ?id= as the parameter. Interesting because I don't think I've ever seen such a link from NUS. Normally, NUS links come with a .nus.edu.sg domain or something to verfify it.&#x20;

When checking the rest of the HTML returned, we can see loads of JS.

<figure><img src="../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

Looks quite shabby doesn't it?



## The Website

This is what the website looks like:

<figure><img src="../../.gitbook/assets/image (147).png" alt=""><figcaption><p><em>May Chong's</em></p></figcaption></figure>

Interesting. We can play spot the difference between the image above, and the login from edurec!

<figure><img src="../../.gitbook/assets/image (160).png" alt=""><figcaption><p><em>Edurec</em></p></figcaption></figure>

Notice a key few differences. There is a property part missing. Also, on Edurec, it says **Register 2FA** and on the other website, it says **Help On 2FA.** Also, earlier I used curl to analyse the website to see loads of hidden JS being executed. However, the main page only reveals this in their page source.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

We can test the login as follows:

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

After logging in, it looks like this was just a phishing campaign!

<figure><img src="../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

Quite cool that NUS would go to this trouble to actually teach us about phishing. No wonder I didn't get a notif about this!&#x20;

## Conclusion

I think it's safe to say that this website is indeed a scam. The differences in English, subtle changes here and there, the weird index.php page and all that lead me to believe that this is indeed some form of scam.&#x20;