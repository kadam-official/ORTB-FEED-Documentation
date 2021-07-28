# ORTB-FEED-Documentation
## **CPC FEED**
### **PUSH**


|Attribute|Description|Using|Always passed|
| :- | :- | :- | :- |
|sid|Endpoint ID|Stream uniqueness in Kadam. Issued by Kadam|Yes|
|skey|API key|Issued by Kadam||
|ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
|ip|User’s IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
|ipv6|User’s IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
|uid|User ID in the SSP|For user uniqueness|Yes|
|limit|Limiting the number of creatives in a response|If there is no limit in the request and on the block, it is counted as 1 by default||
|language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
|subage / subage\_dt / s ubage0 / subage\_ts|User subscription age|If the "subage" parameter is not filled in, filled in incorrectly, or not passed, it is considered "undefined", this reduces the buyout. For the first day of subscription expected: subage=1, subage0=0, subage\_dt - actual date of subscription, subage\_ts - actual date of subscription (unixtime)|Yes|
|pid|Publisher ID|This parameter expects the ID of the publisher (site, webmaster) on the SSP|Yes|
|cat|IAB-category domain|If the domain is transferred, it is not necessary to transfer cat|No|
|page|Page domain|Expected page domain|No|


**Example Request:**

/feed

?sid=1

&skey=3azqxvgap3yNsm8X4rg9PMsgDD

&ua=Mozilla%2F5.0+%28Linux%3B+Android+9%3B+SAMSUNG+SM-A105FN%29+AppleWebKit%2F537.36+%28KHTML%2C+like+Gecko%29+SamsungBrowser%2F12.1+Chrome%2F79.0.3945.136+Mobile+Safari%2F537.36

&ip=212.95.5.236

&uid=Xef4LfyUte-tzwpV3-fMV

&limit=1

&language=en

&pid=1

&subage=2

&cat=IAB3-1

&page=kadam.net

**Example Response:**

[

`  `{

`    `"id": "5555823",

`    `"click\_url": "https://s.lalacoat.com/h/np7hsxgf7znhtwwp372gm4eqzxbippulrjkgossribafyeqhafvgf56srptfmebrzi4563e2k6z442paphs5yoxrncznnt6l4hg7xjrf6bedf2sxw5uyculsxrj4drfsqkv3bne6v542iu6byszifk5qwspk66oukd23j24wkxpusyhqpjgpqoslhnt6mtkv3fjhtgkqhbeys4vgjvpzsutj3ri7prci6jk7dluasj7ymuj3jvvdhdsm5236vgsqwi56a262kvhmwzpr4wknkpwznuzuimkd62z5yvsczc2xiksxn5kscujilyfdeknrha7ddy3ar7lfhyrzwxwdvpsosthvpasvofnsohyggqvxquzsjjwgeajll5idilbnauyrwzrxlmwfcc3gozzve2i6mpjdushbgda2z33d5v5i7efiocwdavzkhrpjq6udllwuxmxqyz3k4y5judmw7sclxp727i7k4l2jr4cteiowgftdpvzvqy2ogeybkkqkbizge72wneoxs2s3pfnr6zl5picdgtjsmygxaucui2jkp37qr725biwqnannnymi6rntuuobhos6idagtcc2rm32btjlvzj3klxlt7fdv2d2xlohjbftmxrrpmpxq6te6osyt3runrjugyciu75fkgfv5q5g6t2lmfihqvc67aekvr36cpckgury?u=https%3A%2F%2Fhl7ce.bemobtrcks.com%2Fgo%2F78602c30-54b0-4db5-bd07-3b2e3a804955%3Fcost%3D3.5%26clickid%3Dcnv4bd32b2809b6bbcfdac2ece8909839f7%26campaign\_id%3D491120%26creative\_id%3D4796823%26site\_id%3D1375589842029800%26category\_id%3D126%26country%3DRU%26browser%3DCHROME%26language%3Dru%26platform%3DANDROID%26subage%3D7%26feed%3D320279",

`    `"campaign\_id": 455520,

`    `"category": "1368",

`    `"title": "Такого вы еще не видели!",

`    `"text": "Самые милые котята",

`    `"image\_url": "https://i.lalaimg.com/auto/492x328/image/vk/6823/823/rect\_607c73884b589t1618768776r1279.png",

`    `"icon\_url": "https://s.lalacoat.com/nurl/662/nnme4yztlr7aqvzvlvgfkz2bmjvau6truwify24jzhuowviilfitubwzjy4vcgejx23othut2tk5eyby3hezfp2pdgzprdg6niuanxstmza75upsjvjx6ylykrjdqsljhyla6srjfyef4kzyjfutevspxnpna6kv3i4uh6jtrhquzukrrcue7aciwe4jmtw4ql2hvgkt4of7sc4djzfaij2hrrj66qmmgnle6kzbxb4uvlzzskv2e36cjgmir5lj7i4xnwjtkx3uuouypgwhb2cimpvfpnwgxlqilk5ny63grusxw3dlvyefvow4pnti3jlu5olakmwqofvrjmma6xey5ai3kr6eka46s25bkxsusyqffmioeouessypetejmn2hcvcshbewsms2b5nkfjkqbdo7uszjookluy2vcvk7i3ljjfutevspjoiw7mcwg7vew2pkkrhkwy4hw2o3covbnmvkmtkk5njxan3dlzyvqa3aflvwelwqk5diqsty6jkybrsaub56vn6zrnxlausmj5rfd2cq7m5os3mtzoh4yz7yprk6epfb6crotofj3fjmaue7yxf42mi=?1=1&data[]=16263451211203914908929689&v[]=3214290623&f=https%3A%2F%2Fi.cdnkimg.com%2Fauto%2F192%2Fimage%2Fvk%2F6823%2F823%2F607c73884b589t1618768776r1279.png",

`    `"cpc": 0.031595385186374184

`  `}

]

### **CLICKUNDER**



|Attribute|Description|Using|Always passed|
| :- | :- | :-: | :- |
|sid|Endpoint ID|Stream uniqueness in Kadam. Issued by Kadam|Yes|
|ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
|ip|User’s IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|


|ipv6|User’s IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
| :- | :- | :- | :- |
|uid|User ID in the SSP|For user uniqueness|Yes|
|limit|Limiting the number of creatives in a response|If there is no limit in the request and on the block, it is counted as 1 by default||
|language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
|pid|Publisher ID|This parameter expects the ID of the publisher (site, webmaster) on the SSP|Yes|
|cat|IAB-category domain|If the domain is transferred, it is not necessary to transfer cat|No|
|format|Traffic format|cu - for clickunder; pops - clickunder|Yes|
|page|Page domain|Expected page domain|No|

**Example Request:**

/feed

?sid=746

&format=cu

&ua=Mozilla%2F5.0+%28Linux%3B+Android+10%3B+SM-J600F%29+AppleWebKit%2F537.36+%28KHTML%2C+like+Gecko%29+Chrome%2F91.0.4472.88+Mobile+Safari%2F537.36

&ip=185.186.246.159

&uid=875539436

&limit=5

&language=fa-IR

&pid=316227

&page=laladan.com

**Example Response:**

{

`  `"result": {

`    `"listing": [

`      `{

`        `"url": "https://s.lalacoat.com/h/np6hsxhj6nnhthfoqdlwm4gwvso2j7w6rnkgoukribafyeqhafvgf3ojsdtfmebrzi42g3e2k6jlizxapgvmcoxrncznnt6lqhkyphjb6bedf2sxw5uyculsxrjyhu6565kl6sw2zlgjcufyjobpn2qp3nrvpuswkb3alwjqp33usyu5pjkffodwxeyfpp2jmsuhurosho55dgsxy5enno67kwjdxvohz7xuhglckn6fgupajk7mnpakvnrmk6v4ke43s2rt2zf7bz4l75jmepciporfor6cvh6xure6uvlhcm3wm4fwagd4armgaqyj6jospitg6v4x2dvxo3ath26ejtivdjnlkxiervfzkg2uuqrtcyrgcczpb5iweklyaayuanlhbmua6bzxoywvezkpgfrvskanbntxw7hbkj45yufrqhcdbr2njnqvawgrxhexnvbqih4juwmvpietxadsueykkse6mnd47blk3vf5mpqqow5wh4nzzwpyzqpy5qnvk4tllfaggzynpjiamzlzlpgktanyy3f2dvpwk5t4xdn3wvpqfyg76sikrmfut2xxsdgsxlstwuxoxh6khluhvow4osabgn2esq4rlnel2viqjnmytueuzrtwuzc4kmqpjyrvo2jliztjpbkffob7xgposdxpcfwze3q4tn3a====?u=https%3A%2F%2lalatraf.com%lalaclick.php%3Fkey%3Dxg7fkmywgliayki699r7%26cpa%3Dcnv33ffc4f3aa8a53af5a9f357e1aad9147%26COST%3D7.555E-4%26SID%3D1378493167565870%26ID%3D4940809%26CID%3D511692%26CATID%3DIAB25-4",

`        `"bid": 0.5023327916860582

`      `}

`    `]

`  `}

}

### **ON SITE PUSH (INPAGE)**


|Attribute|Description|Using|Always passed|
| :- | :- | :-: | :- |
|sid|Endpoint ID|Stream uniqueness in Kadam. Issued by Kadam|Yes|
|skey|API key|Issued by Kadam||
|ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
|ip|User’s IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
|ipv6|User’s IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
|uid|User ID in the SSP|For user uniqueness|Yes|
|limit|Limiting the number of creatives in a response|If there is no limit in the request and on the block, it is counted as 1 by default||
|language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
|pid|Publisher ID|This parameter expects the ID of the publisher (site, webmaster) on the SSP|Yes|
|cat|IAB-category domain|If the domain is transferred, it is not necessary to transfer cat|No|
|page|Page domain|Expected page domain|Yes|

**Example Request:**

/feed

?sid=1

&skey=3azqxvgap3yNsm8X4rg9PMsgDD

&ua=Mozilla%2F5.0+%28Linux%3B+Android+9%3B+SAMSUNG+SM-A105FN%29+AppleWebKit%2F537.36+%28KHTML%2C+like+Gecko%29+SamsungBrowser%2F12.1+Chrome%2F79.0.3945.136+Mobile+Safari%2F537.36

&ip=212.95.5.236

&uid=Xef4LfyUte-tzwpV3-fMV

&limit=1

&language=en

&pid=1

&cat=IAB3-1

&page=kadam.net


**Example Response:**

[

`  `{

`    `"id": "555599",

`    `"click\_url": "https://s.lalacoat.com/h/npwxsxezwznhtbnm4tngo4gpv342t74aqnkgobcrkranjurzbflhuvi7vgzzb72shjo5c2fjkxtuvwofp7sfhe55ncffpt6l4hiir4xnvuv2cmyns5ficvuykvmnashgqtfy3mu6v6d2wu6ijdtijs4nwkpk7b5lko4ex34lu2lezqksn77faoqzewbfiuptmni3kvsshdevnqsuj2zwgwhyk7vi4z7bghzpu75bkov5bjh4ic5tcwci3kovc642ahmjo2hkauuuvokt5oo27gkprey76tndmji7qufq5ke64nggjnfhgk3q66ezgs3zuwufcu3aobtbiu3iimytqnuhimes5ucvqehps2ekynekgyedj2xfggzka5cgak3zkm2euzjwbeufyctgfqwqozq6nrras7s7avth46ifmupde2vyjnuluvhmsdfffrkwa5btquhxktxsra3lwblikme4nnts2ptsqrjkydc6as4wx5pc77wljjnp6rnse7ddhqrscicmmffwkzqppvnqg33wloaltin63trjnwchp3h7dz52pqcjdnv5rhh2tmfutzisbvgqsqnqtjxcyf4ugvdqfjremyllak2j3c7gkzbe6wrzkg5ai5xx3ztgs6cuklmbrunm5ehokjvrljgmpldw?u=https%3A%2F%2Facceptww.com%2F%3Fp%3Dgu3donzxgq5gi3bpgqztqnq%26sub1%3Dcnv6d22d21d1a580cff6f801767012d5ff8",

`    `"campaign\_id": 507671,

`    `"category": "1096",

`    `"title": "Такого вы еще не видели!",

`    `"text": "Самые милые котята",

`    `"image\_url": "https://i.lalakimg.com/auto/492x328/image/vk/499/499/rect\_60daf0b6704d4t1624961206r7408.jpg",

`    `"icon\_url": "https://s.lalacoat.com/nurl/411/nnmeay3hlewvaaddlvgfk2kjmrtac4dr7hmfy26wvlj4kvaijvi3fvsodp5fgia3glm2bmgy3ckzjubfcc3ib6gon5bnn5onrnkaakwyhekgdemn4rexstsjkrjdrkjyrlehac3adadciwcbjfutevspjoiw76cvkoyeqy5ck6oh3ukr56vezaciue5jmtxixl5xvgktnuzbqc4dj3vqfmsdrrj66qmmgpmy3ps5xb4uvlzzdqjeg36cjg2qq5di7i4xnwjtkx3uuouypg2fj2cimpvfpqh57sjidk5ny63grusxyd67zeubvow4pnti3jlu5olakmwqofvrjmma6xey5ai3kr6eka46g2zramoa7uks73w2fykovmyherslmfijqbpkuz3hrharvzuxtrpmnmj2duhqtpdpa6s6af4fiuryjfu4e2mhjecie6suwi5ivz6gw2zljhvpq5k3uos6teyfprkinfueqnrqluuawvxwjq24su3z4ritb4lkrlqgdc3c6tgwbir3tlw4jesgzfsv476fvy4uvj3bw2iuvoiddzk4ephanojfflmzuhlx57cwhh4w3bnm4tnnpoojk3vdzt6qykhuq===?1=1&data[]=162635197027883121278693&v[]=1870629595&f=https%3A%2F%2Fi.cdnkimg.com%2Fauto%2F192%2Fimage%2Fvk%2F499%2F499%2F60daf0b6704d4t1624961206r7408.jpg",

`    `"cpc": 0.00027081758307758715

`  `}

]

