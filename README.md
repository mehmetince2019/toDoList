# toDoList

her sabah güne baslarken kagit kalem alip yapiacaklar  listesi yapiyorum 
önceden onenote veya jooplin'i  acip  sonra bos bir word sayfasi acip o gün yapilacaklari liste yapiyordum. 
simdi bunu pratik sekilde cep tel ekraninda görmek istiyorum.  görevler tamamlandikca tik atacagim 

amac / tanim  :
o gün yapilmasi gerekenleri listeleyecek  bir uygulama . 

Platorm:
Android 


veri girisi pratik olmali

bugün yapilacaklar bölümü  

tamamlananlarin üstü cizilip asagi alinacak ..  
aksam tamamlananlar asive tamamlanmayanlar ana listeye geri islenecek  


---------------------

sistem databasi olarak php mysql kullaniyor 
bunun icin bir websitesi yaptim 

1- td_demo php dosylarinin oldugu zip dosyasini indirin... 
2- sitenizde "td_demo" isimli bir folder olusturup tüm dosyalari icine yükleyin 
3- herbir dosyayi acip (gerekli ise)  xx li bölümleri kendinize göre uyarlayin
2- web sitenizde database olusturun ( db , user ve passwd yi not alin) 
3- sql dosyasini pho myadmin icinde calistirin


--------------------

demo :   
https://ince.one/td_demo/index1.php
admin
1234


-------


sql dosyasi 


-- phpMyAdmin SQL Dump
-- version 5.2.1
-- https://www.phpmyadmin.net/
--
-- Anamakine: localhost:3306
-- Üretim Zamanı: 31 Tem 2024, 08:53:23
-- Sunucu sürümü: 10.3.39-MariaDB-0ubuntu0.20.04.2
-- PHP Sürümü: 8.3.6

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Veritabanı: `td_db`
--

-- --------------------------------------------------------

--
-- Tablo için tablo yapısı `todo`
--

CREATE TABLE `todo` (
  `id` int(2) NOT NULL,
  `thema` varchar(5000) DEFAULT NULL,
  `message` mediumtext DEFAULT NULL,
  `is_normal_and_current` tinyint(1) DEFAULT 0,
  `is_urgent` tinyint(1) DEFAULT 0,
  `is_later` tinyint(1) DEFAULT 0,
  `is_done` tinyint(1) DEFAULT 0
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

--
-- Tablo döküm verisi `todo`
--

INSERT INTO `todo` (`id`, `thema`, `message`, `is_normal_and_current`, `is_urgent`, `is_later`, `is_done`) VALUES
(61, 'learn.microsoft.com -- m365-endpoint-administrator', '\r\nmehmet\r\nhttps://learn.microsoft.com/de-de/credentials/certifications/m365-endpoint-administrator/\r\nda geht es ungefähr um die Aufgaben, die ich gerade umrissen habe.\r\n\r\n\r\nsami \r\nhttps://learn.microsoft.com/de-de/credentials/certifications/m365-administrator-expert/\r\n\r\n\r\n\r\n\r\n---------\r\nhttps://learn.microsoft.com/de-de/credentials/certifications/windows-server-hybrid-administrator/', 0, 0, 0, 0),0, 0, 0),
(424, '10 agustos dump - 12 augustos EXAM\r\n', '', 0, 0, 0, 0);

-- --------------------------------------------------------

--
-- Tablo için tablo yapısı `todo_done`
--

