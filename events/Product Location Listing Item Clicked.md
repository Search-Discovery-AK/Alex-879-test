# Product Location Listing Item Clicked

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Product Location Listing Item Clicked",
    "listingDisplayed": {
        "sortOrder": "<sortOrder>"
    },
    "listingItemClicked": {
        "listing": [
            {
                "itemPosition": "<itemPosition>",
                "location": {
                    "locationBrand": "<locationBrand>",
                    "locationId": "<locationId>",
                    "locationName": "<locationName>",
                    "locationStatus": "<locationStatus>",
                    "locationType": "<locationType>"
                },
                "productInfo": {
                    "sku": "<sku>"
                }
            }
        ]
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|itemPosition|integer|Integer position of a property within a sorted result. The first returned is position 1. For map results, this value can be the rank by distance from POI.|1, 2, 3, 4, 5||||0|||
|locationBrand|string|The brand associated with a location.|BMO Harris, Walmart, Lands' End, Motel 6, AC Hotels|||||||
|locationId|string|Unique Identifier of a Location. |155, 65588, 987764448|||||||
|locationName|string|The friendly name of the location.|Deerefiled Outlet, Old Orchard, Manhatten Midtown|||||||
|locationStatus|string|The status of a location.|Closed, Open, Coming Soon, Wait-listed|||||||
|locationType|string|The type of the location|Retail Store, Lodging, ATM, Banking Branch|||||||
|sku|string|Stock Keeping Unit \(SKU\) Unique Identifier of specific item \(typically\) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants. |34567890, 4567890, 00155-large-cornflower|||||||
|sortOrder|string|Indicates the sort order.|high-low, low-high, nearest-farthest, a-z, newest-oldest|||||||
