```
https://www.zoxcell.com
https://www.fujitsu.com/uk/Images/DS_AEM10941_REV1.2.pdf
https://www.cypress.com/products/s6ae10xa-solar-optimized-energy-harvesting-pmic


MAX17710
https://silvertel.com/ag103/?gclid=Cj0KCQjwwuD7BRDBARIsAK_5YhV6iD_N7eH7jcberW3OaNFsW3dR5nChWcJu1x83_hcdzUhrLolDZD0aAsc8EALw_wcB
https://www.eenewspower.com/news/solar-energy-harvester-ic-operates-indoor-lighting-distribution
https://www.we-online.com/catalog/media/o167190v410%20AppNote_Energy-Harvesting_Gleanergy_dc2344afa_EN.pdf

https://www.ti.com/product/BQ25570

MAX17710
https://www.maximintegrated.com/en/products/power/battery-management/MAX17710.html

TPS61023
https://www.youtube.com/watch?v=aNczz2JZcC8
Low Voltage 3108
https://www.youtube.com/watch?v=BOFt1gl_3ZM

How to Order PCB
https://docs.easyeda.com/en/PCB/Order-PCB

สวิทช์
https://www.vcanbuy.com/#/goodsDetailAgent/url?address=detail.1688.com&itemId=623642152570

tactile sw
IGBT - 80N50

Akk truth passes through 3 states
1. Rediculed
	เยอะเย้ย ประชด
2. violently opposed
	ต่อต้าน รุนแรง
3. accepted as be self-evident
	จำใจต้องยอมรับด้วยหลักฐาน จำนนด้วยหลักฐาน


/usr/bin/modem3g/sakis3g --interactive "--sudo" "OTHER= USBMODEM " "USBMODEM= 12d1:1506 " "USBINTERFACE=0" "connect" "--console" "--sudo" "APN=internet" "APN_USER=true" "APN_PASS=true" "SGUI=terminal" "USBINTERFACE=0" "USBMODEM=12d1:1506" "OTHER=USBMODEM" "MODEM=12d1:1506"

/usr/bin/modem3g/sakis3g --sudo OTHER="USBMODEM" USBMODEM="12d1:1506" USBINTERFACE=0 connect

/usr/bin/modem3g/sakis3g disconnect

curl "https://tools.keycdn.com/geo.json?host=8.8.8.8"

ls | xargs -L 1 echo
echo `ls`
for i in `ls` ; do echo $i ; done

for i in `curl "https://tools.keycdn.com/geo.json?host=8.8.8.8"` ; do echo {{$i}} ; done
rate=$(command1 | sed -ne 's/^rate..\([0-9]*\)%.*/\1/p')

traceroute 8.8.8.8
traceroute 8.8.8.8 | sed -ne 's/.*[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+\).*/\1/p'

traceroute 8.8.8.8 | grep ms

traceroute 8.8.8.8 | grep ms | sed 's/.*\([0-9]+\.[0-9]+\.[0-9]+\).*/\1/g'

traceroute -w 1 8.8.8.8 \
| tail -n+2 \
| awk '{ print $2 }' | grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}"

traceroute -w 1 8.8.8.8 | tail -n+2 | awk '{ print $2 }' | grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" | awk '{print YO "$1"}'

traceroute -w 1 8.8.8.8 | tail -n+2 | awk '{ print $2 }' | grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" | while read r; do echo "\"https://tools.keycdn.com/geo.json?host=$r\""; done | xargs curl

{
}

traceroute -w 1 8.8.8.8 | tail -n+2 | awk '{ print $2 }' | grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" | while read r; do echo "\"https://tools.keycdn.com/geo.json?host=$r\""; done | xargs curl | jq .

while read line; do echo "[ERROR] $line"; done

([0-9]{1,3}[\.]){3}[0-9]{1,3}

traceroute -w 1 8.8.8.8 | grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}"


traceroute -w 1 8.8.8.8 | tail -n+2 | awk '{ print $2 }' | grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" | while read r; do echo "\"https://tools.keycdn.com/geo.json?host=$r\""; done | xargs curl | jq '{ip: .data.geo.ip, isp: .data.geo.isp}' > data.txt

traceroute -w 1 8.8.8.8 | tail -n+2 | awk '{ print $2 }' | grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" | while read r; do echo "\"https://tools.keycdn.com/geo.json?host=$r\""; done | xargs curl | jq '{ip: .data.geo.ip, isp: .data.geo.isp, country: .data.geo.country_name }' > data.txt

traceroute -w 1 8.8.8.8 | tail -n+2 | awk '{ print $2 }' | grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" | while read r; do echo "\"https://tools.keycdn.com/geo.json?host=$r\""; done | xargs curl -s | jq '{ip: .data.geo.ip, isp: .data.geo.isp, country: .data.geo.country_name }'

traceroute -w 1 8.8.8.8 \
| tail -n+2 \
| awk '{ print $2 }' \
| grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" \
| while read r; do echo "\"https://tools.keycdn.com/geo.json?host=$r\""; done \
| xargs curl -s \
| jq '{ip: .data.geo.ip, isp: .data.geo.isp, asn: .data.geo.asn,  city: .data.geo.city,  lat: .data.geo.latitude, lng: .data.geo.longitude }'

43.6644,-79.4195

| jq '{ip: .data.geo.ip, isp: .data.geo.isp,  country: .data.geo.country_name }'

  "host": "8.8.8.8",
  "ip": "8.8.8.8",
  "rdns": "dns.google",
  "asn": 15169,
  "isp": "GOOGLE",
  "country_name": "United States",
  "country_code": "US",
  "region_name": null,
  "region_code": null,
  "city": null,
  "postal_code": null,
  "continent_name": "North America",
  "continent_code": "NA",
  "latitude": 37.751,
  "longitude": -97.822,
  "metro_code": null,
  "timezone": "America/Chicago",
  "datetime": "2020-10-04 10:47:07"

13.7442,100.4608
13.7442,100.4608

37.751,-97.822
37.751,-97.822


curl "https://tools.keycdn.com/geo.json?host=203.131.212.198"

country_name
latitude
longitude



```
