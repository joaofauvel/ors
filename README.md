# ORS
Simple [openrouteservice](https://openrouteservice.org/) client.

## Installation
`pip install ors`

## Usage
```python
>>> import ors

>>> ctx = ors.context(api_key="API-KEY")
>>> client = ors.client(ctx)

>>> client(
...     ors.isochrones(locations=[(8.681495,49.41461)], range_=[300])
... )
{'type': 'FeatureCollection', 'bbox': [8.664521, 49.402801, 8.700767, 49.428668], 'features': [{'type': 'Feature', 'properties': {'group_index': 0, 'value': 300.0, 'center': [8.681494991825476, 49.41459939191395]}, 'geometry': {'coordinates': [[[8.66455, 49.418885], [8.665519, 49.410051], [8.66545, 49.409698], [8.670824, 49.405706], [8.678161, 49.402824], [8.678288, 49.402801], [8.685186, 49.407663], [8.691985, 49.410694], [8.700348, 49.413689], [8.700767, 49.413778], [8.700693, 49.41413], [8.694411, 49.418176], [8.693387, 49.420158], [8.693259, 49.4204], [8.692927, 49.420864], [8.692914, 49.42088], [8.687973, 49.424483], [8.68401, 49.428168], [8.683386, 49.428588], [8.683218, 49.428548], [8.67748, 49.42736], [8.672785, 49.428668], [8.671039, 49.427832], [8.670745, 49.427625], [8.667844, 49.42021], [8.664951, 49.419278], [8.664736, 49.419261], [8.664521, 49.419244], [8.66455, 49.418885]]], 'type': 'Polygon'}}], 'metadata': {'attribution': 'openrouteservice.org | OpenStreetMap contributors', 'service': 'isochrones', 'timestamp': 1730136926865, 'query': {'profile': 'driving-car', 'locations': [[8.681495, 49.41461]], 'range': [300.0]}, 'engine': {'version': '8.2.0', 'build_date': '2024-10-09T09:23:42Z', 'graph_date': '2024-09-23T14:39:49Z'}}}
```

## Supported services
- [x] Isochrones
- [ ] Directions
- [ ] Export
- [ ] Matrix
- [ ] Snapping
- [ ] Geocode
- [ ] Elevation
- [ ] Optimization

## Next steps
- Support for more services
- Tests
- Data validation
- Fail fast
- Docs
- Refactor API
- CLI interface