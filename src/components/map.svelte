<!-- src/components/Map.svelte -->
<script>
  import { onMount } from 'svelte';
  import 'ol/ol.css';
  import Map from 'ol/Map';
  import View from 'ol/View';
  import TileLayer from 'ol/layer/Tile';
  import OSM from 'ol/source/OSM';
  import GeoJSON from 'ol/format/GeoJSON';
  import VectorLayer from 'ol/layer/Vector';
  import VectorSource from 'ol/source/Vector';

  onMount(() => {
    // Create a map
    const map = new Map({
      target: 'map',
      layers: [
        // Add a base layer (OpenStreetMap)
        new TileLayer({
          source: new OSM(),
        }),
        // Add a vector layer for GeoJSON data
        new VectorLayer({
          source: new VectorSource({
            format: new GeoJSON(),
            url: 'https://raw.githubusercontent.com/datasets/geo-countries/master/data/countries.geojson',
          }),
          style: (feature) => ({
            fill: {
              color: '#006a4e', // Set the fill color
            },
            stroke: {
              color: '#006a4e',
              width: 1,
            },
          }),
        }),
      ],
      view: new View({
        center: [0, 0],
        zoom: 2,
      }),
    });
  });
</script>

<div id="map" class="w-full h-screen"></div>
