# Reflection Tutorial 8 - Publisher
Syazantri Salsabila - 2206029443 - AdvPro B

a. How many data your publisher program will send to the message broker in one run?  
> Ada 5 data yang bakal disend dalam sekali run, bisa dihitung dari berapa banyak jumlah ```_ = p.publish_event("user_created".to_owned(), UserCreatedEventMessage { user_id: "1".to_owned(), user_name: "somethingsomething".to_owned() });``` yang ada.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean? 
> Kalau urlnya sama, berarti AMPQ brokernya publisher dan subscriber menggunakan koneksi yang sama, atau bisa dikatakan juga kalau publisher dan subscriber terkoneksi dalam message broker yang sama.