5 to 6 digits
```
"(\\d{5,6})";  // 
```
starts with 1 and 0, then 4 digits of 0-9. i.e. 100281
```
"(?<![0-9])[1]{1}[0]{1}[0-9]{4}(?![0-9])"; // 
```
word starts with r1
```
"((r1)\\w+)"; 
```

extract text inside configOverrides or *onfigOverrides
```
"(?<=onfigOverrides).*";  // extract text inside configOverrides or *onfigOverrides
```
ALLCAPS.ALLCAPS or ALLCAPS.ALLCAPS.ALLCAPSWebV1_0
```
"[A-Z]{1,256}\\.[A-Z]{1,256}(\\.[A-z0-9]*?(?=\\\\|\\\"))?";

```
https://jirap.corp.ebay.com/browse/TEST-73480
```
"https:\\/\\/jirap.corp.ebay.com\\/browse\\/TEST-\\d+";
```

exclude first and last character
```
"(?<=:).*(?=-)"
```
example:
```
input: Rollback manifest ID:appnem-0.0.1_SNAPSHOT_20220510042405761
output: appname
```

get in between characters, excluding delimiters
```
(?<=\M)(.*?)(?=\M)
```
example:
```
input: MsnapshotM
output: snasphot
```

get until character, excluding delimiter
```
(?<=\M)(.*?)(?=\M)
```
example:
```
input: snapshotM
output: snasphot
```
