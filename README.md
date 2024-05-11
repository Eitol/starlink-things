# starlink-things

¿Como hace los speed test?
Hace 8 peticiones seguidas a esta url que es un bucket r2 de cf:

Para medir la velocidad de descarga:
curl --path-as-is -i -s -k -X $'GET' \
    -H $'User-Agent: Dalvik/2.1.0 (Linux; U; Android 13; Pixel 7 Build/TQ2B.230505.005.A1)' -H $'Host: pub-bd7380c3ba9d4093813adcbf37920c1e.r2.dev' -H $'Connection: close' -H $'Accept-Encoding: gzip, deflate, br' \
    $'https://pub-bd7380c3ba9d4093813adcbf37920c1e.r2.dev/random-250MB.bin'


Para medir la velocidad de subida:

Sube un gran fichero a esta url y el servidor reporta "Unauthorized" ¿Estará abusando del servicio de cloudflare xD?:

POST /random-250MB.bin HTTP/1.1
Host: pub-bd7380c3ba9d4093813adcbf37920c1e.r2.dev
Content-Type: text/plain
Content-Length: 25166848
Accept-Encoding: gzip, deflate, br
User-Agent: okhttp/4.9.2
Connection: close

