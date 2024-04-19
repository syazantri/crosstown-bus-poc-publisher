# Reflection Tutorial 8 - Publisher
Syazantri Salsabila - 2206029443 - AdvPro B

a. How many data your publisher program will send to the message broker in one run?  
> Ada 5 data yang bakal disend dalam sekali run, bisa dihitung dari berapa banyak jumlah ```_ = p.publish_event("user_created".to_owned(), UserCreatedEventMessage { user_id: "1".to_owned(), user_name: "somethingsomething".to_owned() });``` yang ada.

<br>

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean? 
> Kalau urlnya sama, berarti AMPQ brokernya publisher dan subscriber menggunakan koneksi yang sama, atau bisa dikatakan juga kalau publisher dan subscriber terkoneksi dalam message broker yang sama.

<br>

c. Running RabbitMQ as message broker.
![Commit 3 screen capture](assets/images/commit3.png) 

<br>

d. Sending and processing event.
![Commit 4 screen capture](assets/images/commit4.png)
Ini merupakan tampak console ketika menjalankan (```cargo run```) subscriber lalu publisher setelah menggunakan RabbitMQ. Dapat terlihat bahwa saat menjalankan publisher, dia bakal ngirimin 5 event ke message broker yang nantinya bakal diconsume sama subscriber.

<br>

e. Monitoring chart based on publisher.
![Commit 5 screen capture](assets/images/commit5.png)
Grafik yang terlihat terdapat spikenya adalah grafik Message Rates. Grafik tersebut akan menggambarkan seberapa banyak/cepat message dikirim publisher dalam 1 menit terakhir. Semakin banyak, grafik (spike) nya akan semakin tinggi. Dalam kasus screenshot saya ini memang disetting dalam 1 menit terakhir, tetapi bisa juga disetting untuk range waktu lainnya