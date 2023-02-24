# gsb-russia

NTv2 transformation for Russia. NTv2 transformation to convert CK42 to WGS84.

## Example

Directly:

```shell
cs2cs -r -W6 +proj=latlong +ellps=krass +nadgrids=@./RUSSIA.gsb,null +to EPSG:4326 examples/a0.txt

59d46'07.938563"N 30d19'30.594478"E 0.000 ГАО_РАН
67d15'59.761229"N 59d19'13.167914"E 0.000 Контроль_верх
67d10'20.889600"N 59d18'57.421261"E 0.000 Контроль_низ
57d11'12.974931"N 75d13'34.437637"E 0.000 Контроль
```

Back:

```shell
cs2cs -W6 -s EPSG:4326 +to +proj=longlat +ellps=krass +nadgrids=@./RUSSIA.gsb,null examples/b0.txt

59d46'07.948200"N       30d19'38.499200"E 0.000 ГАО_РАН
67d15'57.746580"N       59d19'20.495910"E 0.000 Контроль_верх
67d10'18.878550"N       59d19'04.720410"E 0.000 Контроль_низ
57d11'11.007600"N       75d13'37.614000"E 0.000 Контроль
```
