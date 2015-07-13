CrawlerDetect
=======
[![Build Status](https://img.shields.io/travis/JayBizzle/Crawler-Detect/master.svg?style=flat-square)](https://travis-ci.org/JayBizzle/Crawler-Detect) [![Total Downloads](https://img.shields.io/packagist/dt/JayBizzle/Crawler-Detect.svg?style=flat-square)](https://packagist.org/packages/jaybizzle/crawler-detect)
[![Scrutinizer Code Quality](https://img.shields.io/scrutinizer/g/JayBizzle/Crawler-Detect.svg?style=flat-square)](https://scrutinizer-ci.com/g/JayBizzle/Crawler-Detect/?branch=master) [![MIT](https://img.shields.io/badge/license-MIT-ff69b4.svg?style=flat-square)](https://github.com/JayBizzle/Crawler-Detect) [![Version](https://img.shields.io/packagist/v/jaybizzle/Crawler-Detect.svg?style=flat-square)](https://packagist.org/packages/jaybizzle/crawler-detect) [![StyleCI](https://styleci.io/repos/32755917/shield)](https://styleci.io/repos/32755917)

CrawlerDetect is a PHP class for detecting bots/crawlers/spiders via the user agent. Currently able to detect over 360 bots/spiders/crawlers.

### Installation
Run `composer require jaybizzle/crawler-detect 1.*` or add `"jaybizzle/crawler-detect" :"1.*"` to your `composer.json`.

### Usage
```PHP
use Jaybizzle\CrawlerDetect\CrawlerDetect;

$CrawlerDetect = new CrawlerDetect;

// Check the user agent of the current 'visitor'
if($CrawlerDetect->isCrawler()) {
	// true if crawler user agent detected
}

// Pass a user agent as a string
if($CrawlerDetect->isCrawler('Mozilla/5.0 (compatible; Sosospider/2.0; +http://help.soso.com/webspider.htm)')) {
	// true if crawler user agent detected
}

// Output which regex rules matched (if any)
var_dump($CrawlerDetect->getMatches());
```

### Contributing
If you find a bot/spider/crawler user agent that CrawlerDetect fails to detect, please submit a pull request with with the regex pattern added to the `$crawlers` array in `CrawlerDetect.php` and add the failing user agent to `tests/crawlers.txt`.

Failing that, just create an issue with the user agent you have found, and we'll take it from there :)

### Laravel Package
If you would like to use this with Laravel 5, please see [Laravel-Crawler-Detect](https://github.com/JayBizzle/Laravel-Crawler-Detect)

### Changelog
**v1.0.8**
 - Added [''bl.uk_lddc_bot','](http://www.bl.uk/aboutus/legaldeposit/websites/websites/faqswebmaster/)
 - Added ['classbot'](http://allclasses.com)
 - Added ['CoPubbot'](http://www.copub.com/bot.php)
 - Added ['Domain Re-Animator Bot'](http://domainreanimator.com)
 - Added ['Healthbot'](http://HealthHaven.com)
 - Added ['IstellaBot'](http://www.tiscali.it/)
 - Added ['LinkpadBot'](http://www.linkpad.ru)
 - Added ['lufsbot'](http://www.lufs.org/bot.html)
 - Added ['PaperLiBot'](http://support.paper.li/entries/20023257-what-is-paper-li)
 - Added ['Plukkie'](http://www.botje.com/plukkie.htm)
 - Added ['SearchmetricsBot'](http://www.searchmetrics.com/en/searchmetrics-bot/)
 - Added 'TrueBot'
 - Added ['UnisterBot'](http://www.unister.de/)
 - Added ['YioopBot'](http://173.13.143.74/bot.php)
 - Added 'Insitesbot'
 - Added 'xintellibot'
 - Added ['NerdyBot'](http://nerdybot.com/)
 - Added ['NextGenSearchBot'](http://www.zoominfo.com/About/misc/NextGenSearchBot.aspx)
 - Added ['ScreenerBot'](http://www.ScreenerBot.com)
 - Added ['ShowyouBot'](http://showyou.com/crawler)

**v1.0.7**
 - Added ['SurdotlyBot'](http://sur.ly/bot.html)
 - Added ['AddThis'](https://www.addthis.com)
 - Tweaked some regex patterns
 - Fixed [#10](https://github.com/JayBizzle/Crawler-Detect/issues/10)

**v1.0.6**
 - Added ['findxbot'](http://www.findxbot.com)
 - Added ['SemrushBot'](http://www.semrush.com/bot.html)
 - Added ['yoozBot'](http://yooz.ir)

**v1.0.5**
 - Added ['GigablastOpenSource'](https://github.com/gigablast/open-source-search-engine)
 - Added ['MegaIndex.ru'](http://megaindex.com/crawler)
 - Added ['Pingdom.com_bot'](http://www.pingdom.com/)
 - Added ['WeSEE:Ads/PageBot'](http://www.wesee.com/bot/)

**v1.0.4**
 - Added 'CrawlBot'
 - Added ['Flamingo_SearchEngine'](http://www.flamingosearch.com/bot)
 - Added 'python-requests'
 - Added ['Seznam screenshot-generator'](http://fulltext.sblog.cz/screenshot/)
 - Added ['SklikBot'](http://napoveda.sklik.cz/)
 - Added ['trendictionbot'](http://www.trendiction.de/bot)

**v1.0.3**
 - Added ['BUbiNG'](http://law.di.unimi.it/BUbiNG.html)
 - Added ['Qwantify'](https://www.qwant.com/)
 - Added ['archive.org_bot'](http://www.archive.org/details/archive.org_bot)
 - Added ['Applebot'](http://www.apple.com/go/applebot)
 - Added ['TweetmemeBot'](http://datasift.com/bot.html)

**v1.0.2**
 - Added ['AbiLogicBot'](http://www.abilogic.com/bot.html)
 - Added ['Link Valet'](http://www.htmlhelp.com/tools/valet/)
 - Added ['Mrcgiguy'](http://www.w3dir.com/cgi-bin)
 - Added ['LinkExaminer'](http://www.analogx.com/contents/download/network/lnkexam/Freeware.htm)
 - Added ['LinksManager.com_bot'](http://www.linksmanager.com/)
 - Added ['Notifixious'](http://notifixio.us)
 - Added ['online link validator'](http://www.dead-links.com/)
 - Added ['Ploetz + Zeller'](http://www.ploetz-zeller.de)
 - Added ['InfoWizards Reciprocal Link System PRO'](http://www.infowizards.com)
 - Added REL Link Checker
 - Added ['SiteBar'](http://sitebar.org/)
 - Added ['Vivante Link Checker'](http://www.vivante.com)

**v1.0.1**
 - Added ['Yahoo Link Preview'](https://help.yahoo.com/kb/mail/yahoo-link-preview-SLN23615.html) bot

_Parts of this class are based on the brilliant [MobileDetect](https://github.com/serbanghita/Mobile-Detect)_
