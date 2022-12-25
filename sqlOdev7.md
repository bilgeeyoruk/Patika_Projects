####Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.
1.film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
```sql
SELECT rating FROM film GROUP BY rating;
```
2.film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
```sql

```
3. customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?
```sql
SELECT replacement_cost,COUNT(*) FROM film GROUP BY replacement_cost HAVING COUNT(*) > 50;
```
4. city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra
```sql
SELECT store_id,COUNT(customer_id) FROM customer GROUP BY store_id;
```
en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
```sql
SELECT country_id,COUNT(country_id) FROM city GROUP BY country_id  ORDER BY COUNT(country_id) DESCLIMIT 1;
```
