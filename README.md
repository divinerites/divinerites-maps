# divinerites-maps

## About

- Small gohugo.io component for managing open street map & google maps.
- Use lazyloading if set in your project.

## Usage

- For OSM : Ceate an OSM map on http://umap.openstreetmap.fr/

### config.toml

File : `config.toml`

```toml
   # Manage maps & coordinates
   [params]
    [params.global]
      [params.global.map]
        [params.global.map.googlemap]
          ## For google map
          map = false
          title = "Google Map"
          url = "Your Google Map URL"
          # Something like "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d83438.06570739325!2d7.419771260195138!3d46.02690216088217!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x478f2beeb905e245%3A0x1a11f40c1e7924a8!2sCamping+Arolla!5e0!3m2!1sfr!2sfr!4v1535693319433"

        [params.global.map.osm]
          ## For Open Street Map
          map = true
          title = "Open Street Map"

          # Creating  url
          mapName = "my_osm_map_123456"  # Your map name on http://umap.openstreetmap.fr/
          scaleControl = "true"
          miniMap = "false"
          scrollWheelZoom = "true"
          zoomControl = "true"
          allowEdit = "false"
          moreControl = "true"
          searchControl = "true"
          tilelayersControl = "null"
          embedControl = "false"
          datalayersControl = "null"
          onLoadPanel = "none"
          captionBar = "false"
          fullscreenControl = "null"
          scale = "12"
          coordX = "46.0410"  # Your real X coordinate
          coordY = "7.4938"  # Your real Y coordinate
```

### HTML template Usage

```go-html-template
<div>
{{ partial "dr_maps.html" . }}
<div>
```

### Credits

- Copyright © 2020 onwards, Didier Divinerites
