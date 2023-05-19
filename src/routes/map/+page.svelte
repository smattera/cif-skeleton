<script>
  import { Map, Marker } from '@beyonk/svelte-mapbox'

  let mapComponent

	function onReady() {
    mapComponent.flyTo({center:[40.7127281,-74.0060152]}) 
	}
</script>

<div class="relative top-0 left-0 w-full object-cover -z-[1] h-[75vh]">
<Map accessToken="PUBLIC_MAPBOX_TOKEN"
	style="mapbox://styles/mapbox/outdoors-v11"
  bind:this={mapComponent} 
  on:ready={onReady}
>
	 <Marker lat=-74.0060152 lng=40.7127281 label="NYC" />
</Map>
</div>
