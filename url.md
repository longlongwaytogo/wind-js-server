https://nomads.ncep.noaa.gov/cgi-bin/filter_gfs_1p00.pl?dir=%2Fgfs.20230812%2F12%2Fatmos
https://nomads.ncep.noaa.gov/cgi-bin/filter_gfs_1p00.pl?dir=/gfs.20230812/12/atmos

https://nomads.ncep.noaa.gov/cgi-bin/filter_gfs_1p00.pl?
file=gfs.t12z.pgrb2.1p00.f000&lev_10_m_above_ground=on&lev_surface=on&var_TMP=on&var_UGRD=on&var_VGRD=on&leftlon=0&rightlon=360&toplat=90&bottomlat=-90&
dir=%2Fgfs.2023081212


https://nomads.ncep.noaa.gov/cgi-bin/filter_gfs_1p00.pl?
file=gfs.t00z.pgrb2.1p00.f000&lev_10_m_above_ground=on&var_UGRD=on&var_VGRD=on&leftlon=0&rightlon=360&toplat=90&bottomlat=-90&
dir=/gfs.20230812/00/atmos" 
/gfs.20230812/12/atmos'



说明：github上的wind-js-server服务，无法争取访问到数据，主要原因是：
- 数据提供网站，改变了web路径拼接方式
- 缓冲的数据时间和请求时间不一致

// 访问url 获取对应时间的json数据：
timeiso：获取指定日期
searchlimit: 搜索次数限制

http://localhost:7000/nearest?timeIso=20230812&searchLimit=3
http://localhost:7000/nearest?timeIso=20230812&searchLimit=3

转换命令
'converter/bin/grib2json --data --output json-data/2023081212.json --names --compact grib-data/2023081212.f000'