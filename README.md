# proud-pix
Tweet all the photos from a Flickr album

    ./proud-pix
    usage: proud-pix [-h] --flickr-username FLICKR_USERNAME [--index INDEX] [--dryrun] [--list-albums LIST_ALBUMS] [--sleep SLEEP]

# Requirements

* Python2.7
* [tweepy](https://github.com/tweepy/tweepy)

    `sudo yum install python2-pip`

    `sudo pip install tweepy`

* [python-flickr-api](https://github.com/alexis-mignon/python-flickr-api/)

    `sudo pip install flickr_api`

    `sudo pip install python-oauth2`

    `sudo pip install six`

* Get your twitter and flickr api keys and put them in `~/proud-pix.ini`

# examples

    marc@nephelai:~/proud-pix$ ./proud-pix --flickr-username marcn --list-albums 10
    (0, u'Soap Bubbles (20171227)')
    (1, u'Newburyport photowalk 20171202')
    (2, u'Lobster Chinese-style @ Gaga Seafood Restaurant')
    (3, u'Anti-fascist counter-rally @ Boston Common (20171118)')
    (4, u'Exeter photowalk (2017)')
    (5, u'Manchester Photowalk (20171104)')
    (6, u'Boston Book Fest (20171028)')
    (7, u'NH Walk for Epilepsy 2017')
    (8, u'Fryeburg Fair, Fryeburg ME (20171007)')
    (9, u'Meredith, NH (20170923)')
    marc@nephelai:~/proud-pix$

    marc@nephelai:~/proud-pix$ time ./proud-pix --flickr-username marcn --index 9 --sleep 120  --dryrun
    (dry run) Tweeting: Sailing on Lake Winnipesaukee #flickr
    https://www.flickr.com/photos/marcn/37245222622
    (dry run) Tweeting: Butterfly II #flickr
    https://www.flickr.com/photos/marcn/36564631804
    (dry run) Tweeting: Butterfly Wing #flickr
    https://www.flickr.com/photos/marcn/37245219692
    (dry run) Tweeting: Butterfly I #flickr
    https://www.flickr.com/photos/marcn/36564630304
    (dry run) Tweeting: Finding the perfect flower #flickr
    https://www.flickr.com/photos/marcn/37245218532
    (dry run) Tweeting: Girls at Lake Winnipesaukee #flickr
    https://www.flickr.com/photos/marcn/37416895555
    (dry run) Tweeting: Cold Beer and Charcuterie #flickr
    https://www.flickr.com/photos/marcn/37227635236
    (dry run) Tweeting: Come to the water #flickr
    https://www.flickr.com/photos/marcn/37416892935
    (dry run) Tweeting: Swimming Dock #flickr
    https://www.flickr.com/photos/marcn/37227631706
    (dry run) Tweeting: Tiny birdhouse #flickr
    https://www.flickr.com/photos/marcn/37227630366
    (dry run) Tweeting: Lake Winnipesaukee #flickr
    https://www.flickr.com/photos/marcn/36604929243
    (dry run) Tweeting: Lobster Roll #flickr
    https://www.flickr.com/photos/marcn/36604927243
    (dry run) Tweeting: #Instagram #flickr
    https://www.flickr.com/photos/marcn/37416880565
    (dry run) Tweeting: Downeast Corndog (deep fried Lobster) #flickr
    https://www.flickr.com/photos/marcn/36564605944
    (dry run) Tweeting: Miss Meredith #flickr
    https://www.flickr.com/photos/marcn/36604923883
    (dry run) Tweeting: Live Free & Eat Lobster #flickr
    https://www.flickr.com/photos/marcn/36604920513
    (dry run) Tweeting: Fishing on Lake Winnipesaukee #flickr
    https://www.flickr.com/photos/marcn/37227616656
    (dry run) Tweeting: Green eye #flickr
    https://www.flickr.com/photos/marcn/36604917643
    (dry run) Tweeting: Faux Swan #flickr
    https://www.flickr.com/photos/marcn/37018646400
    
    real	0m1.597s
    user	0m0.154s
    sys	0m0.025s
    marc@nephelai:~/proud-pix$ 
    
    marc@nephelai:~/proud-pix$ time ./proud-pix --flickr-username marcn --index 9 --sleep 120  
    Tweeting: Sailing on Lake Winnipesaukee #flickr
    https://www.flickr.com/photos/marcn/37245222622
    Tweeting: Butterfly II #flickr
    https://www.flickr.com/photos/marcn/36564631804
    Tweeting: Butterfly Wing #flickr
    https://www.flickr.com/photos/marcn/37245219692
    Tweeting: Butterfly I #flickr
    https://www.flickr.com/photos/marcn/36564630304
    Tweeting: Finding the perfect flower #flickr
    https://www.flickr.com/photos/marcn/37245218532
    Tweeting: Girls at Lake Winnipesaukee #flickr
    https://www.flickr.com/photos/marcn/37416895555
    Tweeting: Cold Beer and Charcuterie #flickr
    https://www.flickr.com/photos/marcn/37227635236
    Tweeting: Come to the water #flickr
    https://www.flickr.com/photos/marcn/37416892935
    Tweeting: Swimming Dock #flickr
    https://www.flickr.com/photos/marcn/37227631706
    Tweeting: Tiny birdhouse #flickr
    https://www.flickr.com/photos/marcn/37227630366
    Tweeting: Lake Winnipesaukee #flickr
    https://www.flickr.com/photos/marcn/36604929243
    ^CTraceback (most recent call last):
      File "./proud-pix", line 77, in <module>
        time.sleep(float(args.sleep))
    KeyboardInterrupt
    
    real	22m4.749s
    user	0m0.286s
    sys	0m0.043s
    marc@nephelai:~/proud-pix$ 
    
    
    
    