CREATE TABLE `todo_done` (
  `id` int(11) NOT NULL,
  `thema` varchar(5000) DEFAULT NULL,
  `message` mediumtext DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

--
-- Tablo döküm verisi `todo_done`
--

INSERT INTO `todo_done` (`id`, `thema`, `message`) VALUES
(20, 'vortrag - freitag - 2023 sommer 4. daten modellrierung', 'Oku West 1 LF -1-5 -- 577\r\nOku West 2-LF 6.9  \r\n\r\n\r\nhttps://www.youtube.com/watch?v=ugD5_hZ3FHs&list=PLdvbL9al8P8GC3s6xbT1W9Aix9_KjA-Sl&index=7\r\n\r\nhttps://acikders.ankara.edu.tr/pluginfile.php/59402/mod_resource/content/0/Veritaban%C4%B1%20ve%20Y%C3%B6netim%20Sistemleri%20Sunum%204.pdf\r\n\r\nhttp://sibelsomyurek.com/veritabani/ders_notlari.html\r\n\r\n\r\n\r\n Aufgabe 4.1: ERM, Beziehungen und Kardinalitäten\r\n Aufgabe 4.2: Relationenschema (Attribute, Primär- und Fremdschlüssel)\r\n\r\nDaten formate \r\ndaten struktur\r\nDATENMODELLIERUNG\r\ndatenstruktur\r\n\r\n-- aufgabe : anlage 9 ergänzt werden \r\n\r\n\r\n\r\n\r\n\r\n\r\nXML \r\nCSV\r\nJSON\r\n\r\nrelationes datenbak .. verwaltet werden\r\nnedir relationes datenbank\r\nkac tip datenbank ..var ?\r\n\r\nattribut \r\nentität  demis \r\n\r\niliiskiler \r\n1 1\r\n1 n \r\nn n  ( n m ) \r\n\r\nexceldeki sutun... ne oluyordu ...\r\nsatir ... ? \r\n\r\n\r\ncsv da mitarbiter i vermis \r\nne ayrinti var ? ne görüyoruz anlagede okuyalim \r\n\r\nid \r\nnachname \r\nvorname \r\nalter\r\nabteilung\r\n1, musterman max 33 admin \r\n6 musterman jule personal \r\nyapi sql deki insert into ya benziyor \r\n-------------\r\njson projekt  .. te ne var \r\np id   333 \r\nname \r\nkosten \r\naktuere \r\n\r\nsonra tekrar ediyor .. 2. item sanki \r\nid \r\nname \r\nkosten \r\n\r\nköseli parentez , süslü parantez \r\niki nokt aüst üste kullanmis \r\n\r\n----\r\nxml yapisi ve verilen veriler nele peki \r\n\r\n<> icinde hardware demis \r\nönce laptop demis \r\nsonra laptop id -- html taglari kullanmis.  laptop id verisini yani 222 yi gösterdigi yerde \r\n\r\nayni sekild ehtml tagi acmis icine marke yazmis kapatmis \r\n\r\nyani 3. elementimis laptop \r\nözellilkeri \r\nmarka \r\nmodel \r\nos \r\nkosten \r\nkaufjahr \r\nbezitser\r\n\r\nbunlari yazdim ... veriyi okumayi ögrnmek icin \r\nsoruya bakarsak bu kismi yazma demis aslinda \r\nzaten doldurulacak yerde de bu kadar veri yazacak bosluk yok \r\ngenl sormus \r\nbu tarz sorularda hep bu cümle gelir \r\nattributlari yazmasan da olur diye\r\n\r\n\r\nanlage 9 erm yazan sekle bakalim \r\n3 tane dikdörtgen .. icinde mitarbeiter laptop ve projekt yazili \r\n\r\nbundan sunu aniyoruz bu dikdortgenler arasi iliski yi sematize eddecegiz \r\nhangisinden hangisine cizgi cekilecek `\r\niliski.. sekli 1 to 1 \r\n1 to n \r\nn to n lerden birini yazcagiz \r\n\r\nsoruyu okuyalim \r\nSie das in der Anlage 9 dargestellte ERM um sinnvolle Beziehungen, Kardinalitâten und um eine weitere  Entitât.\r\nbir weitre antitäti bulmamiz gerekiyor .. \r\nve sekle eklememiz\r\nve iliskisini belirtmemiz \r\n\r\n\r\nmitarbeter... da abteilung var..\r\n\r\n\r\n\r\n\r\n\r\n\r\n\r\n');

-- --------------------------------------------------------

--
-- Tablo için tablo yapısı `todo_spaeter`
--

CREATE TABLE `todo_spaeter` (
  `id` int(11) NOT NULL,
  `thema` varchar(5000) DEFAULT NULL,
  `message` mediumtext DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

--
-- Tablo döküm verisi `todo_spaeter`
--

INSERT INTO `todo_spaeter` (`id`, `thema`, `message`) VALUES
(2, 'Veeam- lern', 'backup\r\nhttps://mega.nz/fm/Rm5AjQgC\r\n\r\n\r\n\r\n\r\nhttps://www.youtube.com/watch?v=wjIM7XErbAM&list=PLx9CclV47ioiUfzngSqZEb5nrM8WL7-Sq&index=4\r\n\r\n\r\nhttps://www.youtube.com/watch?v=tTfJ4nrvjhk&list=PLDUOF2Be-kzllMebBK2gcB8i5m-4iDZBT\r\n\r\nhttps://www.youtube.com/watch?v=IZNTU6HmYuc\r\n\r\nhttps://www.youtube.com/results?search_query=veaam+dersleri');

-- --------------------------------------------------------

--
-- Tablo için tablo yapısı `users`
--

CREATE TABLE `users` (
  `id` int(11) NOT NULL,
  `username` varchar(50) NOT NULL,
  `password` varchar(50) NOT NULL,
  `email` varchar(100) NOT NULL,
  `zor_sorular` tinyint(1) DEFAULT 0
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

--
-- Tablo döküm verisi `users`
--

INSERT INTO `users` (`id`, `username`, `password`, `email`, `zor_sorular`) VALUES
(1, 'admin', '1234', '', 0);

--
-- Dökümü yapılmış tablolar için indeksler
--

--
-- Tablo için indeksler `todo`
--
ALTER TABLE `todo`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `id` (`id`);

--
-- Tablo için indeksler `todo_done`
--
ALTER TABLE `todo_done`
  ADD PRIMARY KEY (`id`);

--
-- Tablo için indeksler `todo_spaeter`
--
ALTER TABLE `todo_spaeter`
  ADD PRIMARY KEY (`id`);

--
-- Tablo için indeksler `users`
--
ALTER TABLE `users`
  ADD PRIMARY KEY (`id`);

--
-- Dökümü yapılmış tablolar için AUTO_INCREMENT değeri
--

--
-- Tablo için AUTO_INCREMENT değeri `todo`
--
ALTER TABLE `todo`
  MODIFY `id` int(2) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=425;

--
-- Tablo için AUTO_INCREMENT değeri `todo_done`
--
ALTER TABLE `todo_done`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=422;

--
-- Tablo için AUTO_INCREMENT değeri `todo_spaeter`
--
ALTER TABLE `todo_spaeter`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=368;

--
-- Tablo için AUTO_INCREMENT değeri `users`
--
ALTER TABLE `users`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=5;
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
