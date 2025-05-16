# Vecka 21: MongoDB Bootcamp

Nedanstående övningar förutsätter att ni gjort allting som gås igenom i filmen [MongoDB : Konfigurering](https://vimeo.com/1084610688/29a61854da?share=copy).

## Övning 1: Skapa en collection
1. Bege dig till dina **Collections** och klicka på knappen **+ Create Database**.
2. Ge din databas namnet **bookstore** och din collection namnet **books** innan du klickar på **create**.
3. Klicka på **Insret Document**, och välj måsvingarna under **View**. Klistra in nedanstående objekt och klicka på **Insert**

```
{
  "_id":{"$oid":"682736d3c46cb203949447bb"},
  "title" : "The spy who came in from the cold",
  "author" : "John le Carré"
}
```


## Övning 2: Custom Role
1. Logga in på MongoDBAtlas och klicka på **Database Access** i menyn till vänster.
2. Klicka på fliken **Custom Roles**.
3. Klicka på den gröna knappen där det står **Add new custom role**.
4. Ge rollen namnet **booksReadAndWrite**.
5. Under **Actions and Roles** klickar du endast i **Collection Roles**, därefter fyller du i namnet på den databas och collection som du skapade i övning 1.

## Övning 3: Database Users
1. Stanna kvar inne på **Database Access**, men klicka nu in dig på fliken **Database Users**.
2. Klicka på den gröna knappen där det står **Add new database user**.
3. I modalen som dyker upp säkerställer du att **Password** är vald **Authentication Method**.
4. Därefter skall du ange username och password för din databasanvändare, för övningens skull låter du **booksUser** både som username och password.
5. En bit längre ner öppnar du upp fliken **Custom Roles**, klickar på **Add Custom Role**, och i dropdownlistan som dyker upp väljer du din nyligen skapade **booksReadAndWrite**-roll.

## Övning 4: MongoDBCompass
1. Klicka på **Clusters** i vänstermenyn.
2. Bredvid namnet på ditt Cluster finns knappen **Connect**. Klicka på den.
3. I modalen som nu öppnades klickar du på **Compass**.
4. Kopiera den **Connection String** som du kan se i del 2 av modalen.
5. Öppna MongoBCompass och klicka på **Add New Connection**.
6. Under **URI** klistrar du in din kopierade **Connection String**. Se till att ersätta ``<db_username>`` och ``db_password`` med de uppgifter som du gav databasanvändaren, alltså **booksUser**, innan du klickar på **Connect**.
7. Klicka dig fram till din collection, därefter klickar du på **Add Data** följt utav **Insert Document**. Klistra in nedanstående objekt och klicka på **Insert**.

```
{
  "_id": {"$oid": "68273baaa32353a34549161c"},
  "title" : "Ulysseus",
  "author" : "James Joyce"
}
```
