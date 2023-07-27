# cesium heatmap ts

## Project description
```
该库是对开源的cesium heatMap 进行的ts版本的编写，没对做其他的改动
原始cesium heatMap的地址 https://github.com/manuelnas/CesiumHeatmap
原始的heatMap的地址 https://github.com/pa7/heatmap.js
```

## using
```
  const bounds = {
    west: 118.8135860288529,
    east: 118.9463913339937,
    south: 34.982213487281605,
    north: 35.04282012911281
  }
  const obj: IDefalutOption = {
    maxOpacity: 0.8,
    minOpacity: 0.8,
    blur: 0.5,
    gradient: {
      0: 'rgb(68,0,70)',
      0.1: 'rgb(68,0,70)',
      0.2: 'rgb(71,39,113)',
      0.3: 'rgb(56,67,133)',
      0.4: 'rgb(0,93,138)',
      0.5: 'rgb(0,110,137)',
      0.6: 'rgb(0,131,125)',
      0.7: 'rgb(0,159,105)',
      0.8: 'rgb(86,187,85)',
      0.9: 'rgb(180,204,0)',
      1: 'rgb(255,220,0)'
    },
    onExtremaChange: function (obj?: object | undefined): void {
      throw new Error('Function not implemented.')
    },
    radius: 5
  }

  const heatMap = CesiumHeatmapClass.create(viewer, bounds, obj)
  heatMap.setWGS84Data(0, 3, heatmapJson, {
    id: '77H502011CIKM1OL'
  })
  其中heatmapJson的数据结构如下
  cosnt array = [
    {
      "x":纬度,
      "y":经度,
      "value": number
    }
  ]
```

### expectation
```
后续有空再来优化该代码，进行更灵活的使用
```