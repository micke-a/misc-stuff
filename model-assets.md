

##### Asset types

* Shared Asset
  * Things shared between Models or Model Assets
  * Ex. jquery JS library , Twitter Bootstrap CSS framework
  * Can be referenced to from within Model Assets
  * Can be stored in the webapp as normal files
* Model Asset
  * Specific to  model
  * Ex. How to present a result, capture inputs or other reports on the same data 

##### Shared Asset
* name
* contentType
* value

GET `v{version}/shared/asset/{assetName}` 



##### Model Asset
* modelId
* name
* contentType
* value

Models also declares the shared assets they depend on so this can be tracked

##### Config

```groovy
model{
  //normal stuff
  assets{
    asset name:'cgr', contentType:'text/xml', file:'src/main/asserts/cgr.xsl'
    asset name:'calc-xml', contentType:'text/xml', file:'src/main/assets/calc.xml'
    asset name:'view-xml', contentType:'text/xml', file:'src/main/assets/view.xml'
    asset name:'jquery-2.1.3.min.js', shared:true
  }
}
```

##### Access

GET `v{version}/model/{modelId}/asset/{assetName}`
