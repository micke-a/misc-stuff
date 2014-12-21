


##### Model Asset attributes
* modelId
* name
* contentType
* value


##### Config

```groovy
model{
  //normal stuff
  assets{
    asset name:'cgr', contentType:'text/xml', file:'src/main/asserts/cgr.xsl'
    asset name:'calc-xml', contentType:'text/xml', file:'src/main/assets/calc.xml'
    asset name:'view-xml', contentType:'text/xml', file:'src/main/assets/view.xml'
  }
}
```

##### Access

GET `v{version}/model/{modelId}/asset/{assetName}`
