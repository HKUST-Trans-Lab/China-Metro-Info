# China-Metro-Info

通过百度地图API获取全国地铁信息
- [`Visual_metro.ipynb`](https://github.com/HKUST-Trans-Lab/China-Metro-Info/blob/main/Visual_metro.ipynb)
  1. 根据城市编号获取地铁线路与站点经纬度信息；
  2. 根据每两个站点获取详细的中间位置的经纬度信息（用于细化线路）；
  3. 将获取得到的百度站点经纬度信息转为标准的 WGS-84 格式；
  4. 根据经纬度计算距离，支持 Vincenty 和 Haversine 两种计算方式，默认：Vincenty；
  5. 将站点信息与对应经纬度可视化展示 / 以 json 格式保存；
- data
  1. [`guangzhou_Metro.json`](https://github.com/HKUST-Trans-Lab/China-Metro-Info/blob/main/guangzhou_Metro.json)：广州地铁信息；
  2. [`shenzhen_Metro.json`](https://github.com/HKUST-Trans-Lab/China-Metro-Info/blob/main/shenzhen_Metro.json)：深圳地铁信息；
  3. [`Shenzhen_railway.html`](https://github.com/HKUST-Trans-Lab/China-Metro-Info/blob/main/Shenzhen_railway.html)：深圳地铁可视化；
  4. [`Guangzhou_railway.html`](https://github.com/HKUST-Trans-Lab/China-Metro-Info/blob/main/Guangzhou_railway.html)：广州地铁可视化；
  
数据格式
```json
{
"Line_name": ["Line1"],
"Line1":{
  "(0,1)":{"lng":{}, "lat":{}, "dist":{}},
  "(1,2)":{"lng":{}, "lat":{}, "dist":{}},
	"id2name": {"0":"升仙湖"},
	"name2id": {"升仙湖": 0},
	"center_gps": {"0": [104.35384612, 30.78246359]},
	"station_num": 4
  }
}
```
