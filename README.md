# benchmark-thanks
Benchmark results of running [produce-320](https://github.com/un-vector-tile-toolkit/produce-320) for African area.

# Computing environment
## PC
- MacBook Pro (13-inch, 2017, Two Thunderbolt 3 ports)
- 2.3GHz Intel Core i5
- 8 GB 2133 MHz LPDDR3
- macOS Mojave 10.14.3

## Storage
- SanDisk Extreme 900 480GB
- exFAT

# Benckmark
## 1. Download planet.osm.pbf
```console
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current                                                                     
                                 Dload  Upload   Total   Spent    Left  Speed                                                                       
100 44.0G  100 44.0G    0     0  3019k      0  4:15:00  4:15:00 --:--:--  846k
```

## 2. Run produce-320/index.js
```console
{
  z: 6
  minx: 22
  miny: 24
  maxx: 41
  maxy: 39
  exportConfigPath: ./osmium-export-config.json
  modifyPath: ./modify.js
  pbfDirPath: pbf
  mbtilesDirPath: mbtiles
  concurrent: 2
  planetPath: ../welt/planet-190304.osm.pbf
  skipMiniPlanet: false
  skipExistingPbf: false
  skipExistingMbtiles: false
}
```

```console
[ 0:00] Started osmium extract
[ 0:00]   osmium version 1.10.0
[ 0:00]   libosmium version 2.15.0
[ 0:00] Command line options and default settings:
[ 0:00]   input options:
[ 0:00]     file name: ../welt/planet-190304.osm.pbf
[ 0:00]     file format:
[ 0:00]   output options:
[ 0:00]     file name: /private/var/folders/pg/64bpwpzx43xcrz16g6f8qh200000gn/T/58a956d5f78393a8be0f6e490860e389.osm.pbf
[ 0:00]     file format: pbf,pbf_compression=false,add_metadata=false
[ 0:00]     generator: osmium/1.10.0
[ 0:00]     overwrite: yes
[ 0:00]     fsync: no
[ 0:00]   strategy options:
[ 0:00]     strategy: smart
[ 0:00]     with history: no
[ 0:00]   other options:
[ 0:00]     config file:
[ 0:00]     output directory:
[ 0:00]
[ 0:00] Extracts:
[ 0:00] [01] Output:      /private/var/folders/pg/64bpwpzx43xcrz16g6f8qh200000gn/T/58a956d5f78393a8be0f6e490860e389.osm.pbf
[ 0:00]      Format:      PBF
[ 0:00]      Description:
[ 0:00]      Envelope:    (-56.25,-40.9798981,56.25,40.9798981)
[ 0:00]      Type:        bbox
[ 0:00]      Geometry:    BOX(-56.25 -40.9798981,56.25 40.9798981)
[ 0:00]
[ 0:00] Additional strategy options:
[ 0:00]   - [types] relation types: multipolygon
[ 0:00]   - [complete-partial-relations] do not complete partial relations
[ 0:00]
[ 0:00] Running 'smart' strategy in three passes...
[ 0:00] First pass (of three)...
[ 9:17] Second pass (of three)...
[15:45] Third pass (of three)...
[31:19] Done.
```

See also: [produce-320.stdout](produce-320.stdout)

