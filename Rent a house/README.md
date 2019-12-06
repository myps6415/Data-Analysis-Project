# Rent a house
* Data from [開放台灣民間租屋資料](https://rentalhouse.g0v.ddio.io/download).
* It is just started.
* Hope can find some great entry point.

* 輸出物件在地圖上，因佔太多記憶體使電腦速度減緩
```python=
m = folium.Map(location=[25.0360616, 121.560653], zoom_start=12)

for Latitude_and_longitude in zip(taipei_have_place_df['緯度'], taipei_have_place_df['經度']):
    folium.Circle(
        radius=80,
        location=Latitude_and_longitude,
        popup='The Waterfront',
        color='crimson',
        fill=False,
    ).add_to(m)

m
```