###

### **IOS CALENDAR PUSH**


|Attribute|Description|Using|Always passed|
| :- | :- | :-: | :- |
|sid|Endpoint ID|Stream uniqueness in Kadam. Issued by Kadam|Yes|
|skey|API key|Issued by Kadam||
|ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
|ip|User’s IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
|ipv6|User’s IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|


|uid|User ID in the SSP|For user uniqueness|Yes|
| :- | :- | :- | :- |
|limit|Limiting the number of creatives in a response|If there is no limit in the request and on the block, it is counted as 1 by default||
|language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
|pid|Publisher ID|This parameter expects the ID of the publisher (site, webmaster) on the SSP|Yes|
|subage / subage\_dt / s ubage0 / subage\_ts|User subscription age|If the "subage" parameter is not filled in, filled in incorrectly, or not passed, it is considered "undefined", this reduces the buyout. For the first day of subscription expected: subage=1, subage0=0, subage\_dt - actual date of subscription, subage\_ts - actual date of subscription (unixtime)|Yes|

**Example Request:**

/feed

?sid=841

&skey=ca428563f395ec1a7a8ff64cc1b7fb3c

&ua=iOS%2F14.4+%2818D52%29+dataaccessd%2F1.0

&ip=39.45.62.161

&uid=0.00697647.1615680025292

&language=en

&subage\_dt=2021-07-10

&pid=1026013528

&limit=1

**1 Example Response:**

[

`  `{

`    `"click\_url": "https://s.lalacoat.com/h/np3hsxhw5bnhts4bz3lga4ebqpj2lchnrbkgpfdamd4fm2vyleuq2hsmdpnnbogtkricz4jtt5e6gye67zooeomp7yyo4twl4hiprrfnukmxvusxigrwb77x3x6dvolitxm4nzld2b5n5tncsskm3knqwrqma6sw6i5fdqzqkqpqbuksm2mvaocjdfz2mtkitfjf3vcr3ohc5osvshusned3sl6k4af3gfjewwtckgqfp5pk44h5evpgjgevg6ouk2b4tknvkdpu6yccbroj7k7enmri5qsupfivqsqshemwg2s4f7igwoerkp5dtsofgxte5bphlcifluuuj2jtg5jmeultkhdcgmfhwxydmn6c6ulgdjqdcdl7bqagoljpkftrsmrtlexv4b6wjvfosuvvy77tv5dl6h5r64vekk4vh4ietrv7d6y7okivfefbxgc2twonynbfcjk2mbshycdzl4fwc6l7kz7esytdbv7vcatgpv7fg2kkisc6ttu6ws5jdd76kfinjlum6bvxavg5jayyjp6ivxalnfwnvfhbhyos2qddflh544ahiskdrblurpkvcbfvtcowr7ggo2telrjsbsofgv3idtljnf4fiuuy2dyix2iodhmu4bn5osexm===?u=https%3A%2F%2Fmedical-room.site%2Fclick.php%3Fkey%3Dc3ocgvxj64wn27evtfx6%26click\_id%3Dcnved6a226153d06b4c56e21bd07afaaf75%26cost%3D0.0013490979%26SID%3D1381141552589817%26ID%3D4934093%26CID%3D509656%26RID%3D223%26CATID%3DIAB25-3%26TGTXT%3D%26SUBAGE%3D6%26BID%3D321572",

`    `"nurl": "https://s.lalacoat.com/nurl/841/nnmb2nzxbyvfybbxlvgfk2klmbrac6trs2dfy24yq744suyizfvqvvs7doufmielknmj5ofvuhe2pp4u45ktva6jvg2vap6ltxsmcvrk2fhogmydi6dpf7l2jrgassljgl3nnuwyn44fkgwrjymtql2pjnqva6cuuid4s2bt3zhed4kr7d4flcciwg7ut52k7jnlqvm7vpsgx72xrttdc2nnkwjt72sv25lyfb5nnwifktgfjcvj6btw4nqg7scvkhueqz7kk7qmj2h6pk2fhf6g4cofjj2kmcrhsvyhnmg6ambhoja3n4yiwfw2qs3isjkn2sglkj5qcal47fv3rsovs2ok7b5lvu4yw2ywl5huwypq4hg6wb2yhofeqmvci7quofmktm4wix6iaj2daudykrjdqsmzbwpe2lvtkj4iyub2vfv6neotwsm27b5lvu42c2zk3rgegateje3dmcjibsjfljsmzfjxxzcrdxywvumrbcfwfdw2cordxd6huqp42t3fkruvou5ijxadb5sl6dqzb72s7i6erwjwv6mmv7er7txfbacn4ow4zevwt2xypk2t?1=1&data[]=16263414351110619727343372&v[]=3620922448",

`    `"title": "Такого вы еще не видели!",

`    `"description": "Самые милые котята",

`    `"price": 0.0009038956149015577

`  `}

]

**2 Example Response:**

