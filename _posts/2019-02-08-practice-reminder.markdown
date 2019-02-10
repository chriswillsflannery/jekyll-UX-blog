---
layout: post
title:  "UX Challenge: Be Reminded To Practice Your Instrument"
date:   2019-02-08 14:48:23 -0500
categories: jekyll update
---

The prompt is "Be Reminded to Practice Your Instrument." That's all we're given. No
further instructions, no specifications. I decided to tackle this from the perspective
of a developer, who is looking to implement solutions for a user, rather than as
a user myself. I started with the "Why":

![page 1](https://lh3.googleusercontent.com/hLGiUORBb8eGgguUxTQgK0LyuiwIccCnivlsDesC2gKBKQ7g2HLcmlflTHSXaGhX0D495CmfIW3Il4iWYG8wZtCmFA2T3Y_2iuqwqxQAQIhAgY42gVM7kEPCvG_cb6Ju4p1KFRSL4gQ1rN7IL8yODGofEfMgNzr3BtOHCwbsa647YgerYe1235GsbjISR25bYkiP5AJfEDKHLTm7u4ge2eBydEWuTfBuHhltdPPAPDXXPfZDBMV8fNqER0Y19EVoz0rbgMG1TyNV6e9Muvu5AfvOSdoqnZunxmoMIBYoj1J1QOzgz8TmysX5l4hBv7Sl-i8VWlZlSNnuRlZw4BZmgkxLpnC3pNSR0YuqOUWpGXo5jdBw5kxBpLlwL6i-sQ8x7jBAtbV7BVyDb5FLoNYQ9TASN9s3EJvRAXbFDp_q9mT93WeplgDSzQp4kkFZGF0LPeRnOtusKUc5qtrI9LzBSu-by0Shf1i7biFeHcTj7uPz0xJ8eO-Y9yT6hm-tQhga6PSEgSmHNpLaOkebj_yPlYYf6xiVtV4R0vfAVm2pWjrBQt8sluGn0SkyCOql7RLcZbQ9yLY43Z-ajnV1VJMS3H3GoP9IcpcFcWtOvmELTHKDj75-vH16qk2zkRj2ezgBhrPLgj3EapiCGxg7qGXfKshWi69Qjo4=w1248-h1713-no "Page 1")

I created three personas, drawing on traits from people who I know IRL. Each person
corresponds to one of the three "why's", in other words, what is the hangup for this
particular person not already practicing their instrument on a regimented schedule.

I did a bit of research into what some other platforms are offering in terms of
Reminder services, and as far as practicing goes (whether it be an instrument, a
sport, a hobby, or what have you), these were the three big takeaways:

![page 2](https://lh3.googleusercontent.com/c58LAd-rH-CzYTXMQ8zF9juL93kGmQN70tiEi9zT5ePhtItcIp2lxRWJgDJkJawn-eQsRMXwHjR_bu0YbBiHr3kAyRcZvK7QPmscllXBlP3zsuIELEqhvgZD-SFlW4oUBh8du3LnZUBAlN__x1sU8L7J2GqJTwl8KHcWNKvsvhK9_eypGzdx7r51dYZVmVWcKArZ5hcFqDMe2-bJR1kOBYoBXKK2IY6n2-Qzj6uXleEzs2WYkb5CSjU9tjTDdoP1wdOouibyCZq5gQ9M-X765t6XDqE2OMc7gGpB16zgpvI1euk6c8mvVOHLsMQcjEGos0BB9AElo8UtKVmwy6_zrH-PG_OlkLwQFpHnlikPrYjhD3P1ln7r2LpkgKLQi1JyRjfGpcbV5bTsLP-d1QPVq3jVN5Y3lu2af0HxNfQwktCD6p0CP_LJJ_u-mGB-7GmYUFaGMZhx0_OQPeSVw9vP5z633E-NnakQVNhMVvOSeEA-WxjMurI3JeuBC9Ogo-F_D3wd_IXwbSYs5eRb2cn3Skmq0nQ0XHASSMZ84U3X8VPkattgzZjQlKQs80_EouvN4vjh2h11ObsFUffAkw5nmzYh0gRA62ueqXh09x-i_5GMB1dd1NPLD5Wlgl_IqxXsxk6c8rWxfufZLflYfS0GWwCRHh_OzG8=w1248-h1713-no "Page 2")

Mobile push notifications seems to be the strategy which provides the most breadth across
user types, uses technology which is commonplace and familiar to most people, and is
customizable in terms of each user's needs.

As a developer, I then started to think about what building out this platform would
actually entail. Creating a proprietary mobile app seemed like total overkill,
when there are already great third-party push notification platforms which can be
integrated into other software. A much easier plan would be to build a simple,
responsive, one-page website where users can sign up for our service.

![page 3](https://lh3.googleusercontent.com/P4SBme2iQY52d8M3_v7STXMlhs4j_tXEDwcNqtFl33_DoyiDS8gl4vARa6z1Qk2sqq44PIJ0qgrRnNsaScjvU7lWpdhRCDD6rGgqtWbzIUE_5ni62SttvCMriGg87io304joikQw2k8D2zIogC8IpkF7WSHhS0Nxzig7TgNQNAVyOsxQi-oQ3Xdu8NyqkDvPj-ERF2_4BUFXOx0epc05wkmyrvSEdHR31OxT8VCik2EzsNVA7A7OBlpGiF5W4H5QKAtnPx63vWU1FBlKfisJVPhA672SAxgQqsnrtrH4AXQXzkw6ipDBbj-fIJzKNOoB9f6ulUSRMgoZPFINDHw4ZKgqrz1cMfvWSB-vxxdUz4ZKR5L7uUagK11v34ocuZmmlQi8S5OwQ3qjxI3n86H5qAngDZ8FM2x6XJLgAqTqzOFQ-nhyWGKx0kI_0uwucd32sjLsv98spmQTIGHdD9YQTO2u-Ox0XXADECUR2tZWMgOL1PJy1e4eKOcQGn1gqpEVOLUhAUCk1_yiL02LMY6_2d-MF8Pi3UUjZmCqF0wXeZSnkcx3a1mwA483Wxpx4aOGVj98XxENIPGyxph3wJVLoICJRPFFIVWdWH2WWW89pMeBm752mRQCoqonpkxKszLnazCFRvlqg_LnaEwGK8HRQrpHnRnWtB4=w1248-h1713-no "Page 3")

To help the ideation process of the site build, I made a usability flowchart to
help myself work through some of the key steps in the user's experience, and
in the developing company's experience. So not only are we thinking about the
true UX in terms of the user, we're also thinking about the UX of the developer
and their company on the back end.

The only thing left at this point is to take this logic and start to wireframe the
site. It can be super simple, slick and sleek, and will require minimal HTML, CSS,
Javascript and PHP. Then we're ready to build it!

![page 4](https://lh3.googleusercontent.com/iPz3CspbE8hliUs_TgUnYh5IVJit13crc9JJb76oVwnEqXqvRNknT5imrB8KAVf1B2NqsIdcksyXWztqyQhIv_IA2MlsEY4nbsLGUasM_8nl5TJmKgycvG5dzT5CoZ0I0ZipZ1Dm-B78nd7ISwHmmg-8irqQYhdaij2cxgZ1Ql2w6QCO3D9soJNJePtA9sJIz1KOFDaactLBeFCwg_ivR4zrKvwKAjenxbqQMys7IV5wog4gKkmlMSgvOSdtpS0fs_lhXQpUk8RC9t14XZ3YWv6K9VLuIIExd_BpME0xqKBww9aYOUm_qwl8bv771Py5SM6-L1IBmm19wyUXY_UnqzDOWWgSxDggFdz6-ojTNhnwwGyZ_hd4uydOBCRtyBEzGio1fWpmOn98qpC99SH70-lpJWGBdhRrsp264mgEIQxkYYowZWTxwN6tDN2fPruWP5Vvk-mHZzcp-Xwk9p9VfjykvvgWk98pZAGp_-TY4pmHJtXYWw4wkADlKiTC2Vi1AU7xPuaNgdOiUf8qRmtD60rGVROwB90tIcA3d137gcJYxdBGecQLXiZTyTKfATbC60u-a12UtgGJxDF6zkO1wzWnTxk0yDwKf2AK62zvKeG5Z3DkwQV7IKK_kv11uKOHkBOCWiGiNlfQBvywnp4yDMV3KXPBVoM=w1248-h1713-no "Page 4")
