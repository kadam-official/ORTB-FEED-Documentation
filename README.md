## **APP (RTB)**
### **BANNER**



|Attribute|Description|Using|Always passed|
| :- | :-: | :-: | :- |
|id|Unique ID of the bid request, provided by the exchange||Yes|
|at|Auction type. For the first price auction at=1||Yes|
|cur|<p>Auction currency. Valid values: RUB - Russian ruble;</p><p>USD - American dollar</p>||Yes|
|tmax|Maximum time in milliseconds to submit a bid to avoid timeout|Recommended 150-300 ms|Yes|
|imp|Representing the impressions offered|Used to select materials that are relevant to the requirements|Yes|
||id|A unique identifier for this impression||Yes|
||secure|Connection type|<p>Possible choices:</p><p>0 — non-secure (HTTP); 1 — secure (HTTPS)</p>||
||bidfloor|Minimum bid for this impression|||
||bidfloorcur|Impression value currency|||
||format|Array of Format objects representing the banner sizes permitted. If none are specified, then use of the h and w attributes is highly recommended|||
||battr|Blocked creative attributes||No|
||api|List of supported API frameworks for this impression|||
||banner|Parameter for Banner format||Yes|
|||w|Width in device independent pixels (DIPS)||Yes|
|||h|Height in device independent pixels (DIPS)||Yes|
|app|Details about the publisher's app||Yes|
||id|Application ID on the exchange|For the uniqueness of the site, the creation of black- or white-lists|Yes|
||domain|Domain of the application, used for advertiser side blocking. For example, “ mygame.foo.com”|For internal classification of domains in the Kadam system|Yes|
||name|Application name (may be aliased at publisher's request)|||
||bundle|<p>A platform-specific application identifier intended to be unique to the app and independent of the exchange. Examples:</p><p></p><p>IOS - 1453331063</p><p></p><p>Android - com.foo.mygame</p>|||
||storeurl|App store URL for an installed app|||
||cat|IAB site category|You don't have to pass it if the "domain" parameter is filled in, because Kadam classifies domains internally|Recommended|
||ver|Application version|||
||publisher|Details about the Publisher object of the app|||
|||id|Unique ID of the application owner|||
|||name|Publisher name|||
||ext|Additional application parameters|||
|user|Details about the human user of the device||Yes|
||ext|Additional user parameters|||
|||consent|The web-safe base64-encoded IAB Transparency and Consent Framework (TCF) v2 consent string fetched from the publisher's IAB Consent Management Platform (CMP). The structure of the string is defined by the IAB TCF v2|This field will be populated if the publisher has integrated with a CMP for TCF v2 and that CMP indicates that GDPR applies to this ad request and provides a valid consent string||
|regs|Specifies any industry, legal, or governmental regulations in force for this request|||
||coppa|Flag indicating if this request is subject to the COPPA regulations established by the USA FTC|<p>0 - no;</p><p></p><p>1 - yes</p>||
||ext|Additional regs parameters|||
|||gdpr|<p>This field will be set to true in either of the two following cases:</p><p></p><p>1. Google receives a valid IAB Transparency and Consent Framework (TCF) v2 consent string and the Consent Management Platform indicates that GDPR applies to this ad request.</p><p>2. Google does not receive an IAB TCF v2 consent string and, based on information available to Google, this impression will serve to an EEA user.</p>|||
|device|Details about the user's device to which the impression will be delivered||Yes|
||geo|Geolocation of the user device|||
|||type|Source of location data|||
|||country|Standard "ISO3" or "ISO2" country code|||
|||region|Region name|||
|||city|City name|||
|||zip|Zip/postal code|||
||dnt|Standard "Do Not Track" flag as set in the header by the browser|<p>0 - tracking is unrestricted;</p><p></p><p>1 - do not track</p>||
||lmt|"Limit Ad Tracking" signal commercially endorsed|0 - tracking is unrestricted; 1 - tracking must be limited per commercial guidelines||
||ip|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ipv6|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
||devicetype|The general type of device|||
||make|Device make|||
||model|Device model|||
||os|Device operating system|||
||osv|Device operating system version|||
||carrier|Carrier or ISP|||
||js|Support for JavaScript, where 0 - no, 1 - yes|||
||language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
||connectiontype|Network connection type|||
||ext|Additional user device parameters|||

**Example Request:**

{

`  `"id": "b2b765f061f361a7",

`  `"imp": [

`    `{

`      `"id": "1",

`      `"banner": {

`        `"format": [

`          `{

`            `"w": 320,

`            `"h": 50

`          `}

`        `],

`        `"w": 320,

`        `"h": 50,

`        `"battr": [

`          `6,

`          `7

`        `],

`        `"api": [

`          `3,

`          `5,

`          `7

`        `]

`      `},

`      `"bidfloor": 0.004724,

`      `"bidfloorcur": "USD",

`      `"secure": 1

`    `}

`  `],

`  `"app": {

`    `"id": "208212064",

`    `"name": "iSound : Cloud Music Player",

`    `"bundle": "1453331063",

`    `"domain": "raw.githubusercontent.com",

`    `"storeurl": "https://apps.apple.com/us/app/isound-cloud-music-player/id1453331063?uo=4",

`    `"cat": [

`      `"IAB1-6"

`    `],

`    `"ver": "3.1",

`    `"publisher": {

`      `"id": "102046074",

`      `"name": "Busra Yildiz"

`    `}

`  `},

`  `"device": {

`    `"ua": "Mozilla/5.0 (iPhone; CPU iPhone OS 14\_6 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E148",

`    `"geo": {

`      `"type": 2,

`      `"country": "DEU",

`      `"region": "NW",

`      `"city": "Bielefeld",

`      `"zip": "33602"

`    `},

`    `"dnt": 1,

`    `"lmt": 1,

`    `"ip": "37.201.146.143",

`    `"devicetype": 4,

`    `"make": "apple",

`    `"model": "iphone",

`    `"os": "iOS",

`    `"osv": "14",

`    `"js": 1,

`    `"language": "en",

`    `"carrier": "Vodafone Germany Cable",

`    `"connectiontype": 2

`  `},

`  `"user": {

`    `"ext": {

`      `"consent": "1"

`    `}

`  `},

`  `"at": 1,

`  `"tmax": 586,

`  `"cur": [

`    `"USD"

`  `],

`  `"regs": {

`    `"coppa": 0,

`    `"ext": {

`      `"gdpr": 1

`    `}

`  `}

}

**Example Response:**

{

`  `"cur": "USD",

`  `"id": "th8qj7l3tp5sbjg99t7",

`  `"seatbid": [

`    `{

`      `"bid": [

`        `{

`          `"id": "1",

`          `"adid": "TPL35\_AD4921726",

`          `"crid": "TPL35\_AD4921726",

`          `"cid": "509290",

`          `"impid": "1",

`          `"price": 0.014145912714302543,

`          `"lurl": "https://s.viicoat.com/lurl/830/nnbqypdkjerv4xtfhm5viiy2hy2qc4a5avceq72ymjewgyaokho72rlp6dy55d5ivxd3nfrtm3huswkufdvfiycibgaptd4ir7l7vneyheq77i4mzbgrdueixdjtgmpngpoe4kljv3fpqubainmdevspjnqva6auci4qd3jtezcteykqpbkfeofzk2zfotwdmbnoqvpzvba5sm54yvknsuocl6jdtn63tzkiesqys43g5bzzqwd7w2mxjlffnhkvki4esko2k5n3wycjqvksx7yhko7vi7kayjwnavlnrbegvcsxigbwau5ikvooashq5k2irmu6v6d2wu6yjdyovneiwkpk7b5lkpieq2gak5gb4mqu6flcgbkdx2isnktuznjhwaibpt4wxex4y2hztl4hvowttc3lffpu6s3bkb4fiutybbldraimyom5yryfki4es2jsk27xjkksdwdfaoernmz3mtmczguzwuv2hjbzsmcxyvegs2kjmiyfykypkthey2gbkp6fl6r3jlmtc47xjccniweukhtm2spckwf3h65gpoevcmu6jihkmtgvrtup6u6qhrhw2q77sbfgfqd43bikatlisjjntwv3257pyvrz7fwytrwbxsw2nqkw5i6otq53sk33jhvpq5kq====?1=1&data[]=16267695581629189819560392&v[]=1326260065&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}&total=1.051696270431351&loss=${AUCTION\_LOSS}",

`          `"adomain": [

`            `"oleg-maltsev.ru"

`          `],

`          `"cat": [

`            `"IAB3-10"

`          `],

`          `"adm": "<div id=\"EpLvPrThwzjHXYMe\"><a href=\"https://s.viicoat.com/h/nodxsxhg65nhtcogyg6j3l4hvowts2osulmlrb4x5f5hyuyizfvquuqpoquvgkgcyprm4322gpluvx2w2bk2xpkb3ez6nwcj3fi7rvgsxd465ufhqffksulwrrjtxklihs7e5uvzwk723lohw2ldhjso2k43fp5nvxd3nfrt2zg6xs6zxswk3r5wsyz4mtkkyfjhf7sqhintzasulpzwgunvkzjdr2jj2jkfni3dooefmuoajnglevnkz5a5q64k2ymos2xwv3k32yx5pnpikg3vvey4rixt4zl2uv2uhq4mb3kxjsjwfxvczwcddklkxzkkosdaub5vlur4374orukj3nsvc2qnlldpxrjqi2s4c7sipf2fq6cihe4a4rjl3nnrbuctsbemfis675fjrvlqxrjzhwlbwjke5q3dv3fpquefjmipkgdvrzrzzfu5nxyexqruqngtfjq6ikyvacsczihkmtmp4pfkbcuf2comsm2mprawwpqqnuqfg6yflrqsow6t764jppf7zoe7qv3hzoi3z6k7aly6degrkal4xy74fi2nhgvfqxektmfutzivuus2xreftnsxm5evdrxjr3kt4432hjlvpyhrlbmk3vzqobutevspjnqvboa=?u=https%3A%2F%2Foleg-maltsev.ru%2F%3Futm\_source%3Dkad\_tizer%26utm\_campaign%3D509290%26utm\_medium%3D1380663657990203%26utm\_content%3D4921726\" trackerlink=\"https://s.viicoat.com/c/nodxsxhg65nhtcogyg6j3l4hvowts2osulmlrb4x5f5hyuyizfvquuqpoquvgkgcyprm4322gpluvx2w2bk2xpkb3ez6nwcj3fi7rvgsxd465ufhqffksulwrrjtxklihs7e5uvzwk723lohw2ldhjso2k43fp5nvxd3nfrt2zg6xs6zxswk3r5wsyz4mtkkyfjhf7sqhintzasulpzwgunvkzjdr2jj2jkfni3dooefmuoajnglevnkz5a5q64k2ymos2xwv3k32yx5pnpikg3vvey4rixt4zl2uv2uhq4mb3kxjsjwfxvczwcddklkxzkkosdaub5vlur4374orukj3nsvc2qnlldpxrjqi2s4c7sipf2fq6cihe4a4rjl3nnrbuctsbemfis675fjrvlqxrjzhwlbwjke5q3dv3fpquefjmipkgdvrzrzzfu5nxyexqruqngtfjq6ikyvacsczihkmtmp4pfkbcuf2comsm2mprawwpqqnuqfg6yflrqsow6t764jppf7zoe7qv3hzoi3z6k7aly6degrkal4xy74fi2nhgvfqxektmfutzivuus2xreftnsxm5evdrxjr3kt4432hjlvpyhrlbmk3vzqobutevspjnqvboa=?u=https%3A%2F%2Foleg-maltsev.ru%2F%3Futm\_source%3Dkad\_tizer%26utm\_campaign%3D509290%26utm\_medium%3D1380663657990203%26utm\_content%3D4921726\" data-set=\"href\" target=\"\_blank\" class=\"k-bloc wzuRrdoPaKupOzsD\"><div class=\"k-bloc\_\_age\">12+</div><div class=\"k-bloc\_\_img\" style=\"background-image: url('https://i.cdnkimg.com/auto/300x194/image/tesr/1726/726/rect\_60e3140b614cat1625494539r8069.jpg');\"></div><div class=\"k-bloc\_\_btnwrap\"><div class=\"k-bloc\_\_btn\"><div>Выведи компанию на новый уровень! Комплексный пиар Олега Мальцева</div><div class=\"k-bloc\_\_domain\">oleg-maltsev.ru</div><div class=\"k-bloc\_\_disclaimer\"></div></div><div class=\"k-bloc\_\_arrow\"><svg width=\"30\" height=\"18\" viewBox=\"0 0 30 18\" fill=\"none\" xmlns=\"http://www.w3.org/2000/svg\"><path d=\"M3 9L27 9\" stroke=\"white\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\"/><path d=\"M22.5 4.5L27 9L22.5 13.5\" stroke=\"white\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\"/></svg></div></div></a></div><style>#EpLvPrThwzjHXYMe \* {box-sizing: border-box;font-family: Arial, sans-serif}#EpLvPrThwzjHXYMe .k-bloc {position: relative;width: 300px;height: 250px;display: block;background-color: #fff}#EpLvPrThwzjHXYMe .k-bloc:hover .k-bloc\_\_btnwrap {bottom: 32px}#EpLvPrThwzjHXYMe .k-bloc\_\_img {height: 194px;width: 300px;background-position: center;background-repeat: no-repeat;background-size: cover;overflow: hidden;}#EpLvPrThwzjHXYMe .k-bloc\_\_text {font-weight: 400;position: absolute;bottom: 5px;left: 18px;max-width: 265px;font-size: 8px;line-height: 9px;color: #b4b4b4;height: 18px;overflow: hidden}#EpLvPrThwzjHXYMe .k-bloc\_\_btnwrap {position: absolute;bottom: 27px;left: 8px;display: flex;justify-content: space-between;align-items: flex-end;width: 284px;box-sizing: border-box;text-decoration: none;transition: all .2s;background-color: #4f4f4f;box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);border-radius: 5px;padding: 12px 8px 12px 12px}#EpLvPrThwzjHXYMe .k-bloc\_\_btn {width: 220px;font-size: 14px;line-height: 16px;color: #fff;font-weight: 700;margin-right: 4px;box-sizing: border-box;transition: all .2s}#EpLvPrThwzjHXYMe .k-bloc\_\_arrow {margin-bottom: -4px;width: 30px;height: 18px;display: flex;justify-content: center;align-items: center;box-sizing: border-box;transition: all .2s}#EpLvPrThwzjHXYMe .k-bloc\_\_arrow svg {width: 100%;height: 100%}#EpLvPrThwzjHXYMe .k-bloc\_\_domain {font-size: 12px;line-height: 14px;color: #69c0ff;margin-top: 8px;margin-bottom: 3px;}#EpLvPrThwzjHXYMe .k-bloc\_\_age {width: 24px;height: 24px;left: 8px;top: 8px;position: absolute;display: flex;justify-content: center;align-items: center;font-weight: bold;font-size: 10px;line-height: 12px;color: gray;background-color: #fcfcfc;opacity: .75;border-radius: 2px}#EpLvPrThwzjHXYMe .k-bloc\_\_disclaimer {font-size: 7px;line-height: 8px;color: #B4B4B4;}</style>"

`        `}

`      `]

`    `}

`  `]

}

### **NATIVE**


|Attribute|Description|Using|Always passed|
| :- | :-: | :-: | :- |
|id|Unique ID of the bid request, provided by the exchange||Yes|
|at|Auction type. For the first price auction at=1||Yes|
|cur|<p>Auction currency. Valid values: RUB - Russian ruble;</p><p>USD - American dollar</p>||Yes|
|tmax|Maximum time in milliseconds to submit a bid to avoid timeout|Recommended 150-300 ms|Yes|
|imp|Representing the impressions offered|Used to select materials that are relevant to the requirements|Yes|
||id|A unique identifier for this impression||Yes|
||tagid|Identifier for specific ad placement or ad tag that was used to initiate the auction||No|
||bidfloor|Minimum bid for this impression|||
||bidfloorcur|Impression value currency|||
||native|A Native object||Yes|
|||request|Request payload complying with the Native Ad Specification|<p>Options:</p><p>openrtb.native.string - JSON query text; openrtb.native - the query is a JSON object.</p><p>It is similar to openrtb.native.string, only in case of string query is encoded to JSON text</p>|Yes|
|||ver|Version of the Native Ad Specification to which request complies. RECOMMENDED by the OpenRTB specification|||
||secure|Connection type|<p>Possible choices:</p><p>0 — non-secure (HTTP); 1 — secure (HTTPS)</p>||
||battr|Blocked creative attributes||No|
|site|Details about the publisher's website||Yes|
||id|Site ID on the exchange|For the uniqueness of the site, the creation of black- or white-lists|Yes|
||domain|Domain of the site|For internal classification of domains in the Kadam system|Yes|
||page|URL of the page where the impression will be shown|||
||name|Stream name or its unique identifier|||
||content|Details about the Content within the site|||
||cat|IAB site category|You don't have to pass it if the "domain" parameter is filled in, because Kadam classifies domains internally|Recommended|
|user|Details about the human user of the device||Yes|
||id|Unique user ID in your system|Kadam generates on its own if not filled in||
|bcat|Blocked advertiser categories using the IAB content categories|||
|regs|Specifies any industry, legal, or governmental regulations in force for this request|||
| :- | :- | :- | :- |
||coppa|Flag indicating if this request is subject to the COPPA regulations established by the USA FTC|<p>0 - no;</p><p></p><p>1 - yes</p>||
||ext|Additional regs parameters|||
|||gdpr|<p>This field will be set to true in either of the two following cases:</p><p></p><p>1. Google receives a valid IAB Transparency and Consent Framework (TCF) v2 consent string and the Consent Management Platform indicates that GDPR applies to this ad request.</p><p>2. Google does not receive an IAB TCF v2 consent string and, based on information available to Google, this impression will serve to an EEA user.</p>|||
|device|Details about the user's device to which the impression will be delivered||Yes|
||geo|Geolocation of the user device|||
|||country|Standard "ISO3" or "ISO2" country code|||
|||lat|Latitude from -90.0 to +90.0, where negative is south|||
|||lon|Longitude from -180.0 to +180.0, where negative is west|||
|||type|Source of location data|||
||dnt|Standard "Do Not Track" flag as set in the header by the browser|<p>0 - tracking is unrestricted;</p><p></p><p>1 - do not track</p>||
||lmt|"Limit Ad Tracking" signal commercially endorsed|0 - tracking is unrestricted; 1 - tracking must be limited per commercial guidelines||
||ip|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ipv6|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
||devicetype|The general type of device|||
||make|Device make|||
||model|Device model|||
||os|Device operating system|||
||osv|Device operating system version|||
||carrier|Carrier or ISP|||
||js|Support for JavaScript, where 0 - no, 1 - yes|||
||language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
||connectiontype|Network connection type|||
||ext|Additional user device parameters|||

**Example Request:**

{

`  `"at": 2,

`  `"cur": [

`    `"USD"

`  `],

`  `"device": {

`    `"devicetype": 4,

`    `"geo": {

`      `"country": "UKR",

`      `"lat": 50.4522,

`      `"lon": 30.5287,

`      `"type": 2

`    `},

`    `"ip": "46.211.72.11",

`    `"js": 1,

`    `"ua": "Mozilla/5.0 (iPhone; CPU iPhone OS 14\_6 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/14.1.1 Mobile/15E148 Safari/604.1",

`    `"language": "uk"

`  `},

`  `"id": "e646e381-6bb1-47f5-88ce-112faf746235",

`  `"imp": [

`    `{

`      `"tagid": "5803",

`      `"bidfloor": 0.01,

`      `"bidfloorcur": "USD",

`      `"id": "fec7a9a871",

`      `"native": {

`        `"request": "{\"ver\":\"1.2\",\"plcmttype\":4,\"plcmtcnt\":2,\"assets\":[{\"id\":1,\"required\":1,\"title\":{\"len\":100}},{\"id\":2,\"required\":1,\"img\":{\"type\":3,\"w\":400,\"h\":400}},{\"id\":3,\"data\":{\"type\":2,\"len\":200}}],\"eventtrackers\":[{\"event\":1,\"methods\":[1]}]}",

`        `"ver": "1.2"

`      `},

`      `"secure": 1

`    `}

`  `],

`  `"site": {

`    `"cat": [

`      `"IAB12",

`      `"IAB12-1",

`      `"IAB12-2",

`      `"IAB12-3"

`    `],

`    `"domain": "www.unian.ua",

`    `"id": "1553",

`    `"name": "www.unian.ua",

`    `"page": "https://www.unian.ua/",

`    `"Content": {}

`  `},

`  `"tmax": 500,

`  `"user": {

`    `"id": "6f1ab8ca-0487-44a5-808f-d2f4f0c84047"

`  `},

`  `"ext": {

`    `"audit": {

`      `"id": 0

`    `},

`    `"shown": null,

`    `"reload\_count": 0

`  `},

`  `"bcat": [

`    `"IAB25-3",

`    `"IAB8-5",

`    `"IAB7-5",

`    `"IAB7-6",

`    `"IAB7-19",

`    `"IAB7-44",

`    `"IAB7-31",

`    `"IAB7-14",

`    `"IAB7-38",

`    `"IAB7-42",

`    `"IAB7-20",

`    `"IAB7-4",

`    `"IAB7-17",

`    `"IAB9-9",

`    `"IAB7-16",

`    `"IAB7-15",

`    `"IAB7-11",

`    `"IAB17-18",

`    `"IAB11-4",

`    `"IAB25-5",

`    `"IAB7",

`    `"IAB7-18",

`    `"IAB9-7",

`    `"IAB7-26"

`  `]

}

**Example Response:**

{

`  `"cur": "USD",

`  `"id": "69fe4946-eb8a-4d80-92ed-a078e6d128a4",

`  `"seatbid": [

`    `{

`      `"bid": [

`        `{

`          `"id": "1",

`          `"adid": "4904435",

`          `"crid": "4904435",

`          `"cid": "436414",

`          `"impid": "e96a25ea74",

`          `"price": 0.010579906888306142,

`          `"nurl": "https://s.viicoat.com/nurl/799/nn2e43julv6vabtamixag2azpftfy4kzd5xx2lqfpumwiziafrpvmz35omagi2stmyaxsxigmv5fhpu6nn2lzg5bzqzx5g7ov2ph6zgshjyw2ywjjejwemej4ho4dovo5wakgsqjqtxi5vj6hhuzfm53jym7g4o6kntedguz7vgvg23bpbkff6efuxbgsd2kfevaqxrlhbewsmswj65v5udzkxndsq7zgpu6storkhdikseajditvfsoxdfpw6uzkpjr57aiqnho2q6ji6gfhw2nrqztakonl24hsxvphhqictdmyjerhb2pnd5ds5wzgnk7ostpsb4vlgrzjc4tgwexjk7olnm2v7d3nfwnk6xuvpxfwwnk7r5ws3gvpj2kmcrhsvyhnmg6ambhoja3n4yiwfwzes3km4cqx63dsdz4zkoaw2lm3kkorfruw4kuki4itjp6uzyau2uh3ncltewmkzrvmt2lmfihrjdn6bfqzycuj6jwgumyk2qphu5rgg7e2surkj454ujqfvpaknlzfjkgjwcxfcieu2uckvvjwyvozxmiip4uni4ic3dxsfj7pdwd2jg6wnsrjprl4uiikni2qtocgdhewswbkswmfcf7j7atmv77j6h7hehrupj7a24kkkh4b6nlqcv23r5wna======?1=1&data[]=16267702601928352117733179&v[]=499249867&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}",

`          `"lurl": "https://s.viicoat.com/lurl/799/nn2e43julv6vabtamixag2azpftfy4kzd5xx2lqfpumwiziafrpvmz35omagi2stmyaxsxigmv5fhpu6nn2lzg5bzqzx5g7ov2ph6zgshjyw2ywjjejwemej4ho4dovo5wakgsqjqtxi5vj6hhuzfm53jym7g4o6kntedguz7vgvg23bpbkff6efuxbgsd2kfevaqxrlhbewsmswj65v5udzkxndsq7zgpu6storkhdikseajditvfsoxdfpw6uzkpjr57aiqnho2q6ji6gfhw2nrqztakonl24hsxvphhqictdmyjerhb2pnd5ds5wzgnk7ostpsb4vlgrzjc4tgwexjk7olnm2v7d3nfwnk6xuvpxfwwnk7r5ws3gvpj2kmcrhsvyhnmg6ambhoja3n4yiwfwzes3km4cqx63dsdz4zkoaw2lm3kkorfruw4kuki4itjp6uzyau2uh3ncltewmkzrvmt2lmfihrjdn6bfqzycuj6jwgumyk2qphu5rgg7e2surkj454ujqfvpaknlzfjkgjwcxfcieu2uckvvjwyvozxmiip4uni4ic3dxsfj7pdwd2jg6wnsrjprl4uiikni2qtocgdhewswbkswmfcf7j7atmv77j6h7hehrupj7a24kkkh4b6nlqcv23r5wna======?1=1&data[]=16267702601928352117733179&v[]=499249867&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}&loss=${AUCTION\_LOSS}",

`          `"adomain": [

`            `"news-fancy.com"

`          `],

`          `"cat": [

`            `"IAB9"

`          `],

`          `"adm": "{\"native\":{\"ver\":\"1.1\",\"link\":{\"url\":\"https://s.viicoat.com/h/nonxsxen6znhtxhvu7xgasfm6go7mtsj3t22p3uqxpavm6r3phuta3slbnpbq6yeq2xjh3ruhyvngygpp36fhb6lmgbfpvg5mpuhtahx66dy5d6ssjp2sulwqrjtteligo3e4rmjkgt6dh7wwslm3knqjkivdj7bt73ljfwnvgyevyksxdp4vq5rs3g2tmck6fjht5cqhhrwwmadb35wgwwakzj7ks3jgj3a5o3dkoafm54yjklypwuzjtgfg4udoecis2v5rtpkczmcpnjvnemwnbbfctetmlti5chog6uwvgkuu5egbid3kxjdzhp75diutw3fkfvagwwl4lbdarxrtj5uq6lulb4eqojybzcsxwkycaxpuopwz42omtxu4nmjavpntzh6smcxy5ezf66tk3xtvir6u5wiusoholqwxgr2vjw6ovhgumpwvhkwedxx4vockt37jnu7zsd45hymon7vy23ykuzb23deaexuiabvfixuyzcjme2bkkc5ajswekacgffdkzibpboauzjjloiol55nuh7znp66k5t4xqnvrriqfsuc6pvfkf6l4p6cunhkz37kxtfjwc2j4uk2kfnjwqczjb7e265vy2rngvacljqtgtxq5vtxbr6wliaus2jss2bypepp?u=https%3A%2F%2Fnews-fancy.com%2F52995-u-nekotoryx-zhenshchin-nesprosta-shirokie-bedra-axnete.html%3Fsource%3D392%26id%3D4904435%26site\_id%3D1380295462490606%26mark3%3D321375%26tid%3D59198\"},\"assets\":[{\"id\":1,\"required\":1,\"title\":{\"text\":\"Что означают широкие бедра у женщин? То, чего мужчины не знают\"}},{\"id\":2,\"required\":1,\"img\":{\"w\":400,\"h\":400,\"url\":\"https://i.cdnkimg.com/auto/400/image/tesr/4435/435/60d4448055998t1624523904r3436.jpg\"}}]}}"

`        `}

`      `]

`    `}

`  `]

}

### **VIDEO**


|Attribute|Description|Using|Always passed|
| :- | :-: | :-: | :- |
|id|Unique ID of the bid request, provided by the exchange||Yes|
|at|Auction type. For the first price auction at=1||Yes|
|cur|<p>Auction currency. Valid values: RUB - Russian ruble;</p><p>USD - American dollar</p>||Yes|
|tmax|Maximum time in milliseconds to submit a bid to avoid timeout|Recommended 150-300 ms|Yes|
|imp|Representing the impressions offered|Used to select materials that are relevant to the requirements|Yes|
||id|A unique identifier for this impression||Yes|
||video|Parameter for Video format||Yes|
|||mimes|Whitelist of content MIME types supported|Examples: "image/jpg", "image/gif" и "application/x-shockwave-flash".||
|||maxdurati on|Maximum video ad duration in seconds|||
|||minduration|Minimum video ad duration in seconds|||
|||protocols|Array of supported video bid response protocols. At least one supported protocol must be specified|<p>Examples: VAST\_1\_0 = 1;</p><p>VAST\_2\_0 = 2;</p><p>VAST\_3\_0 = 3</p>|Yes|
|||w|Width of the video player in device independent pixels|||
|||h|Height of the video player in device independent pixels|||
|||startdelay|Indicates the start delay in seconds for pre-roll, mid-roll, or post-roll ad placements|||
|||linearity|Indicates if the impression must be linear, nonlinear, etc. If none specified, assume all are allowed|<p>Examples:</p><p></p><p>LINEAR = 1: Linear/In-stream; NON\_LINEAR = 2: Non-linear/Overlay</p>||
|||pos|Ad position on screen|||
|||api|List of supported API frameworks for this impression|||
||instl|<p>1 - the ad is interstitial or full screen;</p><p></p><p>0 - not interstitial</p>|||
||tagid|Identifier for specific ad placement or ad tag that was used to initiate the auction|||
| :- | :- | :- | :- | :- |
||bidfloor|Minimum bid for this impression|||
||bidfloorcur|Impression value currency|||
||secure|Connection type|<p>Possible choices:</p><p>0 — non-secure (HTTP); 1 — secure (HTTPS)</p>||
||battr|Blocked creative attributes||No|
|site|Details about the publisher's website||Yes|
||id|Site ID on the exchange|For the uniqueness of the site, the creation of black- or white-lists|Yes|
||domain|Domain of the site|For internal classification of domains in the Kadam system|Yes|
||page|URL of the page where the impression will be shown|||
||name|Stream name or its unique identifier|||
||content|Details about the Content within the site|||
||cat|IAB site category|You don't have to pass it if the "domain" parameter is filled in, because Kadam classifies domains internally|Recommended|
||publisher|Details about the Publisher object of the site|||
|||id|Unique ID of the site owner|||
|user|Details about the human user of the device||Yes|
||id|Unique user ID in your system|Kadam generates on its own if not filled in||
|bcat|Blocked advertiser categories using the IAB content categories|||
|regs|Specifies any industry, legal, or governmental regulations in force for this request|||
||coppa|Flag indicating if this request is subject to the COPPA regulations established by the USA FTC|<p>0 - no;</p><p></p><p>1 - yes</p>||
||ext|Additional regs parameters|||
|||gdpr|<p>This field will be set to true in either of the two following cases:</p><p></p><p>1. Google receives a valid IAB Transparency and Consent Framework (TCF) v2 consent string and the Consent Management Platform indicates that GDPR applies to this ad request.</p><p>2. Google does not receive an IAB TCF v2 consent string and, based on information available to Google, this impression will serve to an EEA user.</p>|||
|device|Details about the user's device to which the impression will be delivered||Yes|
||geo|Geolocation of the user device|||
|||country|Standard "ISO3" or "ISO2" country code|||
||dnt|Standard "Do Not Track" flag as set in the header by the browser|<p>0 - tracking is unrestricted;</p><p></p><p>1 - do not track</p>||
||lmt|"Limit Ad Tracking" signal commercially endorsed|0 - tracking is unrestricted; 1 - tracking must be limited per commercial guidelines||
||ip|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ipv6|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
| :- | :- | :- | :- | :- |
||ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
||devicetype|The general type of device|||
||make|Device make|||
||model|Device model|||
||os|Device operating system|||
||osv|Device operating system version|||
||carrier|Carrier or ISP|||
||js|Support for JavaScript, where 0 - no, 1 - yes|||
||language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
||connectiontype|Network connection type|||
||ext|Additional user device parameters|||

**Example Request:**

{

`  `"id": "726d8755-d126-4319-a969-1e006454fda5",

`  `"imp": [

`    `{

`      `"id": "i726d8755-d126-4319-a969-1e006454fda5",

`      `"video": {

`        `"mimes": [

`          `"video/mp4"

`        `],

`        `"minduration": 1,

`        `"maxduration": 60,

`        `"protocols": [

`          `2,

`          `3,

`          `5,

`          `6

`        `],

`        `"w": 640,

`        `"h": 360,

`        `"startdelay": 0,

`        `"linearity": 1,

`        `"pos": 1,

`        `"api": [

`          `1,

`          `2

`        `]

`      `},

`      `"instl": 0,

`      `"bidfloor": 0.65,

`      `"bidfloorcur": "USD",

`      `"secure": 1

`    `}

`  `],

`  `"site": {

`    `"id": "670",

`    `"domain": "serialytut.me",

`    `"cat": [

`      `"IAB1-5"

`    `],

`    `"page": "https://gavanaplay.me/",

`    `"publisher": {

`      `"id": "694"

`    `}

`  `},

`  `"device": {

`    `"ip": "95.125.117.20",

`    `"ua": "Mozilla/5.0 (Linux; Android 9; SAMSUNG SM-A105FN) AppleWebKit/537.36 (KHTML, like Gecko) SamsungBrowser/14.2 Chrome/87.0.4280.141 Mobile Safari/537.36",

`    `"language": "ru",

`    `"geo": {

`      `"country": "ESP"

`    `}

`  `},

`  `"user": {

`    `"id": "a944913f-a3d1-44ab-837f-f97c785d237c"

`  `},

`  `"at": 2,

`  `"tmax": 300,

`  `"cur": [

`    `"USD"

`  `]

}

**Example Response:**

{

`  `"cur": "USD",

`  `"id": "726d8755-d126-4319-a969-1e006454fda5",

`  `"seatbid": [

`    `{

`      `"bid": [

`        `{

`          `"id": "1",

`          `"adid": "4924327",

`          `"crid": "4924327",

`          `"cid": "509220",

`          `"impid": "i726d8755-d126-4319-a969-1e006454fda5",

`          `"price": 0.6890557421065893,

`          `"adomain": [

`            `"brooffer.com",

`            `"fortunatenews.com"

`          `],

`          `"cat": [

`            `"IAB13-1"

`          `],

`          `"adm": "<?xml version=\"1.0\" encoding=\"UTF-8\"?><VAST version=\"3.0\"><Ad id=\"item\_0\"><InLine><AdSystem><![CDATA[KDM]]></AdSystem><AdTitle><![CDATA[Акции Tesla дают от 200% Регистрируйся и получай доход. Всему научим!]]></AdTitle><Impression><![CDATA[https://s.viicoat.com/nurl/491/nn2e6ztelryv4b3dmixvaysopftaw6cqd43xm7kypvetcyqip5oqoyrjf4agk2stmyaxwxibmr4fh7pwnn2ovxec4df2tmfutzivbahx66dw4asgo5vtdo33brhfrfnryp4j3nnt2ngdzx44slxdijwpugkkw7jmyuy4g2cql3uiztksmajhflckiazfmt3luikz42yshea5oor6ju5wwklykrjdqsljyju46sta3b4v5qrz2l4tvzso57vu7qcv3uzys2evshrutlcr7z3lebe4naawk7duxfi72x52hehzsm6cjs3gbvs2wrxlks26ryjxhy3an7efkupijbqouv7dt7hynbnlvxd3m2gsk7rz7t4gqwv23r5wndnfotvzmbjs2bywwffwsmswz5p47p2h7zidwhb2o3te3y6aw6zvfeb2mfedevspnorblhtlpo4etrus5bb22xtanrwem6ojngo7n4khq5xssvcshbewsmvgocbwgnnkkzjoas3i2jknj27c7kckxlohwzunuvcyxnrvd4sxliehsx2ugv6s4bhqppvfvecknsbfkx4lmkc5vsst4vfa6vdqoc5wfungskgdbs3ngehuythrktwfnsr4jdetnw7lsdtfnucqkoee3uowtxdifaxeplwfnehir34va===?1=1&data[]=16267883652405580382770346&v[]=4130701133&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}]]></Impression><Creatives><Creative id=\"4924327\" AdID=\"4924327\"><Linear skipoffset=\"00:00:00\"><Duration>00:00:30</Duration><TrackingEvents></TrackingEvents><VideoClicks><ClickThrough><![CDATA[https://s.viicoat.com/h/noixsxgotznhtcvsqtbjrl4hvowtsun5s6myctcb5coj7w7rvlota7stpnywqwaunvyeuon76kkmyzzydxgfhu2kyezzns2d2fizxkctqbel3f4zqhgkn3hbyvj5qsda3jl6hh6pq2c2xlohwzumev7dt7hynbnlvxd3m2fsktt6vbu3p3cfaopjnms7ytkjeqb4qvquqbfwr72uj5f4ceeyk3ddxollg6xe2w7jkow7ntbz4rvfimdjosqvh6mksttedozrkuleqzuipppyjnnnndjflw2jrfjxtjcrhhew3p7sstggpqd4kvafqqoo6x5e2w6f3jtuyuyyb5a2mvipjiuvekc6bizctzrzh3yuhskr4pcfvccivg3f5j2k7lahbvcqhhawxfmr4ne7sutm5fil424jb2ju26csmndzyuf5ik6dbudnvno3k6td5z6xlgjq7pnmbugntw5leasteu4heltskvseczlblzsaqajspztfkzazgz7qa6s6kr5ss4swgnhwyz24pnnaknk7s642dvugvtvmuxi222s35gsvfdh7fo7dsxg2tmfumaeprvx6niuzt36r5zgugvtqynnqr53bdjkh7rwfrp7ve2bwifucvto7inazb7c4diwbs7i=?u=http%3A%2F%2Fbrooffer.com%2Fclick.php%3Fkey%3Dgmaej3st93w4pd4n89s5%26cost%3D0.0%26SID%3D1358019555422776%26ID%3D4924327%26CID%3D509220%26RID%3DES%26CATID%3D1175%26SUBAGE%3D0%26LANG%3Dru%26PLTFRM%3DANDROID]]></ClickThrough></VideoClicks><MediaFiles><MediaFile delivery=\"progressive\" type=\"video/mp4\" codec=\"0\" bitrate=\"992\" width=\"1280\" height=\"720\"><![CDATA[https://i.imgkcdn.com/video/video/4327/327/60e46a79c6d22t1625582201r8751.mp4]]></MediaFile></MediaFiles></Linear></Creative></Creatives></InLine></Ad></VAST>"

`        `}

`      `]

`    `}

`  `]

}

