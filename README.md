# proud-pix
Tweet all the photos from a Flickr album

    ./proud-pix
    usage: proud-pix [-h] --flickr-username FLICKR_USERNAME [--index INDEX] [--dryrun] [--list-albums LIST_ALBUMS] [--sleep SLEEP] [--extra-hashtags EXTRA_HASHTAGS]

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

    marc@nephelai:~/proud-pix$ ./proud-pix --flickr-username marcn --index 9 --sleep 120  --dryrun
    (dry run) Tweeting: Sailing on Lake Winnipesaukee #flickr
    https://www.flickr.com/photos/marcn/37245222622
    (dry run) Tweeting: Butterfly II #flickr
    https://www.flickr.com/photos/marcn/36564631804
    (dry run) Tweeting: Butterfly Wing #flickr
    https://www.flickr.com/photos/marcn/37245219692

    
    marc@nephelai:~/proud-pix$ time ./proud-pix --flickr-username marcn --index 9 --sleep 120  
    Tweeting: Sailing on Lake Winnipesaukee #flickr
    https://www.flickr.com/photos/marcn/37245222622
    Tweeting: Butterfly II #flickr
    https://www.flickr.com/photos/marcn/36564631804

