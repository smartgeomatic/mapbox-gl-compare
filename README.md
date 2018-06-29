mapbox-gl-compare
---

Swipe and sync between two maps

![Swipe example](http://i.imgur.com/MvjwVLu.gif)

Map movements are synced with [mapbox-gl-sync-move](https://github.com/mapbox/mapbox-gl-sync-move).

### Usage

```js
var before = new mapboxgl.Map({
  container: 'before', // Container ID
  style: 'mapbox://styles/mapbox/light-v9'
});

var after = new mapboxgl.Map({
  container: 'after', // Container ID
  style: 'mapbox://styles/mapbox/dark-v9'
});

var compare = new mapboxgl.Compare(before, after, {
  mousemove: true // Optional. Set to true to enable swiping during cursor movement.
});

compare.destroy() //cleans listeners and remove swiper
```

Demo: https://www.mapbox.com/mapbox-gl-js/example/mapbox-gl-compare/

### Developing

    npm install & npm start & open http://localhost:9966

You'll need a [Mapbox access token](https://www.mapbox.com/help/create-api-access-token/) stored in localstorage. Set it via

    localStorage.setItem('MapboxAccessToken', '<TOKEN HERE>');

### Testing

Tests require an MapboxAccessToken env variable to be set.

    export MapboxAccessToken="YOUR ACCESS TOKEN"

Lastly, run the test command from the console:

    npm test