[

`  `{

`    `"id": "5557371",

`    `"click\_url": "https://s.lalacoat.com/h/np6hsxgn5fnhts7urcogm4eb62k67px2rbkgovcr2b5gzuribflhuvi7slly772shjo5c2gukdtuvsw5odsfhd6tnoffpt6l4hior65gyaz2cm2ys5fgbmdzlk5dtdvsrpf3hne6v6dvlirzt2g7fjsmznr2jync4y5ns2zz6zgvhs2spidrpcclo77vit2lyeiiqvsrybfuzmsv22u4gupqk7ukb2ti6jk6vtv4wz4ymujzjcytdyxizssvvgcx3u5kc2rt2zfzfv4p75jmepcipn6f5ff7znjgrjveefiwqesib5fdcwralyziaqibjt7e5hh5k7efl6nvigathaotjtqve6o4kdr33qzq5ngre6toicivanmbw4eygtispjxebjcq4dez7tneupsi7c3zjykde2k5kazxw6crmfeg2mabfvoqmzd7pyageslfgegx6uahg57hub3idrcmth6jrshprv6qnj4priuzzjgswmgojqn65px345iwbspltycc7x6v3zfhmvrqg5muy7snpo4onj6tkqbfkyjtj2mnoztq2pmvuakjnezbm7dyulxtsmzulyhtpchpoa======?u=https%3A%2F%2Favtofun.info%takogo-vi-eshe-ne-videli",

`    `"campaign\_id": 424518,

`    `"category": "1080",

`    `"title": "Такого вы еще не видели!",

`    `"text": "Самые милые котята",

`    `"image\_url": "https://i.lalakimg.com/auto/492x328/image/vk/7371/371/rect\_60cda4dada569t1624089818r9023.jpg",

`    `"icon\_url": "https://s.lalacoat.com/nurl/870/nnmbsntfbawvwc3flvgfk2cbmnqq66drvwdvy24y6k7ygviizfvqvvs7dodvmiclgkr652ox5lq5h6s3ccg6jz6on5bnnomasnkaakwyheowd2nc4vexstsjkrjdqck2agkxac3adadciwcbjfutevspjoiw76cvkoyeqy5ck6mnozxapgtkiiprncff5d2kxksnevu7heiheddotjfgzgfgn63ttu7qfnukost7vv4q2sigohatg2p7jjroq6k2ti4urojtlcluvjulyhe25r5ws3gvpl2kw22lrjcr2begrqcxjqpdefhrkyrqkq56setku5hrkj47iufajlbtavi2das6a6vazphp227qkrvueykqpakgcc4kkyrtckjne4hmf3lnpfomo5phrjito3zjkrjdqsljgkthba3dgwvfmuxajnrnevgauxrog654kaqmg2r2mn7xguruie3ddgckc6nfkth3mj24av6l3lvwr4sv6xj4eumik7333fepgpkewstayb6nwueyjwyijcoijxevi6pek3a6xlxfuhopcy7ipsqmxtx5nm======?1=1&data[]=16268562813881280618918804&v[]=3780696939&f=https%3A%2F%2Fi.lalakimg.com%2Fauto%2F192%2Fimage%2Fvk%2F7371%2F371%2F60cda4dada569t1624089818r9553.jpg",

`    `"cpc": 0.001349156436044723

`  `},

### **NATIVE**



|Attribute|Description|Using|Always passed|
| :- | :- | :-: | :- |
|sid|Endpoint ID|Stream uniqueness in Kadam. Issued by Kadam|Yes|
|skey|API key|Issued by Kadam||
|ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
|ip|User’s IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
|ipv6|User’s IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
|uid|User ID in the SSP|For user uniqueness|Yes|
|language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
|pid|Publisher ID|This parameter expects the ID of the publisher (site, webmaster) on the SSP|Yes|
|format|Traffic format|native - native, experimental; teaser - native, experimental|Yes|
|page|Page domain|Expected page domain|Yes|

**Example Request:**

/feed

?sid=744

&skey=b1cb709d9efcd995ade4749a8eaa9f52

&ua=Mozilla%2F5.0+%28Linux%3B+Android+11%3B+SM-T500%29+AppleWebKit%2F537.36+%28KHTML%2C+like+Gecko%29+Chrome%2F91.0.4472.120+Safari%2F537.36

&ip=79.203.211.204

&uid=8b3aa564-bd47-541b-a2d6-20f67f0c37df

&language=de

&pid=93

&page=hclips.com

&format=native

**Example Response:**

[

`  `{

`    `"id": "5555670",

`    `"url": "https://s.lalacoat.com/h/npvxsxge6nnhtrfmt3ijvl4hvowts2m7zcd5jigt5f5hysqilfituftqanrabyvw5w7u6akxzzhkgzhypge22p7zndhmktptmdiprvgs3dt7nchfj2bwac5akwvbvklihg7e5qegvtvflirzykhm5rcoznryhbhd23d3nfwnvfhnwy2t3blfdeslnn3bh72jnpuhuvm7hjewseqxx5eurkd2i3jdxd67trl4oshi6lgfler3tdnye7m5jbtue7b4gq7uvmjrxgsm55k5tbl4oovbniz2mtck4fkofnxnx5h7snsxlujwt3wkznicrjf3f5he423lcb4qiwdaime5kxrhujtpq6n42e77s2hpvfekgyfy7nj5eosi4eyor7oumpwxv7o45nz2ymbcbdxf7gd2qnno2s4l4wuhlltdaep7u3wijpa776ntygw5ndjkjb7ugtikgr6cuadfjzqh6wrnlucxw6t7kazfknlalr7uiadgff6vmnsig5qq6lipek573u5u2kmodrqomhuzj6nrj4y2jrm5sy7rd2nq7iosxb7m4pgvggspmhkf475cmz4huzgi3l3o4ndmknbwaseq25krrfewgvxu6s3b6dq43g4hba5yusbsujdzcry=?u=https%3A%2F%2Fbongacams.com%2Ftrack%3Fc%3D724872%26subid%3D1378335325453686%26subid2%3D320918",

`    `"cid": "485741",

`    `"title": "Самые милые котята",

`    `"desc": "-",

`    `"image": "https://s.lalacoat.com/nurl/744/nnmea3ddbf5vcb3dlvgfkz2inrsa66lrusovy24xvku47kohw2lm2v37lnmvqkf4k5qfcco74tlz5y5qzxagiugtrog5csj34h3npkswicxwdocxcbb57yxhkzfde6djgjlo7uxytfdriu3qubxeexbwjnqva6cuklehn2jtk7duu26apg6ncp7zndpyiuxtmc3xbfctq357mme3j3ro7a2cqfjuydwmbshe5hdjwv4zthtuo6atgxfsjkbypbto345bqdu4nltuuxxapfl6uoisuez243m3mbn2avoz3627wm5wj3ainlhkkw5dsse3gnkrugbf3f5ck3zst3fefm3q3nrvduswkfwrulmcksolpvwuq6v23r5wndyfi22cmfihr5glugafmiye65krzok6svwxteokijnsfvj4n4uviuryjfutfjtqqnrtlkswklqew2wsks57nkeup66fao5znmz5ytcda5tesnzwbb4ftesvuzgmsu2r4risv4lk6tqocsvbkpy7nzrzxfvohzh7mdrvi7sgkzic63rryzf54y6iprk7epgtrog5cspdmvi4qufeykmpfwpe6ze5svflvds3znuwzwu3asq=?1=1&data[]=16263375622729284407226739&v[]=3405945929&f=https%3A%2F%2Fi.cdnkimg.com%2Fauto%2F492x328%2Fimage%2Ftesr%2F8670%2F670%2Frect\_603e5e46360eat1614700102r2091.gif",

`    `"cpc": 0.0018077912298031153

`  `}

]

## **RTB**
### **CLICKUNDER**


|Attribute|Description|Using|Always passed|
| :-: | :-: | :-: | :- |
|id|Unique ID of the bid request, provided by the exchange||Yes|
|at|Auction type. For the first price auction at=1||Yes|
|cur|<p>Auction currency. Valid values: RUB - Russian ruble;</p><p>USD - American dollar</p>||Yes|
|tmax|Maximum time in milliseconds to submit a bid to avoid timeout|Recommended 150-300 ms|Yes|
|imp|Representing the impressions offered|Used to select materials that are relevant to the requirements|Yes|
||id|A unique identifier for this impression||Yes|
||secure|<p>Connection type. Possible choices: 0 — non-secure (HTTP);</p><p>1 — secure (HTTPS)</p>|||
||bidfloor|Minimum bid for this impression|||
||bidfloorcur|Impression value currency|||
||tagid|Identifier for specific ad placement or ad tag that was used to initiate the auction||Recommended|
||ext|Additional parameters|||
||instl|Parameter for Clickunder format||Yes|
|site|Details about the publisher's website||Yes|
||id|Site ID on the exchange|For the uniqueness of the site, the creation of black- or white-lists|Yes|
||domain|Domain of the site|For internal classification of domains in the Kadam system|Yes|
||page|URL of the page where the impression will be shown|||
||name|Stream name or its unique identifier|||
||publisher|Details about the Publisher object of the site|||
|||id|Unique ID of the site owner|||
||cat|IAB site category|You don't have to pass it if the "domain" parameter is filled in, because Kadam classifies domains internally|Recommended|
||ext|Additional site parameters|||
|user|Details about the human user of the device||Yes|
||id|Unique user ID in your system|Kadam generates on its own if not filled in||
||buyeruid|Buyer-specific ID for the user as mapped by the exchange for the buyer|||
||geo|Geolocation of a user device|||
|||utcoffset|Local time as the number +/- of minutes from UTC|||
|device|Details about the user's device to which the impression will be delivered||Yes|
||geo|Geolocation of the user device|||
|||country|Standard "ISO3" or "ISO2" country code|||
|||region|Region name|||
|||city|City name|||
||ip|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ipv6|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
||js|Support for JavaScript, where 0 - no, 1 - yes|||
||language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
||ext|Additional device parameters|||


**Example Request:**

{

`  `"id": "0ccab30d-a5a6-4574-8e60-aa4b4b76b4a3",

`  `"at": 1,

`  `"imp": [

`    `{

`      `"id": "724555910",

`      `"instl": 1,

`      `"secure": 0

`    `}

`  `],

`  `"site": {

`    `"id": "895584",

`    `"domain": "lalala.com",

`    `"cat": [

`      `"IAB25-3"

`    `],

`    `"page": "http://lalala.com",

`    `"ext": {

`      `"exchangecat": 508,

`      `"idzone": "5555336"

`    `}

`  `},

`  `"device": {

`    `"ua": "Mozilla/5.0 (Linux; Android 10; M2006C3LG) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.120 Mobile Safari/537.36",

`    `"ip": "95.47.98.198",

`    `"geo": {

`      `"country": "UKR"

`    `},

`    `"language": "ru",

`    `"os": "Android",

`    `"js": 1,

`    `"ext": {

`      `"remote\_addr": "95.47.98.198",

`      `"x\_forwarded\_for": ""

`    `}

`  `},

`  `"user": {

`    `"id": "55f7d2acada5b1.424949471132178479"

`  `}

}

**Example Response:**

{

`  `"id": "0ccab30d-a5a6-4574-8e60-aa4b4b76b4a3",

`  `"seatbid": [

`    `{

`      `"bid": [

`        `{

`          `"id": "1",

`          `"adid": "4927824",

`          `"crid": "4927824",

`          `"impid": "724711910",

`          `"price": 1.9711000061035155,

`          `"nurl": "https://s.lalacoat.com/nurl/863/nn2eqnzrlevvuarsmivfimkopfta27s5d5xcu7krpumtkzs2pufqkybnp4agg2stmyaxwxqkmr5vh34bnn2nfo6pyu2gmx3tneakouqkhmuz77eiuhdopvpirbjvbzom5xiuso7bstc22v2aubxlqvyqioy3fvcwjiihq2jsk2h34sm4i4kfg4fanzbfynslmfihqvcszb3osm2xy5fgxqdz5dyt76liqddfb43azzyziu7ivpctbg2oltlicqebknqhbxiorzhkqznvph5bkwlxqezx5msko3t2s3g7hkf2q3dn45ff5ydzk7vdsevbgoxg3g3alkqflreh5o543knqwspfdgcvthzn2fw2k5hlsyctfudrnmkldahvzghicg2uprcqhhrwwmiddqh5cuwlq3g2nnewzwu3asvdkjof2uryjgu4o7udoryfa6cuqi4jpkync7aitfdy3do22byynezfmt2lmgqephcqlwnwwmuojvficuxi6tt7ut4zgbl4ksdjm5fwonqapafaj5smujtpq62e4i5vrujrqx3wdiktxgsxrscktsdotl2m4nkhuucrvbgzenwojnfmcvgu6gg36t6bgzl76t7b2p7prnfj6nvyuux4th7m5bnlvxd3m2a=?1=1&data[]=16268540604187916861458595&v[]=3750347983&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}",

`          `"lurl": "https://s.lalacoat.com/lurl/863/nn2eqnzrlevvuarsmivfimkopfta27s5d5xcu7krpumtkzs2pufqkybnp4agg2stmyaxwxqkmr5vh34bnn2nfo6pyu2gmx3tneakouqkhmuz77eiuhdopvpirbjvbzom5xiuso7bstc22v2aubxlqvyqioy3fvcwjiihq2jsk2h34sm4i4kfg4fanzbfynslmfihqvcszb3osm2xy5fgxqdz5dyt76liqddfb43azzyziu7ivpctbg2oltlicqebknqhbxiorzhkqznvph5bkwlxqezx5msko3t2s3g7hkf2q3dn45ff5ydzk7vdsevbgoxg3g3alkqflreh5o543knqwspfdgcvthzn2fw2k5hlsyctfudrnmkldahvzghicg2uprcqhhrwwmiddqh5cuwlq3g2nnewzwu3asvdkjof2uryjgu4o7udoryfa6cuqi4jpkync7aitfdy3do22byynezfmt2lmgqephcqlwnwwmuojvficuxi6tt7ut4zgbl4ksdjm5fwonqapafaj5smujtpq62e4i5vrujrqx3wdiktxgsxrscktsdotl2m4nkhuucrvbgzenwojnfmcvgu6gg36t6bgzl76t7b2p7prnfj6nvyuux4th7m5bnlvxd3m2a=?1=1&data[]=16268540604187916861458595&v[]=3750347983&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}&loss=${AUCTION\_LOSS}",

`          `"adomain": [

`            `"z.lala.adpool.bet",

`            `"start.lalamatch.com"

`          `],

`          `"cat": [

`            `"IAB9-7"

`          `],

`          `"adm": "<?xml version=\"1.0\" encoding=\"ISO-8859-1\"?><ad><popunderAd><url><![CDATA[https://s.lalacoat.com/h/npqxsxg45fnhtmwvzhtwo4hy27kjjl7yrbkgoscribafyeqhafvgf6xksttfmebrzi4zm342k6hma2papgt4woxrncznnt6l4hqjrfbx6bedf2sxw5uyculsxrj255wl4cu3bne6v542iu7tqp6u3vsn7cz47zvjvxd3nfrtyzguvs2spiarhccligffitugmnihqvdnzbfxtssul3fwfa6ap3ndxceydclezpwv56mfhab3jnwtddsmtki75t25wi53e3o2kvhlwysr7bip5hmw5y2mms2komxxbbfqsrfxtaggkbjwa4cqcrjwqqzrha3ncqqjxf77yu4e5jxiev4oybu3q6pi6e73g2arguqt2wlfje2wecl2bjkg4kl5aiyuayjqln6a2btgp55qk2cngjvfw4cywjke5q3dqcnpquefjn7ilb3xrzrqqqpan3yexcrwqngvzvubicyvb6uig4e2mtpbts3kve6uz7cjkm2mbjauazsigjsvy6yike3swksugjexuzqkpviam333prigcs3gmmhxcxifn5p33l4os3m5jpozwuzx5t4p3sux2bgctd6kwnaoz7e42aqywlxkhudicbiepitgmcivg6r2phczpcoijvnuy4cvjkcou3qss7cegwcqpbkjftlbuwgrot2lmgahrcuqa4======?u=https%3A%2F%2Fz.cdn.lalapool.bet%2Fload%3Fz%3D2138977233%26random%3D%5Brandom%5D%26subID1%3Dcnv851a013cf8f6ca85bc5d4000d85f8c91%26s%3D1381598192828800\_321678]]></url></popunderAd></ad>"

`        `}

`      `]

`    `}

`  `]

}

### **PUSH**


|Attribute|Description|Using|Always passed|
| :- | :-: | :-: | :- |
|id|Unique ID of the bid request, provided by the exchange||Yes|
|at|Auction type. For the first price auction at=1||Yes|
|cur|<p>Auction currency. Valid values: RUB - Russian ruble;</p><p>USD - American dollar</p>||Yes|
|tmax|Maximum time in milliseconds to submit a bid to avoid timeout|Recommended 150-300 ms|Yes|
|imp|Representing the impressions offered|Used to select materials that are relevant to the requirements|Yes|
||id|A unique identifier for this impression||Yes|
||secure|<p>Connection type. Possible choices: 0 — non-secure (HTTP);</p><p>1 — secure (HTTPS)</p>|||
||bidfloor|Minimum bid for this impression|||
||bidfloorcur|Impression value currency|||
||tagid|Identifier for specific ad placement or ad tag that was used to initiate the auction||No|
||ext|Additional parameters|||
|||subage|User subscription age|If the parameter "subage" is not filled in, filled in incorrectly, or is not passed, it is considered "undefined", this reduces the redemption|Yes|
||native|Parameter for Push format||Yes|
|||request|Request payload complying with the Native Ad Specification|<p>Options:</p><p>openrtb.native.string - JSON query text; openrtb.native - the query is a JSON object.</p><p>It is similar to openrtb.native.string, only in case of string query is encoded to JSON text</p>|Yes|
|||ver|Version of the Native Ad Specification to which request complies. RECOMMENDED by the OpenRTB specification|||
|site|Details about the publisher's website||Yes|



||id|Site ID on the exchange|For the uniqueness of the site, the creation of black- or white-lists|Yes|
| :- | :- | :- | :- | :- |
||domain|Domain of the site|For internal classification of domains in the Kadam system|Yes|
||page|URL of the page where the impression will be shown|||
||name|Stream name or its unique identifier|||
||publisher|Details about the Publisher object of the site|||
|||id|Unique ID of the site owner|||
||cat|IAB site category|You don't have to pass it if the "domain" parameter is filled in, because Kadam classifies domains internally|Recommended|
||ext|Additional site parameters|||
|user|Details about the human user of the device||Yes|
||id|Unique user ID in your system|Kadam generates on its own if not filled in||
||buyeruid|Buyer-specific ID for the user as mapped by the exchange for the buyer|||
||geo|Geolocation of a user device|||
|||utcoffset|Local time as the number +/- of minutes from UTC|||
|device|Details about the user's device to which the impression will be delivered||Yes|
||geo|Geolocation of the user device|||
|||country|Standard "ISO3" or "ISO2" country code|||
|||region|Region name|||
|||city|City name|||
||ip|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ipv6|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
||js|Support for JavaScript, where 0 - no, 1 - yes|||
||language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
||ext|Additional user device parameters|||

**Example Request:**

{

`  `"id": "1",

`  `"at": 1,

`  `"cur": [

`    `"USD"

`  `],

`  `"tmax": 150,

`  `"imp": [

`    `{

`      `"id": "1-1",

`      `"secure": 1,

`      `"bidfloor": 0.001,

`      `"bidfloorcur": "USD",

`      `"native": {

`        `"ver": "1.2",

`        `"request": "{\"ver\":\"1.1\",\"layout\":1,\"adunit\":2,\"plcmtcnt\":1,\"assets\":[{\"id\":1,\"required\":

`                    `1,\"title\":{\"len\":45}},{\"id\":2,\"required\":1,\"img\":{\"type\":1,\"wmin\":192,\"hmin\":

`                    `192,\"mimes\":[\"image/jpeg\",\"image/png\"]}},{\"id\":3,\"required\":1,\"data\":{\"type\":

`                    `2,\"len\":40}},{\"id\":4,\"required\":0,\"img\":{\"type\":3,\"wmin\":360,\"hmin\":240,

`                    `\"mimes\":[\"image/jpeg\",\"image/png\"]}},{\"id\":5,\"required\":0,\"data\":{\"type\":12}},

`                    `{\"id\":6,\"required\":0,\"data\":{\"type\":12}}],\"plcmttype\":4}"

`      `}

`      `"ext": {

`        `"subage": 2}

`  `],

`  `"site": {

`    `"id": "1",

`    `"domain": "kadam.net",

`    `"page": "https://kadam.net/ru/",

`    `"name": "kdm-1",

`    `"publisher": {

`      `"id": "1"

`    `},

`    `"cat": [

`      `"IAB3-1"

`    `]

`  `},

`  `"device": {

`    `"ip": "212.95.5.236",

`    `"ua": "Mozilla%2F5.0+%28Linux%3B+Android+9%3B+SAMSUNG+SM-A105FN%29+AppleWebKit%2F537.36+

`            `%28KHTML%2C+like+Gecko%29+SamsungBrowser%2F12.1+Chrome%2F79.0.3945.136+Mobile+Safari%2F537.36",

`    `"geo": {

`      `"country": "AT"

`    `}

`  `},

`  `"user": {

`    `"id": "Xef4LfyUte-tzwpV3-fMV"

`  `}

}

**Example Response:**

{

`  `"id": "38b55b13-2548-429f-a667-f40f9895a8fc",

`  `"seatbid": [

`    `{

`      `"bid": [

`        `{

`          `"id": "1",

`          `"adid": "4809045",

`          `"crid": "4809045",

`          `"impid": "429959488",

`          `"price": 0.4735776340961457,

`          `"nurl": "https://s.viibum.com/nurl/379/nn2ew3bqbr4qwa3fmj4vizcapftau4apd43xs7kwpupgays6obiqwyzoomdtg2stmyahsuacmj5fh3wwnn2oncnk543wmx3tneaigvqkeau7phub3oqprh5gd45ohenjwvid7s5fqokv2kw6ihrtgckht2r7k6smpieus2jssy55qklphbkrvukode4c6t2lmfihqvfca7ewqm66jza7cup2rjkyqshrsbeposuelc4flb725rv76v2y7sygrlkvaby5iupkk6we7bcr33hrmavbnankwts422aubwkq4b3pach6jz2ncul35rjwhalizj2j6stkrb4zjyun5cl43knqwrqla6mu4kg6rf6nvgyliyfypfk2aokkhrqrfrsjcbwxfa7rjcwfnisuj3qwguzna4liqs7vwtf3xn46v6d2wu72jnatwvspjoqsj2y4nuu6olwt3qetyilpjbagulaimxs7lx2tf2heobkshbewsmswx52ksuq5qzidrelle23e3eue7givfir2jdrtcxrmpudtigtegqe6s2w3khtuqzhapndouo6r66dfpd2i73c4yvnchpay564cjtewkxjbalamisdk7qcurjzsrav4ivvwjpytmv7pj65irogtksie22eckl57vawwrw26eoxrnwxnbuv7twxypk5nhe======?1=1&data[]=16263527312597347616893108&v[]=968756519&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}",

`          `"lurl": "https://s.viibum.com/lurl/379/nn2ew3bqbr4qwa3fmj4vizcapftau4apd43xs7kwpupgays6obiqwyzoomdtg2stmyahsuacmj5fh3wwnn2oncnk543wmx3tneaigvqkeau7phub3oqprh5gd45ohenjwvid7s5fqokv2kw6ihrtgckht2r7k6smpieus2jssy55qklphbkrvukode4c6t2lmfihqvfca7ewqm66jza7cup2rjkyqshrsbeposuelc4flb725rv76v2y7sygrlkvaby5iupkk6we7bcr33hrmavbnankwts422aubwkq4b3pach6jz2ncul35rjwhalizj2j6stkrb4zjyun5cl43knqwrqla6mu4kg6rf6nvgyliyfypfk2aokkhrqrfrsjcbwxfa7rjcwfnisuj3qwguzna4liqs7vwtf3xn46v6d2wu72jnatwvspjoqsj2y4nuu6olwt3qetyilpjbagulaimxs7lx2tf2heobkshbewsmswx52ksuq5qzidrelle23e3eue7givfir2jdrtcxrmpudtigtegqe6s2w3khtuqzhapndouo6r66dfpd2i73c4yvnchpay564cjtewkxjbalamisdk7qcurjzsrav4ivvwjpytmv7pj65irogtksie22eckl57vawwrw26eoxrnwxnbuv7twxypk5nhe======?1=1&data[]=16263527312597347616893108&v[]=968756519&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}&loss=${AUCTION\_LOSS}",

`          `"adomain": [

`            `"track.lala.eu",

`            `"lalalar.me"

`          `],

`          `"cat": [

`            `"IAB25-4"

`          `],

`          `"adm": "<?xml version=\"1.0\" encoding=\"ISO-8859-1\"?><ad><popunderAd><url><![CDATA[https://s.lalabum.com/h/nokhsxg5xznhtbxhvtgwi4gm4wy35peiqjkgou2ribafyeqhafvgfdmxrptfmebrzi43e242k7d4azxaphp2coprncznnt6luhdm5oac6bedf2sxw5uycultxrj7r6o4soulbne6v542iu7y7hojhkfqwspk66oukcsm75ggvkyljhvpphcfalhdnmybecx3mn4mavst6vfwsmswoc5wgvmakzalqsxrvtre5q3cz7w6au7yjlq5lh43jczvg5inasvlk2brtaoezdiduadyuo5aukunmrvlmlphvpcrhg4wum6wjoilteh7klbdysd3ubluphvd6v5ejsu2k5ytg5thbnqaa4qmlbmkyyk2x5eo4ycqpdcbfeci5pwfd72k5hnx7pctxklw5scxnqua6jq3m4yay6c2krshy7ianangc2qkf5mfomrjf5ldgsbxnmhsqwkxn7husygypkazbhkl7ayfmt2lmfihqrqsubfx3d2uld6la2f5kyahdvcr7jkkyt5ukjx6hayavrv6u2owogivfdgo2ollj5xqu7teu6yzoj2wicbpleadi6t6lbrucz3dbjtv2ctcpf4fcy2mmvqqq4k2a5thm6sxidtprbnmulyp3caempqzjk5zlnujbde3x5erhyos2qddfoplqxpkzmfut2xxs5sugcxwcav7jbrwgyfdrsjl6t2tcjpe4u7drz7xjwvtjzidevsprmk4gmhlcola5cfyca4awxqynqcem===?u=https%3A%2F%2Ftrack.lobby-x.eu%2Fb229bef2-2901-4472-b022-c31262385df3%3Fw%3D47682%26Sub\_Age%3D0%26Campaign\_ID%3D495896%26creative%3D4809045%26website%3D1340370455156916%26platform%3DANDROID%26cost%3D7.5E-4%26subid%3Dcnvc3b413f236a8b582f1edfd7c0c97a0e9]]></url></popunderAd></ad>"

`        `}

`      `]

`    `}

`  `]

}

### **ON SITE PUSH (INPAGE)**



|Attribute|Description|Using|Always passed|
| :- | :-: | :-: | :- |
|id|Unique ID of the bid request, provided by the exchange||Yes|
|at|Auction type. For the first price auction at=1||Yes|
|cur|<p>Auction currency. Valid values: RUB - Russian ruble;</p><p>USD - American dollar</p>||Yes|
|tmax|Maximum time in milliseconds to submit a bid to avoid timeout|Recommended 150-300 ms|Yes|
|imp|Representing the impressions offered|Used to select materials that are relevant to the requirements|Yes|
||id|A unique identifier for this impression||Yes|
||secure|<p>Connection type. Possible choices: 0 — non-secure (HTTP);</p><p>1 — secure (HTTPS)</p>|||
||bidfloor|Minimum bid for this impression|||
||bidfloorcur|Impression value currency|||
||tagid|Identifier for specific ad placement or ad tag that was used to initiate the auction||No|
||ext|Additional parameters|||
||native|Parameter for Push format||Yes|
|||request|Request payload complying with the Native Ad Specification|<p>Options:</p><p>openrtb.native.string - JSON query text; openrtb.native - the query is a JSON object.</p><p>It is similar to openrtb.native.string, only in case of string query is encoded to JSON text</p>|Yes|
|||ver|Version of the Native Ad Specification to which request complies. RECOMMENDED by the OpenRTB specification|||



|site|Details about the publisher's website||Yes|
| :- | :- | :- | :- |
||id|Site ID on the exchange|For the uniqueness of the site, the creation of black- or white-lists|Yes|
||domain|Domain of the site|For internal classification of domains in the Kadam system|Yes|
||page|URL of the page where the impression will be shown||Yes|
||name|Stream name or its unique identifier|||
||publisher|Details about the Publisher object of the site|||
|||id|Unique ID of the site owner|||
||cat|IAB site category|You don't have to pass it if the "domain" parameter is filled in, because Kadam classifies domains internally|Recommended|
||ext|Additional site parameters|||
|user|Details about the human user of the device||Yes|
||id|Unique user ID in your system|Kadam generates on its own if not filled in||
||buyeruid|Buyer-specific ID for the user as mapped by the exchange for the buyer|||
||geo|Geolocation of a user device|||
|||utcoffset|Local time as the number +/- of minutes from UTC|||
|device|Details about the user's device to which the impression will be delivered||Yes|
||geo|Geolocation of the user device|||
|||country|Standard "ISO3" or "ISO2" country code|||
|||region|Region name|||
|||city|City name|||
||ip|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ipv6|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
||js|Support for JavaScript, where 0 - no, 1 - yes|||
||language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
||ext|Additional user device parameters|||

**Example Request:**

{

`  `"id": "1",

`  `"at": 1,

`  `"cur": [

`    `"USD"

`  `],

`  `"tmax": 150,

`  `"imp": [

`    `{

`      `"id": "1-1",

`      `"secure": 1,

`      `"bidfloor": 0.001,

`      `"bidfloorcur": "USD",

`      `"native": {

`        `"ver": "1.2",

`        `"request": "{\"assets\":[{\"title\":{\"len\":50},\"id\":1,\"required\":1},{\"id\":2,\"img\":

`                    `{\"w\":200,\"hmin\":200,\"type\":3,\"wmin\":200,\"h\":200},\"required\":1}],\"plcmtcnt\":

`                    `8,\"ver\":1.2}"

`      `}

`  `],

`  `"site": {

`    `"id": "1",

`    `"domain": "kadam.net",

`    `"page": "https://kadam.net/ru/",

`    `"name": "kdm-1",

`    `"publisher": {

`      `"id": "1"

`    `},

`    `"cat": [

`      `"IAB3-1"

`    `]

`  `},

`  `"device": {

`    `"ip": "212.95.5.236",

`    `"ua": "Mozilla%2F5.0+%28Linux%3B+Android+9%3B+SAMSUNG+SM-A105FN%29+AppleWebKit%2F537.36+

`            `%28KHTML%2C+like+Gecko%29+SamsungBrowser%2F12.1+Chrome%2F79.0.3945.136+Mobile+Safari%2F537.36",

`    `"geo": {

`      `"country": "AT"

`    `}

`  `},

`  `"user": {

`    `"id": "Xef4LfyUte-tzwpV3-fMV"

`  `}

}

**Example Response:**

{

`  `"cur": "RUB",

`  `"id": "a81f6c55-5f2f-44fb-a2d3-44503513c663",

`  `"seatbid": [

`    `{

`      `"bid": [

`        `{

`          `"id": "1",

`          `"adid": "4937999",

`          `"crid": "4937999",

`          `"cid": "511272",

`          `"impid": "1234567",

`          `"price": 0.3153782760333318,

`          `"nurl": "https://s.lalacoat.com/nurl/460/nn2bs3ddlz7quademj7aoyq6pftaylyld43x2l2spvggazyipjoagzjmpvlwg2stmyaxuxqln53fhmwmnn2propbtazx537a4waipk5ny63gqasgo5btdhd3brjvrfekr6jmfywy352dzn7irhxdijwptxwn27jm54y4g2dnl3apttcsmbfggocjngjm7vvclyihshg6he4wgs2wj5fwcudyurw3qsdixjlulw3atwovfyrz4hzs33sovfvja6o34ckuxjbtnuw2qwefphvpnclxwezycr5omco3igdn2behpt2xoquye2pvkzxtfhsvtjlxb63akpafkcpqjcirbbsoig4vdwmc2o23pfwnvgyevakr3gbnhnnxs3g2tmckrfixtjsthmnty4g7jvfwcuaygi2nm5wdgbkrugbf4b5jpufnt5vpavcuijqva6huzoq2avttnturapdyk6ag22kjnezfmt2lsfx3avrx5jfwt2suj2vwhlehx7a4lnuwzwuu5i3dioefmu5sjjqqoyd2prmdcqbv6i54k2e2kvepwysbyblzjtrtvey7vdzqsfjz7ghwxja6wnsujnepcvhvk3fdysgjg2zz7c7gk3ifau4ijxb3h7v67kv6g6xmk354x7heku======?1=1&data[]=16263517182058676639420194&v[]=2874186872&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}",

`          `"lurl": "https://s.lalacoat.com/lurl/460/nn2bs3ddlz7quademj7aoyq6pftaylyld43x2l2spvggazyipjoagzjmpvlwg2stmyaxuxqln53fhmwmnn2propbtazx537a4waipk5ny63gqasgo5btdhd3brjvrfekr6jmfywy352dzn7irhxdijwptxwn27jm54y4g2dnl3apttcsmbfggocjngjm7vvclyihshg6he4wgs2wj5fwcudyurw3qsdixjlulw3atwovfyrz4hzs33sovfvja6o34ckuxjbtnuw2qwefphvpnclxwezycr5omco3igdn2behpt2xoquye2pvkzxtfhsvtjlxb63akpafkcpqjcirbbsoig4vdwmc2o23pfwnvgyevakr3gbnhnnxs3g2tmckrfixtjsthmnty4g7jvfwcuaygi2nm5wdgbkrugbf4b5jpufnt5vpavcuijqva6huzoq2avttnturapdyk6ag22kjnezfmt2lsfx3avrx5jfwt2suj2vwhlehx7a4lnuwzwuu5i3dioefmu5sjjqqoyd2prmdcqbv6i54k2e2kvepwysbyblzjtrtvey7vdzqsfjz7ghwxja6wnsujnepcvhvk3fdysgjg2zz7c7gk3ifau4ijxb3h7v67kv6g6xmk354x7heku======?1=1&data[]=16263517182058676639420194&v[]=2874186872&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}&loss=${AUCTION\_LOSS}",

`          `"adomain": [

`            `"lalary.ru"

`          `],

`          `"cat": [

`            `"IAB2-3"

`          `],

`          `"adm": "{\"native\":{\"ver\":\"1.1\",\"link\":{\"url\":\"https://s.lalacoat.com/h/noihsxeburnhtggx465gasgy77lornuwzwu3assb7l47zi4jqpnda7sopnywq4aunvyeuooxq2h4yzzydxgfh5ckyez6zosm2fiyblktqbemtgost7spjuhnjkndsevrgoxg3k3alkifl47ozdsmzknqwspfdccv6pxmrzgmvgyljhsr7bljdow4x4y4mtkkyfjgx7sqhintzasukhzwgunvkzjdrkjjyjkerm3dih4fpfgogpqtd6upgcqvhh4y625edozrkrfuroktrcw6rh2orey5wtndmjiyqv2txbgyzyuwzbg7cvdziyftbrw3t5kf7y73j5qfk4rgbfugexaxiea3e4z43y46c2h7wne7wyhkrvj3uomerq2nmtkk5fjppzx7hl2gwcjuvrzkiuwg6drqnall4vpjusk2gknw3nz2orr6k2v7jh3mtjfbttw6b6vhk5kqu22ehm4akuqeef4q4fyhlazu2jyrbansq6ytl6lif3n43h5ydrtfdlljtrxmkuukrlot3kkm3knqwrqar6gw7zvctuoe4gg3lhvpq6vvggspmghv676hmb4huzfx5ce64ndmlrbwasfvwfkbr444gvxu6s3b6dq43o4h?u=https%3A%2F%2Fmodels.chery.ru%2Ftiggo4%2F%3Futm\_source%3DJustNow-teaser-2%26utm\_medium%3Dcp%D1%81%26utm\_campaign%3Djn\_t\_7pro%26utm\_term%3DIAB1-1\_1352756290519210\",\"directUrl\":\"https://models.chery.ru/tiggo4/?utm\_source=JustNow-teaser-2&utm\_medium=cpс&utm\_campaign=jn\_t\_7pro&utm\_term=IAB1-1\_1352756290519210\"},\"assets\":[{\"id\":1,\"required\":1,\"title\":{\"text\":\"Рассрочка 0%\"}},{\"id\":2,\"required\":1,\"img\":{\"w\":192,\"h\":192,\"url\":\"https://i.lalakimg.com/auto/192/image/vk/7999/999/60eedcafca39ft1626266799r8761.png\"}}]}}"

`        `},

`        `{

`          `"id": "2",

`          `"adid": "-341757022",

`          `"crid": "-341757022",

`          `"cid": "0",

`          `"impid": "1234567",

`          `"price": 0.2933655055920208,

`          `"nurl": "https://s.lalacoat.com/nurl/460/nn2bs3ddlz7quademj7aoyq6pftaylyld43x2l2spvggazyipjoagzjmpvlwg2stmyaxcxqemv5vhmwmnn2propbtazx537a4waipk5ny63gqasgo5btdhd3brjvrfekr6jmfywy352dzn7irhxdijwptxwn27jm54y4g2apl2xnx3csmbfhwqnnjbkc7deyly4hulox2mmnclgtur2ocul2yrj2z4loqjl4ppl3sb47nnn4ssl43knqwrqik6nurkhxpajtjdouvwkycaqcmsdtiyowoyj3aarqwmr3iayuoujzejsbmoiwpm3ewoi2lz4sy4qxhyosyk3kpqcb2id6hyagklrsdjuquistduprcjrddqwwo4rokzntwpy3cm4rwmlpdqzcqzyvdmbc4hrhaqahccrmj5ycypqtnvoc6e3nbi6xwgibcqrakkqgc53aumcpoawseelnfbsgixjilrjt2gq3gihruzilcv6dg6ymbinsana4gzta4brrkuoxwiqeduwbuaqaautxshbep4dwmsyznjprmxkaev5tulbsaear4aj6frlxwljscumt4frqp4if67jrpyusyibzcegvwlymnm5qs4rvhawwcocwbatfyibgf5jdoddmhjqcocc5dnrhgdrccaprw4qdgbcsyljme4aawhbaoq7aqxtebarca2jkhaee6lzzmicd27qha4zdujdaeiwhmyr4pynwski6hqgtqc3vmmcs4kq7b4paeqjhgadqicjrla3twlibjusqoyqpbmhtwfyzgvsuwgaipesbagkwfiycyo25h4tqmerbeuxamlb4aqaxclchd53syeiefq5aewrrgfyryhaskusrgyifkj5tqbqsdaetapilmiffgdbeoetaogiqdaywch34duwxkpb4b4wdem3ccr7dyldznz3dyltic4bsm2lzgbkaapaigmrc6pblov6bq23odr5amhcohz7wslsrnvrhwgjjgqab2alkhq7vkmabfeucacqahbudym2lmevqogb4caph6ujldz7ruczearqbagywjmfd4riyhmkfqjqiczqfokzwjiaayjzycjgr2e2mdyueip35bvmbggqobjld4aalan3xukqscvttuuqih56ganikfetdghrriamsowithqmqq7ilempuydryai7ak7jvfeqwey3zczpxaoiba4lbkllddvzageiacuftemlchvscust5aznsggyblfrc6djibuudcrztfyndoob5cjvaugqdafxrm7zfdmzbmpqageehyor4cflsolamaifc2idnmavs6pqueabsu5b4fnrrapjjbizb2jdhpyiq4x3od4hcsobvnvtayjzimymh4oaicu7hsnqvhqsh2hzhe5gakoj6e5qd4bdtbegqee3fjm4qwyb2hrswied6bjsbuyigmebvcbivaasdikijcmogejioji4awdbjauvwkfksdqcaiazzcqbx2tdfh4ecehiemaccouqfcq5ggvahanttu6d4cibcqeacoynt4raopeqtcajnnulhkkqeirsrmjirfbfboo24barh2ij3ejjcucizaj2bamidd4ucaoyufysti2t4gnrwkci2lenuqoyqnycq64zafv4suerreyju6hb7jmsbskiodqttqplihytqchz3fqltofjbmnmq2jc6aisaavdgjnraqaailnptgeaefm5dkhjklmaak2dfdyyvag2ameoa2e22nmmh4fbvh4gc4zkah4muemrfaegcuka5g5pxuxsieuaxgobjfytsgqq6hjpqkhqkebtq2hiloqnb4ylapudsubbrczvv47qljagcogzxcitw2k24a47eepiqaqrbopy2aifbag3zauptsczrafqge6y6avqgkaabceodoejipmecccqbfmjboortdqqxw7bbd4wcamytcueaofdqpe5uoeyvpayqoejrdv2widtger4conrx2bkw3ccinkffofedmcufvbctgkiwre4az3dj7l4hvowttklisoam5ru7v6d2xljzufukovf5jjraeliw3m5es2jsgyus3d3p2jlfc2q4fobfjdgj6sdhxfsqdrunrngoirlzvbshpwviww3uwkij25bavdfumt5yr65q2b2pjnqva6cuuidyc22xqrguxokspg2fbrfwqkq2xmfut2xxtxsrgb6f6b3boyvfsmoyk7pdtylkgxteywwzko7kekhyjlc7eln7jcdjzxgwlk5e22zwkxpu7esx4bifhgcnrtrjnscn2fknfvp2zh4khaku65h2fuxnqjiq====?1=1&data[]=16263517182058676639452695&v[]=953069526&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}",

`          `"lurl": "https://s.lalacoat.com/lurl/460/nn2bs3ddlz7quademj7aoyq6pftaylyld43x2l2spvggazyipjoagzjmpvlwg2stmyaxcxqemv5vhmwmnn2propbtazx537a4waipk5ny63gqasgo5btdhd3brjvrfekr6jmfywy352dzn7irhxdijwptxwn27jm54y4g2apl2xnx3csmbfhwqnnjbkc7deyly4hulox2mmnclgtur2ocul2yrj2z4loqjl4ppl3sb47nnn4ssl43knqwrqik6nurkhxpajtjdouvwkycaqcmsdtiyowoyj3aarqwmr3iayuoujzejsbmoiwpm3ewoi2lz4sy4qxhyosyk3kpqcb2id6hyagklrsdjuquistduprcjrddqwwo4rokzntwpy3cm4rwmlpdqzcqzyvdmbc4hrhaqahccrmj5ycypqtnvoc6e3nbi6xwgibcqrakkqgc53aumcpoawseelnfbsgixjilrjt2gq3gihruzilcv6dg6ymbinsana4gzta4brrkuoxwiqeduwbuaqaautxshbep4dwmsyznjprmxkaev5tulbsaear4aj6frlxwljscumt4frqp4if67jrpyusyibzcegvwlymnm5qs4rvhawwcocwbatfyibgf5jdoddmhjqcocc5dnrhgdrccaprw4qdgbcsyljme4aawhbaoq7aqxtebarca2jkhaee6lzzmicd27qha4zdujdaeiwhmyr4pynwski6hqgtqc3vmmcs4kq7b4paeqjhgadqicjrla3twlibjusqoyqpbmhtwfyzgvsuwgaipesbagkwfiycyo25h4tqmerbeuxamlb4aqaxclchd53syeiefq5aewrrgfyryhaskusrgyifkj5tqbqsdaetapilmiffgdbeoetaogiqdaywch34duwxkpb4b4wdem3ccr7dyldznz3dyltic4bsm2lzgbkaapaigmrc6pblov6bq23odr5amhcohz7wslsrnvrhwgjjgqab2alkhq7vkmabfeucacqahbudym2lmevqogb4caph6ujldz7ruczearqbagywjmfd4riyhmkfqjqiczqfokzwjiaayjzycjgr2e2mdyueip35bvmbggqobjld4aalan3xukqscvttuuqih56ganikfetdghrriamsowithqmqq7ilempuydryai7ak7jvfeqwey3zczpxaoiba4lbkllddvzageiacuftemlchvscust5aznsggyblfrc6djibuudcrztfyndoob5cjvaugqdafxrm7zfdmzbmpqageehyor4cflsolamaifc2idnmavs6pqueabsu5b4fnrrapjjbizb2jdhpyiq4x3od4hcsobvnvtayjzimymh4oaicu7hsnqvhqsh2hzhe5gakoj6e5qd4bdtbegqee3fjm4qwyb2hrswied6bjsbuyigmebvcbivaasdikijcmogejioji4awdbjauvwkfksdqcaiazzcqbx2tdfh4ecehiemaccouqfcq5ggvahanttu6d4cibcqeacoynt4raopeqtcajnnulhkkqeirsrmjirfbfboo24barh2ij3ejjcucizaj2bamidd4ucaoyufysti2t4gnrwkci2lenuqoyqnycq64zafv4suerreyju6hb7jmsbskiodqttqplihytqchz3fqltofjbmnmq2jc6aisaavdgjnraqaailnptgeaefm5dkhjklmaak2dfdyyvag2ameoa2e22nmmh4fbvh4gc4zkah4muemrfaegcuka5g5pxuxsieuaxgobjfytsgqq6hjpqkhqkebtq2hiloqnb4ylapudsubbrczvv47qljagcogzxcitw2k24a47eepiqaqrbopy2aifbag3zauptsczrafqge6y6avqgkaabceodoejipmecccqbfmjboortdqqxw7bbd4wcamytcueaofdqpe5uoeyvpayqoejrdv2widtger4conrx2bkw3ccinkffofedmcufvbctgkiwre4az3dj7l4hvowttklisoam5ru7v6d2xljzufukovf5jjraeliw3m5es2jsgyus3d3p2jlfc2q4fobfjdgj6sdhxfsqdrunrngoirlzvbshpwviww3uwkij25bavdfumt5yr65q2b2pjnqva6cuuidyc22xqrguxokspg2fbrfwqkq2xmfut2xxtxsrgb6f6b3boyvfsmoyk7pdtylkgxteywwzko7kekhyjlc7eln7jcdjzxgwlk5e22zwkxpu7esx4bifhgcnrtrjnscn2fknfvp2zh4khaku65h2fuxnqjiq====?1=1&data[]=16263517182058676639452695&v[]=953069526&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}&loss=${AUCTION\_LOSS}",

`          `"adm": "{\"native\":{\"ver\":\"1.1\",\"link\":{\"url\":\"https://s.lalacoat.com/h/nptxsxeburnhtggx465gasgy77lornuwzwu3assb7l47zi4jqpnda7sopnywq4aunvyeuooxq2h4yzzydxgfh5ckyez6zosm2fiyblktqbemtgost7spjuhnjkndsevrgoxg3k3alkifl47ozdsmzknqwspfdccv6pxmrzgmvgyljhsr7bljdow4x4y4mtkkznjhubqhrbfxp72uj5fyceeikzk4as3ywjkytpi33b57resdrfvnlgxlzfuye62wky5zc2wcv726yzvqpotvluckndbfktwlmw22rfgvhznssovx37dggqhqujecas2jfqpe3y3aytafhyrz6oodlpso37mvp6cwy45mc24qwhfznh5pq6v22ommnpji56dvsfjmh372ucjytfgguzfhwelsiaivihqdp4paiezzdratoz2lbjmwafygbzyy3g7js226buf5ljt4xn656viqfrfwqkq2xmfut2xxsdgsxlstwuxoxh6khluhvow4osclgrppeqsr3r4xyuaivs47fukjofvvq6kmy2ae4smiunea====?u=https%3A%2F%2F1.pasxfixs.com%2Fclick%2Fdspsl%2Fc9vnexyR5m%2Fv1ua5VfHQCKaKPZGsdy5Jg%3Fbip%3DP06ea5akUPS\_b1Y-5ZIZEPAddb46OXgK4ieMTNP8LNKJk4f63M8g\_4rs4qMbyUL9wEe-bytIFBbGY6Og1bMpAE\_cfeYmF9ThU5jnAOnvid3gt8hXnaoM-8orhKIJJYwzbgFPsHrLwal2GiA9RlZwfPPRr5fWJnvXkED4s5z9QJn5qbG5JeKOwJPynY5RFz9gCySulnPYDDZGaa7sQaKr\_R7zHxievN4DnnOVThV98EuI8gpTTnPbxXCJSY4uk5Wj2Q4DWBQms6XkEMCpHRqHI5MDTDGjsDMbK6FFuEK89wO8oWtQ0YfVsCRrWhyM5qY8S1gL6j-Qg8\_44RHdxISRuVgfNbIprTjPuZy7dLylhJ-ibwMLDoe0hODsCWwNt\_9vpB2ob\_xVClYB5IAtWAvi2F9CbZXnwi9U81KBm3hjAVN6zAHvKJcxPNkEsRi-swMtGQ0hJ6TyY61A\_6BoNLwEU7OJJx2CDyP2E0xr4oiuTJ82WYz5aXueaQVhEF82Sj39Y4DKJBl8xaNlsZ6wTXP2dI\_6dd\_DXWxLuBQFrbkbep5FXgm8PEHhM944nATN1siEF-d-uMOIhl-UAjuXwmA\_BIr53mYXsUW2\_5k4b5TYJ87COoUyqGNZlgxnDGHUS1GjUm6Uv\_b-41m0kt66Kl3Uln1lNjUl77sRPDPNRWvX6jPQU9DMcmv3Ynpx2CidAKOwti3zqMPLYX1IgkZDVqfR5ZQ3FQ8K0oBVLfAvb2KBIrAwUVyrVboL\_loPwN3Itgvgmu1aDMlTkK5636Z8A2me\_OJjMIxcIlZ3Qz1K85N5Z3YN1\_Totz7xvppdjJmzPIeg37zsN8YyVsqzWSmSQAA7uIYLSwS62LKTIB9f7bzZhPVB\_9ydNWpk\_OCGGNP2YrKSPrjay40CWlR3OJpLOEzCAH8WdYvjKHsC5H-zoxrEpSFH0RuEZ3PWieOM-gTr7lWg\",\"directUrl\":\"https://1.pasxfixs.com/click/dspsl/c9vnexyR5m/v1ua5VfHQCKaKPZGsdy5Jg?bip=P06ea5akUPS\_b1Y-5ZIZEPAddb46OXgK4ieMTNP8LNKJk4f63M8g\_4rs4qMbyUL9wEe-bytIFBbGY6Og1bMpAE\_cfeYmF9ThU5jnAOnvid3gt8hXnaoM-8orhKIJJYwzbgFPsHrLwal2GiA9RlZwfPPRr5fWJnvXkED4s5z9QJn5qbG5JeKOwJPynY5RFz9gCySulnPYDDZGaa7sQaKr\_R7zHxievN4DnnOVThV98EuI8gpTTnPbxXCJSY4uk5Wj2Q4DWBQms6XkEMCpHRqHI5MDTDGjsDMbK6FFuEK89wO8oWtQ0YfVsCRrWhyM5qY8S1gL6j-Qg8\_44RHdxISRuVgfNbIprTjPuZy7dLylhJ-ibwMLDoe0hODsCWwNt\_9vpB2ob\_xVClYB5IAtWAvi2F9CbZXnwi9U81KBm3hjAVN6zAHvKJcxPNkEsRi-swMtGQ0hJ6TyY61A\_6BoNLwEU7OJJx2CDyP2E0xr4oiuTJ82WYz5aXueaQVhEF82Sj39Y4DKJBl8xaNlsZ6wTXP2dI\_6dd\_DXWxLuBQFrbkbep5FXgm8PEHhM944nATN1siEF-d-uMOIhl-UAjuXwmA\_BIr53mYXsUW2\_5k4b5TYJ87COoUyqGNZlgxnDGHUS1GjUm6Uv\_b-41m0kt66Kl3Uln1lNjUl77sRPDPNRWvX6jPQU9DMcmv3Ynpx2CidAKOwti3zqMPLYX1IgkZDVqfR5ZQ3FQ8K0oBVLfAvb2KBIrAwUVyrVboL\_loPwN3Itgvgmu1aDMlTkK5636Z8A2me\_OJjMIxcIlZ3Qz1K85N5Z3YN1\_Totz7xvppdjJmzPIeg37zsN8YyVsqzWSmSQAA7uIYLSwS62LKTIB9f7bzZhPVB\_9ydNWpk\_OCGGNP2YrKSPrjay40CWlR3OJpLOEzCAH8WdYvjKHsC5H-zoxrEpSFH0RuEZ3PWieOM-gTr7lWg\"},\"assets\":[{\"id\":1,\"required\":0,\"title\":{\"text\":\"Новое сообщение:\"}},{\"id\":2,\"required\":0,\"img\":{\"w\":192,\"h\":192,\"url\":\"https://lalafixx.com/i57adpgseu/8e161b2a545cf057.png\"}},{\"id\":3,\"required\":0,\"data\":{\"value\":\"Таких милых котят вы еще никогда не видели\"}}]}}"

`        `}

`      `]

`    `}

`  `]

}

### **NATIVE (TEASER)**



|Attribute|Description|Using|Always passed|
| :- | :-: | :-: | :- |
|id|Unique ID of the bid request, provided by the exchange||Yes|
|at|Auction type. For the first price auction at=1||Yes|
|cur|<p>Auction currency. Valid values: RUB - Russian ruble;</p><p>USD - American dollar</p>||Yes|
|tmax|Maximum time in milliseconds to submit a bid to avoid timeout|Recommended 150-300 ms|Yes|
|imp|Representing the impressions offered|Used to select materials that are relevant to the requirements|Yes|
||id|A unique identifier for this impression||Yes|
||secure|<p>Connection type. Possible choices: 0 — non-secure (HTTP);</p><p>1 — secure (HTTPS)</p>|||
||bidfloor|Minimum bid for this impression|||
||bidfloorcur|Impression value currency|||
||tagid|Identifier for specific ad placement or ad tag that was used to initiate the auction||No|
||ext|Additional parameters|||
||native|Parameter for Push format||Yes|
|||request|Request payload complying with the Native Ad Specification|<p>Options:</p><p>openrtb.native.string - JSON query text; openrtb.native - the query is a JSON object.</p><p>It is similar to openrtb.native.string, only in case of string query is encoded to JSON text</p>|Yes|
|||ver|Version of the Native Ad Specification to which request complies. RECOMMENDED by the OpenRTB specification|||
|site|Details about the publisher's website||Yes|
||id|Site ID on the exchange|For the uniqueness of the site, the creation of black- or white-lists|Yes|
||domain|Domain of the site|For internal classification of domains in the Kadam system|Yes|
||page|URL of the page where the impression will be shown|||
||name|Stream name or its unique identifier|||
||publisher|Details about the Publisher object of the site|||
|||id|Unique ID of the site owner|||
||cat|IAB site category|You don't have to pass it if the "domain" parameter is filled in, because Kadam classifies domains internally|Recommended|
||ext|Additional site parameters|||
|user|Details about the human user of the device||Yes|
||id|Unique user ID in your system|Kadam generates on its own if not filled in||
||buyeruid|Buyer-specific ID for the user as mapped by the exchange for the buyer|||
||geo|Geolocation of a user device|||



|||utcoffset|Local time as the number +/- of minutes from UTC|||
| :- | :- | :- | :- | :- | :- |
|device|Details about the user's device to which the impression will be delivered||Yes|
||geo|Geolocation of the user device|||
|||country|Standard "ISO3" or "ISO2" country code|||
|||region|Region name|||
|||city|City name|||
||ip|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ipv6|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
||js|Support for JavaScript, where 0 - no, 1 - yes|||
||language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
||ext|Additional user device parameters|||

**Example Request:**

{

`  `"id": "1",

`  `"at": 1,

`  `"cur": [

`    `"USD"

`  `],

`  `"tmax": 150,

`  `"imp": [

`    `{

`      `"id": "1-1",

`      `"secure": 1,

`      `"bidfloor": 0.001,

`      `"bidfloorcur": "USD",

`      `"native": {

`        `"ver": "1.2",

`        `"request": "{\"assets\":[{\"title\":{\"len\":50},\"id\":1,\"required\":1},{\"id\":2,\"img\":

`        `{\"w\":200,\"hmin\":200,\"type\":3,\"wmin\":200,\"h\":200},\"required\":1}],\"plcmtcnt\":8,\"ver\":1.2}"

`      `}

`  `],

`  `"site": {

`    `"id": "1",

`    `"domain": "kadam.net",

`    `"page": "https://kadam.net/ru/",

`    `"name": "kdm-1",

`    `"publisher": {

`      `"id": "1"

`    `},

`    `"cat": [

`      `"IAB3-1"

`    `]

`  `},

`  `"device": {

`    `"ip": "212.95.5.236",

`    `"ua": "Mozilla%2F5.0+%28Linux%3B+Android+9%3B+SAMSUNG+SM-A105FN%29+AppleWebKit%2F537.36+

`            `%28KHTML%2C+like+Gecko%29+SamsungBrowser%2F12.1+Chrome%2F79.0.3945.136+Mobile+Safari%2F537.36",

`    `"geo": {

`      `"country": "AT"

`    `}

`  `},

`  `"user": {

`    `"id": "Xef5LfyUte-tzwpV3-fMV"

`  `}

}

**Example Response:**

{

`  `"cur": "USD",

`  `"id": "55554159-526d-4922-b1cd-b3268d242961",

`  `"seatbid": [

`    `{

`      `"bid": [

`        `{

`          `"id": "1",

`          `"adid": "4561472",

`          `"crid": "4561472",

`          `"cid": "436412",

`          `"impid": "22087-eupvu",

`          `"price": 0.6162098801136017,

`          `"nurl": "https://s.lalacoat.com/nurl/497/nn2eyzthaf6vqb3pmj7fgzq4pftac623d42h4kafpungoyaooegqayt5ojlwc2stmygx6wagmf6vhdhxnn2lxg5mzazx565ltt7ibk5ny63gqasgo5fddil3bqavr7ho23p4rqftyvntz4perhxdijwpuh4p65jmfszeqnz2s3552y2iojsveocjfeawlpduefitakrcgiygsmswj5fwdich2rjttqlihdde55ghk3efl3xjkpith7sfrnqjbtgckd2uq5pgezzj4yaymtmrbycixy5lgtwr7deuppctgk2gr43azv3oyuurhlpqjylibxte4sgzkf6iiuz7sfuklppsr5t3a6odxgcy2362k5hlsyctfudrnmkldahvzghicg2up7sqhmodu5xgjwz5rr4evkw4pnuwgoke2udikb4fieqlpkna2f6kuayjrbpdwedrq2jskzhuwynai6ofaxm3nmzi4tkkqfjpxl7bzfhicmcpx5ewbwt3lrtf46kyazqhw66bkmdpyuj67fvdz3smwleqzocx6xubhojr4pxorbfmq6v23r2iwqyzumcdl2qhxy6vrhvgnssvjlewkwl6ka4twtqfsweu5w3f7n5myvrz5fwzdcupzrt7q7cv4i6kbswx66plnvksybikvao6sxgktmfutziq====?1=1&data[]=16263531872967219577169276&v[]=2730842573&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}",

`          `"lurl": "https://s.lalacoat.com/lurl/497/nn2eyzthaf6vqb3pmj7fgzq4pftac623d42h4kafpungoyaooegqayt5ojlwc2stmygx6wagmf6vhdhxnn2lxg5mzazx565ltt7ibk5ny63gqasgo5fddil3bqavr7ho23p4rqftyvntz4perhxdijwpuh4p65jmfszeqnz2s3552y2iojsveocjfeawlpduefitakrcgiygsmswj5fwdich2rjttqlihdde55ghk3efl3xjkpith7sfrnqjbtgckd2uq5pgezzj4yaymtmrbycixy5lgtwr7deuppctgk2gr43azv3oyuurhlpqjylibxte4sgzkf6iiuz7sfuklppsr5t3a6odxgcy2362k5hlsyctfudrnmkldahvzghicg2up7sqhmodu5xgjwz5rr4evkw4pnuwgoke2udikb4fieqlpkna2f6kuayjrbpdwedrq2jskzhuwynai6ofaxm3nmzi4tkkqfjpxl7bzfhicmcpx5ewbwt3lrtf46kyazqhw66bkmdpyuj67fvdz3smwleqzocx6xubhojr4pxorbfmq6v23r2iwqyzumcdl2qhxy6vrhvgnssvjlewkwl6ka4twtqfsweu5w3f7n5myvrz5fwzdcupzrt7q7cv4i6kbswx66plnvksybikvao6sxgktmfutziq====?1=1&data[]=16263531872967219577169276&v[]=2730842573&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}&loss=${AUCTION\_LOSS}",

`          `"adomain": [

`            `"lala-fancy.com"

`          `],

`          `"cat": [

`            `"IAB14"

`          `],

`          `"adm": "{\"native\":{\"ver\":\"1.1\",\"link\":{\"url\":\"https://s.lalacoat.com/h/nobxsxf7t5nhtw7vvlvgasgmwsxznmmwzwu3assbxhn3d47jwtota7q4pnywq6iunvyeuomrrkh4yzzydxgfhskkyez2v62m2fi65kktqben3uvl4hj5zbheicndstmjgni2osxwxpczavgijd7nt24ljxqvfahnyxclpfwnvgyev4ksph2faipdnmyagfp3mnnmavst6vfwsmxwb65wgvuakzolqsuqtifmosggqarpiumn5dfnpkvqwspk66pzkh2dmyinszgpzzxb3nnzuo2mxmyv6skpbjjx6ohv45elcmpl6szyqumyk74tvilkgoteysxbktnyrev7j74tmv25cnuzbtgckauplobijzhgw2yqpecfqycdbgnfyjzvzfi4p4surbejlbsru5fn55t62ridtqll6lrnsso4kjsiaiqfrrvxuswcbguvfl24q45iqx5qnovetcb66vukeovbrh2m3wgsqcwzuvkiobbusbteo4xqonsbg4yvu623aezxylifgupdam25f5nfimzof4adms3aikg45dn32hcjt5dtkdklripgmrrnlnhysblsbvgqsqnqtm7uuotzxl4hvowts23nhiuh6nkjkjeppdxyzzxqqrkhjj467xssolcp23qlkzhuwildjot62===?u=https%3A%2F%2lalafancy.com%2F19603-kotyata.html%3Fsource%3D391%26id%3D4561472%26site\_id%3D1358915106853353%26mark3%3D316397%26tid%3D37698\"},\"assets\":[{\"id\":1,\"required\":1,\"title\":{\"text\":\"Таких милых котят вы еще никогда не видели\"}},{\"id\":2,\"required\":1,\"img\":{\"w\":400,\"h\":400,\"url\":\"https://i.lalakimg.com/auto/400/image/tesr/1472/472/5fbc73b0de9b6t1606185904r655.jpg\"}}]}}"

`        `}

`      `]

`    `}

`  `]

}

### **BANNER**



|Attribute|Description|Using|Always passed|
| :- | :-: | :-: | :- |
|id|Unique ID of the bid request, provided by the exchange||Yes|
|at|Auction type. For the first price auction at=1||Yes|
|cur|<p>Auction currency. Valid values: RUB - Russian ruble;</p><p>USD - American dollar</p>||Yes|
|tmax|Maximum time in milliseconds to submit a bid to avoid timeout|Recommended 150-300 ms|Yes|
|imp|Representing the impressions offered|Used to select materials that are relevant to the requirements|Yes|
||id|A unique identifier for this impression||Yes|
||secure|<p>Connection type. Possible choices: 0 — non-secure (HTTP);</p><p>1 — secure (HTTPS)</p>|||
||bidfloor|Minimum bid for this impression|||
||bidfloorcur|Impression value currency|||
||tagid|Identifier for specific ad placement or ad tag that was used to initiate the auction||No|
||ext|Additional parameters|||
||banner|Parameter for Banner format||Yes|
|||w|Width in device independent pixels (DIPS)||Yes|
|||h|Height in device independent pixels (DIPS)||Yes|
|site|Details about the publisher's website||Yes|
||id|Site ID on the exchange|For the uniqueness of the site, the creation of black- or white-lists|Yes|



||domain|Domain of the site|For internal classification of domains in the Kadam system|Yes|
| :- | :- | :- | :- | :- |
||page|URL of the page where the impression will be shown|||
||name|Stream name or its unique identifier|||
||publisher|Details about the Publisher object of the site|||
|||id|Unique ID of the site owner|||
||cat|IAB site category|You don't have to pass it if the "domain" parameter is filled in, because Kadam classifies domains internally|Recommended|
||ext|Additional site parameters|||
|user|Details about the human user of the device||Yes|
||id|Unique user ID in your system|Kadam generates on its own if not filled in||
||buyeruid|Buyer-specific ID for the user as mapped by the exchange for the buyer|||
||geo|Geolocation of a user device|||
|||utcoffset|Local time as the number +/- of minutes from UTC|||
|device|Details about the user's device to which the impression will be delivered||Yes|
||geo|Geolocation of the user device|||
|||country|Standard "ISO3" or "ISO2" country code|||
|||region|Region name|||
|||city|City name|||
||ip|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ipv6|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
||js|Support for JavaScript, where 0 - no, 1 - yes|||
||language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
||ext|Additional user device parameters|||

**Example Request:**

{

`  `"id": "1",

`  `"at": 1,

`  `"cur": [

`    `"USD"

`  `],

`  `"tmax": 150,

`  `"imp": [

`    `{

`      `"id": "1-1",

`      `"secure": 1,

`      `"bidfloor": 0.001,

`      `"bidfloorcur": "USD",

`      `"banner": {

`        `"w": 640,

`        `"h": 360

`      `}

`    `}

`  `],

`  `"site": {

`    `"id": "1",

`    `"domain": "kadam.net",

`    `"page": "https://kadam.net/ru/",

`    `"name": "kdm-1",

`    `"publisher": {

`      `"id": "1"

`    `},

`    `"cat": [

`      `"IAB3-1"

`    `]

`  `},

`  `"device": {

`    `"ip": "212.95.5.236",

`    `"ua": "Mozilla%2F5.0+%28Linux%3B+Android+9%3B+SAMSUNG+SM-A105FN%29+AppleWebKit%2F537.36+

`            `%28KHTML%2C+like+Gecko%29+SamsungBrowser%2F12.1+Chrome%2F79.0.3945.136+Mobile+Safari%2F537.36",

`    `"geo": {

`      `"country": "AT"

`    `}

`  `},

`  `"user": {

`    `"id": "Xef4LfyUte-tzwpV3-fMV"

`  `}

}

**Example Response:**

{

`  `"cur": "RUB",

`  `"id": "55c2ce7f-2a3e-4d4b-a98b-dc97c68d9416",

`  `"seatbid": [

`    `{

`      `"bid": [

`        `{

`          `"id": "1",

`          `"adid": "TPL77\_AD4884264",

`          `"crid": "TPL77\_AD4884264",

`          `"cid": "503406",

`          `"impid": "1",

`          `"price": 2.1730898173053195,

`          `"nurl": "https://s.lalacoat.com/nurl/396/nn2eazjrbivaybjqmj4qayy5pftfy7ild43xm4ydpuodo2ypfjpqumtwp5igm2stmyahcxiamb5vhcgznn2ll2fqqa3h5d6drwtxuzccabattpsvc5baddpx72p7vo6554wspnucsd7veivyswn2cxjx5zunu6jwlkimpqzqjzcxuykqpbkfeocnffzfobzrcfnacvcshbewsmvgodfwaupqkvmkqsezqnjp6suprrtoyu6zicuth7wb4frz26m5tclxhpbtltmb2imipgbvvxkinezhmd5dmbciqvpqhk2grboycfy6yuxb6upajylibxte4sgzkerzyu6ano4tgx4xjlgz3ygjktmerrp7z3je3ckrpgtfgoy3hryn6tj2lrnk75zc3v3mgmcvdimclyd2zcapdu4rzwu3bndasj5e6wzyjfutevspj4qrd3esk3jdkcztcypewykqpbkffsdwueydhhkjmgehuvnshlq5lmn5jcrwgruikzj3estbae2h27ksnanwnsr3atetclhhjbvoa62e5i53d6quszglz4twvbl6jro4n7xvkptwvnxyqv75vx522ooujnagovgrrnjuqswo5vlshw3f757myvrz5fw47nmpzrt7q7cv4i6k5oolx7n5nucsybim52ua6pfktmfutziq====?1=1&data[]=16263541733087802523950643&v[]=-1830393826&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}&total=2.1730898173053195",

`          `"adomain": [

`            `"lalads.com",

`            `"lalads.site"

`          `],

`          `"cat": [

`            `"IAB18-1"

`          `],

`          `"w": 336,

`          `"h": 280,

`          `"adm": "<div id=\"fzEzZhreHpxfDveA\"><a href=\"https://s.lalacoat.com/h/nobhsxf3wfnhtvmgw2rgksfy3s7m6s2j2wdlnixvzxevm6rrpf4quxqpoquvgkfjwh4m4322gpluv3kt2bk7jm2b3ez6zpck3fi3rxf6z656lkgjakbwac5akwvbvkliho7e5z5mzdsvfirz4wskvs2jznr4zku5zdalnfwnvfhnwy2r3blejeslnnya772joxuhuvm7hjewteqxv5e4guuqkyp4qs3czjkf7s3cvdvxfwr3x35bj5sm7womk7xzkfexjiynszgoj5hcxrpyao2cn43p7eckcfj57c2tksiwvd7atsawhmd37nknastiyjku5s3fvwnzjvj63fwtgrbripe55uswilljk5zkk5xucikrfbpaumrjra5t4npdmcqmsuhchhx6eov6j255aveckvyvwjy7kyzx46cymrhgazqooboaiztxpmbgmqdbmihxqukqgr5c2u3cjjr5eosi4eyp5qpbmpwxvhmys5z2ymc43aosdgd2qnno2s66xqehlltdzhmrq3wijobnpwpxstiyjchzkmrh4yzgee4suirtd5sts435dnfg6ayceyassyzcfckonge3rw45ldidptjojo72hedop57cxn7qzuv24u5vfmht2d4fcwsrlkouawkipzgxxhftxdjvias2mezu5p72mvyn5x22afewsmswj5fwlea=?u=https%3A%2F%2lalads.com%2FBht8Y8ry%3Fcost%3D2.5%26currency%3Drub%26external\_id%3Dcnvde13946446956080c6850718bb5f2227%26creative\_id%3D4884264%26ad\_campaign\_id%3D503406%26source\_id%3D1342406209202279%26category\_id%3D1189\" trackerlink=\"https://s.lalacoat.com/c/nobhsxf3wfnhtvmgw2rgksfy3s7m6s2j2wdlnixvzxevm6rrpf4quxqpoquvgkfjwh4m4322gpluv3kt2bk7jm2b3ez6zpck3fi3rxf6z656lkgjakbwac5akwvbvkliho7e5z5mzdsvfirz4wskvs2jznr4zku5zdalnfwnvfhnwy2r3blejeslnnya772joxuhuvm7hjewteqxv5e4guuqkyp4qs3czjkf7s3cvdvxfwr3x35bj5sm7womk7xzkfexjiynszgoj5hcxrpyao2cn43p7eckcfj57c2tksiwvd7atsawhmd37nknastiyjku5s3fvwnzjvj63fwtgrbripe55uswilljk5zkk5xucikrfbpaumrjra5t4npdmcqmsuhchhx6eov6j255aveckvyvwjy7kyzx46cymrhgazqooboaiztxpmbgmqdbmihxqukqgr5c2u3cjjr5eosi4eyp5qpbmpwxvhmys5z2ymc43aosdgd2qnno2s66xqehlltdzhmrq3wijobnpwpxstiyjchzkmrh4yzgee4suirtd5sts435dnfg6ayceyassyzcfckonge3rw45ldidptjojo72hedop57cxn7qzuv24u5vfmht2d4fcwsrlkouawkipzgxxhftxdjvias2mezu5p72mvyn5x22afewsmswj5fwlea=?u=https%3A%2F%2Fmigtds.com%2FBht8Y8ry%3Fcost%3D2.5%26currency%3Drub%26external\_id%3Dcnvde13946446956080c6850718bb5f2227%26creative\_id%3D4884264%26ad\_campaign\_id%3D503406%26source\_id%3D1342406209202279%26category\_id%3D1189\" data-set=\"href\" target=\"\_blank\" class=\"k-bloc yMYoyBIvbMhofBbE\"><div class=\"k-bloc\_\_img\" style=\"background-image: url('https://i.lalakimg.com/auto/336x168/image/tesr/4264/264/rect\_60c1bfe267527t1623310306r2827.jpg');\"></div><div class=\"k-bloc\_\_wrapper\"><div class=\"k-bloc\_\_title\">Таких милых котиков вы еще не видели</div><div class=\"k-bloc\_\_arrow\"><svg width=\"30\" height=\"18\" viewBox=\"0 0 30 18\" fill=\"none\" xmlns=\"http://www.lala.org/2000/svg\"><path d=\"M3 9L27 9\" stroke=\"#A4A4A4\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\"/><path d=\"M22.5 4.5L27 9L22.5 13.5\" stroke=\"#A4A4A4\" stroke-width=\"2\" stroke-linecap=\"round\" stroke-linejoin=\"round\"/></svg></div></div></a></div><style>@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=swap');#fzEzZhreHpxfDveA \* {box-sizing: border-box;font-family: 'Roboto', sans-serif;}#fzEzZhreHpxfDveA .k-bloc {position: relative;width: 336px;height: 280px;display: block;background-color: #ffffff;text-decoration: none;}#fzEzZhreHpxfDveA .k-bloc:hover .k-bloc\_\_arrow svg path{stroke: #ffffff;}#fzEzZhreHpxfDveA .k-bloc:hover .k-bloc\_\_wrapper {margin-top: -15px;}#fzEzZhreHpxfDveA .k-bloc\_\_img {background-position: center;background-repeat: no-repeat;background-size: cover;width: 336px;height: 168px;}#fzEzZhreHpxfDveA .k-bloc\_\_wrapper {background-color: #4F4F4F;box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.2);border-radius: 5px;padding: 14px 8px 4px;margin: -10px auto 0;width: 100%;max-width: 312px;transition: all 0.2s;}#fzEzZhreHpxfDveA .k-bloc\_\_title {font-weight: bold;font-size: 13px;line-height: 15px;color: #FFFFFF;min-height: 64px;margin-bottom: 10px;}#fzEzZhreHpxfDveA .k-bloc\_\_arrow {width: 30px;height: 18px;margin: 0 0 0 auto;}#fzEzZhreHpxfDveA .k-bloc\_\_arrow svg {width: 100%;height: 100%;transition: all 0.2s;}</style>"

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
||secure|<p>Connection type. Possible choices: 0 — non-secure (HTTP);</p><p>1 — secure (HTTPS)</p>|||
||bidfloor|Minimum bid for this impression|||
||bidfloorcur|Impression value currency|||
||tagid|Identifier for specific ad placement or ad tag that was used to initiate the auction||No|
||ext|Additional parameters|||
||video|Video format parameter||Yes|
|||mimes|Whitelist of content MIME types supported|Popular MIME types include but are not limited to "image/jpg", "image/gif" and "application/x-shockwave-flash".|Yes|
|||minduration|Minimum video ad duration in seconds|||
|||maxdurati on|Maximum video ad duration in seconds||Yes|
|||protocols|Array of supported video bid response protocols|<p>Examples: VAST\_1\_0 = 1;</p><p>VAST\_2\_0 = 2;</p><p>VAST\_3\_0 = 3</p>|Yes|
|||w|Width of the video player in device independent pixels (DIPS)||Yes|
|||h|Height of the video player in device independent pixels (DIPS)||Yes|
|||startdelay|Indicates the start delay in seconds for pre-roll, mid-roll, or post-roll ad placements|Valid values: number of seconds - the commercial is shown after the specified number of seconds; 0 - pre-roll (commercial is shown before the main content); -1 - mid-roll (commercial is shown during the main content); -2 - post- roll (commercial is shown after the main content); -3 - pause-roll (commercial is shown during a pause)|Yes|
|site|Details about the publisher's website||Yes|
||id|Site ID on the exchange|For the uniqueness of the site, the creation of black- or white-lists|Yes|
||domain|Domain of the site|For internal classification of domains in the Kadam system|Yes|
||page|URL of the page where the impression will be shown|||
||name|Stream name or its unique identifier|||
||publisher|Details about the Publisher object of the site|||
|||id|Unique ID of the site owner|||



||cat|IAB site category|You don't have to pass it if the "domain" parameter is filled in, because Kadam classifies domains internally|Recommended|
| :- | :- | :- | :- | :- |
||ext|Additional site parameters|||
|user|Details about the human user of the device||Yes|
||id|Unique user ID in your system|Kadam generates on its own if not filled in||
||buyeruid|Buyer-specific ID for the user as mapped by the exchange for the buyer|||
||geo|Geolocation of a user device|||
|||utcoffset|Local time as the number +/- of minutes from UTC|||
|device|Details about the user's device to which the impression will be delivered||Yes|
||geo|Geolocation of the user device|||
|||country|Standard "ISO3" or "ISO2" country code|||
|||region|Region name|||
|||city|City name|||
||ip|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ipv6|User device IP address|To determine the geolocation of a user's device on the Kadam side|Required “ip” or “ipv6”|
||ua|User agent|To identify the user's operating system, device and browser on the Kadam side|Yes|
||js|Support for JavaScript, where 0 - no, 1 - yes|||
||language|Main browser language, ISO 3166-1 alpha-2 coding|To define the browser language. Examples: &language=ru-RU or &language=ru. If the parameter "language" is not filled in, filled in incorrectly or not passed, it is considered "undefined", it reduces the buyout||
||ext|Additional user device parameters|||

**Example Request:**

{

`  `"id": "1",

`  `"at": 1,

`  `"cur": [

`    `"USD"

`  `],

`  `"tmax": 150,

`  `"imp": [

`    `{

`      `"id": "1-1",

`      `"secure": 1,

`      `"bidfloor": 0.001,

`      `"bidfloorcur": "USD",

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

`        `"startdelay": 0

`      `}

`      `"instl": 0

`    `}

`  `],

`  `"site": {

`    `"id": "1",

`    `"domain": "kadam.net",

`    `"page": "https://kadam.net/ru/",

`    `"name": "kdm-1",

`    `"publisher": {

`      `"id": "1"

`    `},

`    `"cat": [

`      `"IAB3-1"

`    `]

`  `},

`  `"device": {

`    `"ip": "212.95.5.236",

`    `"ua": "Mozilla%2F5.0+%28Linux%3B+Android+9%3B+SAMSUNG+SM-A105FN%29+AppleWebKit%2F537.36+

`            `%28KHTML%2C+like+Gecko%29+SamsungBrowser%2F12.1+Chrome%2F79.0.3945.136+Mobile+Safari%2F537.36",

`    `"geo": {

`      `"country": "AT"

`    `}

`  `},

`  `"user": {

`    `"id": "Xef4LfyUte-tzwpV3-fMV"

`  `}

}

**Example Response:**

{

`  `"cur": "USD",

`  `"id": "4c5568d6-9671-418c-addc-74f2d61e0697",

`  `"seatbid": [

`    `{

`      `"bid": [

`        `{

`          `"id": "1",

`          `"impid": "item\_1",

`          `"price": 0.6621354882128117,

`          `"adm": "<?xml version=\"1.0\" encoding=\"UTF-8\"?><VAST version=\"3.0\"><Ad id=\"item\_0\"><InLine><AdSystem><![CDATA[KDM]]></AdSystem><AdTitle><![CDATA[Таких милых котят вы еще никогда не видили!]]></AdTitle><Impression><![CDATA[https://s.lalacoat.com/nurl/505/nn2eyn3hbj7vcvtamjzfoz2jpftas4ikd43swlycpvhwanakfvpqgm37pvmgo2stmyaxuwaamr3vh6h2nn2ipiwltxektmfutzivby6nwwcwwasgo5btdkl3bqpvriwerpxzllnnstvfkow2v6u3kub7zp6ztjcrfleefyztgrd5phh4pjgbigg5ninvmt2lmfir7mlnpbecdw2re5ercwqbkrjdqsljgkthbs3akhyfkwfijdt4uup7jkkmez7mko3ufkjtzkzooy45peh2gctvxqzwk7dyl2eht72u2bec7qsx3nejyujduvqajrdlaa3gw56jkfd6iuz36fuglhso6naia6k7ri42xr6utng2wyfs22zj6ovbnaz2itsigqbtzxkqhbewtmsc4gsf56t2k4dwwdozgdq7zngyvcd2xlohjcvta7tojnqva6cvgxoxmqbs6iryqv3atvvweldrpvzvn2zhujtermlnnfewsmswj5fzc35qky36us3j5jke5k3drgsljlz6ufvsljsnjlvvg4damqhx6wqkg4u6wyvzp76fcepzniqo4tee4b2lqv4zvfw3smnqyks4tkmhvow4osfugfhdn7c5ub52vom7wnv3ausnljrma7hzkcqe22eskkw23ioxp3sfn3ot5pdmz3h6mpuhzy7by7yjdtnjwc2ga===?1=1&data[]=16263545302379371112518666&v[]=1903153267&cur=${AUCTION\_CURRENCY}&bid=${AUCTION\_PRICE}]]></Impression><Creatives><Creative id=\"4931228\" AdID=\"4931228\"><Linear skipoffset=\"00:00:00\"><Duration>00:00:29</Duration><TrackingEvents></TrackingEvents><VideoClicks><ClickThrough><![CDATA[https://s.lalacoat.com/h/nopxsxglsjnhtz6mzw7zxl4hvowtsuo6vxnygskbqxrnnjvc5loda7qcpnywq4aunvyeuooqwch4yzzydxgfhqkkyezyl6km2fizbkktqben5lo3qom4x45y7jj7asb65jl7o2ubkfz3yu6246h76vf7jkb75huzkc4exxubvh3lhhvpq6vvhkclncjfiwhbmnjd2epchih5cmcxqjewcugycszdvxlkyjkgnm3dil4fphnznxqtdho6n7avhhwzxsilbfwnvgyevtctmaw6kbejnlgl32frmobhwvsdhoiwvkhsukxwtmd37finastiyjku5s3fwkpjjvj6lmedvsvs45rubdogjuqeqslup3nuqikrgblaemqrmnjnsrbdrbl5avo4ybhnsm4f7fgisupwvrk3qs3ixjknhnwnklqfmrufjmzmgzdtrzrwgs3hnxyexqruqngrbedcisyvacrjjuhkmtprrcdph4eyswjzqm2mazauc2cpme3vw7ykauzh2ksvgindkyaloeeakmtwfycdehjxgbohsxqfi2sonwhjukzj57g3nannnu4cxvksrdmo3c2g62wwzxttgmgauls7vn4wzwu3assdkzykiwiiubxbuvd7vgdzb72sna3ec2bk3c3uyqmdzzjrulazpu======?u=http%3A%2F%2lalafer.com%2Fclick.php%3Fkey%3Dg43ie8y23wuj5zbxz34v%26cost%3D0.0%26SID%3D1360206185401685%26ID%3D4931228%26CID%3D510325%26RID%3DEE%26CATID%3D1520%26SUBAGE%3D0%26LANG%3Dru%26PLTFRM%3DANDROID%26price\_model%3D2]]></ClickThrough></VideoClicks><MediaFiles><MediaFile delivery=\"progressive\" type=\"video/mp4\" codec=\"0\" bitrate=\"915\" width=\"1280\" height=\"720\"><![CDATA[https://i.laladn.com/video/video/1228/228/60e860a7a32fet1625841831r9272.mp4]]></MediaFile></MediaFiles></Linear></Creative></Creatives></InLine></Ad></VAST>"

`        `}

`      `],

`      `"seat": "1",

`      `"group": 0

`    `}

`  `]

}

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
| :- | :- | :- | :- | :- |
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
| :- | :- | :- | :- | :- |
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

