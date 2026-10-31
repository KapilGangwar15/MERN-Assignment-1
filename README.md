# Assignment-1 What happens between typing a URL and seeing the page?

1. Cache check: Browser pehle apne cache me chek karta hai ki uske paas yaad me IP address to nahi hai.
2. DNS lookup: Agar cache me nahi milta, toh browser DNS server se domain name (`example.com`) ko IP address me convert karne ko kehta hai.
3. TCP connection: IP address milne ke baad, browser server ke sath TCP connection banata hai (3-way handshake).
4. TLS handshake (HTTPS): Agar site HTTPS hai, toh browser server ke sath encryption ke liye TLS handshake karta hai.
5. HTTP request: Ab browser server ke paas ek HTTP request bhejta hai, jaise `GET /index.html`.
6. Server processing: Server request ko handle karta hai, database (jaise MongoDB in MERN) se data liye toh liye, aur ek response banata hai (status code 200 OK + HTML file).
7. Browser rendering: Browser ko HTML milta hai, toh:
    - HTML ko DOM (Document Object Model) me parse karta hai.
    - CSS ko CSSOM (CSS Object Model) me banata hai.
    - DOM + CSSOM = Render Tree banata hai.
    - Layout calculate karta hai, screen pe paint karta hai.
    - JavaScript ko run karta hai jo page ko dynamic bana deta hai (React me frontend hota hai).
8. Result:Akhir me tu apna webpage dekh pata hai.
Simple flow diagram (apne sabdo me)
URL type → Cache check → DNS (domain → IP) → TCP connect → TLS (HTTPS) → HTTP GET request → Server response (HTML) → Browser render (DOM + CSSOM) → Page display

