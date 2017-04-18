vue-google-maps-location-selector
=============

A vuejs google maps component that allows latitude and longitude to be selected from a map interface.

## Installation
---------------
##npm
``` sh
npm install --save vue-google-maps-location-selector
```

Include the google maps script in the head of your index.html file and add your API key
``` html
<script src="https://maps.googleapis.com/maps/api/js?key=[YOUR_API_KEY_HERE]"></script>
```

Use the component by passing though an initial latitude and longitude.
The `locationUpdated` event will fire as soon as the maps `center_changed` event fires.
``` html
<map-location-selector :latitude=[ADD_INITIAL_LATITUDE] :longitude=[ADD_INITIAL_LONGITUDE]
  @locationUpdated="locationUpdated">
</map-location-selector>
```

You can get the location in the callback function defined in the `locationUpdated` event.
``` javascript
methods:{
  locationUpdated(latlng) {
    this.latitude = latlng.lat;
    this.longitude = latlng.lng;
  }
}
```
