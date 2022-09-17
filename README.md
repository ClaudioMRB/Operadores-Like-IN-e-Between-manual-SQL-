# 			Operadores-Like-IN-e-Between
nota: o operador IN pode ser usado tanto para valores como para tabelas.

[SQL LIKE Operador (w3schools.com)](https://www.w3schools.com/sql/sql_like.asp)



## ------------------------------O SQL LIKE Operator---------------------------

O operador é usado em uma cláusula para procurar um padrão especificado em uma coluna.`LIKE`` WHERE`

Existem dois curingas frequentemente usados em conjunto com o operador:` LIKE`

- O sinal percentual (%) representa zero, um ou vários caracteres
- O sinal de sublinhado (_) representa um único caractere

**Nota:** O MS Access usa um asterisco (*) em vez do sinal percentual (%) e um ponto de interrogação (?) em vez do sublinhado (_).

O sinal percentual e o sublinhado também podem ser usados em combinações!

### COMO a sintaxe

**SELECT** *column1, column2, ...*
**FROM** *table_name*
**WHERE** *columnN* **LIKE** *pattern*;



**Ponta:** Você também pode combinar qualquer número de condições usando ou operadores.` AND``OR`

Aqui estão alguns exemplos mostrando diferentes operadores com curingas '%' e '_':`LIKE`

| LIKE Operator                  | Description                                                  |
| :----------------------------- | :----------------------------------------------------------- |
| WHERE CustomerName LIKE 'a%'   | Finds any values that start with "a"                         |
| WHERE CustomerName LIKE '%a'   | Finds any values that end with "a"                           |
| WHERE CustomerName LIKE '%or%' | Finds any values that have "or" in any position              |
| WHERE CustomerName LIKE '_r%'  | Finds any values that have "r" in the second position        |
| WHERE CustomerName LIKE 'a_%'  | Finds any values that start with "a" and are at least 2 characters in length |
| WHERE CustomerName LIKE 'a__%' | Finds any values that start with "a" and are at least 3 characters in length |
| WHERE ContactName LIKE 'a%o'   | Finds any values that start with "a" and ends with "o"       |

## Banco de dados de demonstração

A tabela abaixo mostra a tabela completa "Clientes" do banco de dados de amostras Northwind:

| CustomerID | CustomerName                         | ContactName          | Address                                        | City            | PostalCode | Country     |
| :--------- | :----------------------------------- | :------------------- | :--------------------------------------------- | :-------------- | :--------: | :---------- |
| 1          | Alfreds Futterkiste                  | Maria Anders         | Obere Str. 57                                  | Berlin          |   12209    | Germany     |
| 2          | Ana Trujillo Emparedados y helados   | Ana Trujillo         | Avda. de la Constitución 2222                  | México D.F.     |   05021    | Mexico      |
| 3          | Antonio Moreno Taquería              | Antonio Moreno       | Mataderos 2312                                 | México D.F.     |   05023    | Mexico      |
| 4          | Around the Horn                      | Thomas Hardy         | 120 Hanover Sq.                                | London          |  WA1 1DP   | UK          |
| 5          | Berglunds snabbköp                   | Christina Berglund   | Berguvsvägen 8                                 | Luleå           |  S-958 22  | Sweden      |
| 6          | Blauer See Delikatessen              | Hanna Moos           | Forsterstr. 57                                 | Mannheim        |   68306    | Germany     |
| 7          | Blondel père et fils                 | Frédérique Citeaux   | 24, place Kléber                               | Strasbourg      |   67000    | France      |
| 8          | Bólido Comidas preparadas            | Martín Sommer        | C/ Araquil, 67                                 | Madrid          |   28023    | Spain       |
| 9          | Bon app'                             | Laurence Lebihans    | 12, rue des Bouchers                           | Marseille       |   13008    | France      |
| 10         | Bottom-Dollar Marketse               | Elizabeth Lincoln    | 23 Tsawassen Blvd.                             | Tsawassen       |  T2F 8M4   | Canada      |
| 11         | B's Beverages                        | Victoria Ashworth    | Fauntleroy Circus                              | London          |  EC2 5NT   | UK          |
| 12         | Cactus Comidas para llevar           | Patricio Simpson     | Cerrito 333                                    | Buenos Aires    |    1010    | Argentina   |
| 13         | Centro comercial Moctezuma           | Francisco Chang      | Sierras de Granada 9993                        | México D.F.     |   05022    | Mexico      |
| 14         | Chop-suey Chinese                    | Yang Wang            | Hauptstr. 29                                   | Bern            |    3012    | Switzerland |
| 15         | Comércio Mineiro                     | Pedro Afonso         | Av. dos Lusíadas, 23                           | São Paulo       | 05432-043  | Brazil      |
| 16         | Consolidated Holdings                | Elizabeth Brown      | Berkeley Gardens 12 Brewery                    | London          |  WX1 6LT   | UK          |
| 17         | Drachenblut Delikatessend            | Sven Ottlieb         | Walserweg 21                                   | Aachen          |   52066    | Germany     |
| 18         | Du monde entier                      | Janine Labrune       | 67, rue des Cinquante Otages                   | Nantes          |   44000    | France      |
| 19         | Eastern Connection                   | Ann Devon            | 35 King George                                 | London          |  WX3 6FW   | UK          |
| 20         | Ernst Handel                         | Roland Mendel        | Kirchgasse 6                                   | Graz            |    8010    | Austria     |
| 21         | Familia Arquibaldo                   | Aria Cruz            | Rua Orós, 92                                   | São Paulo       | 05442-030  | Brazil      |
| 22         | FISSA Fabrica Inter. Salchichas S.A. | Diego Roel           | C/ Moralzarzal, 86                             | Madrid          |   28034    | Spain       |
| 23         | Folies gourmandes                    | Martine Rancé        | 184, chaussée de Tournai                       | Lille           |   59000    | France      |
| 24         | Folk och fä HB                       | Maria Larsson        | Åkergatan 24                                   | Bräcke          |  S-844 67  | Sweden      |
| 25         | Frankenversand                       | Peter Franken        | Berliner Platz 43                              | München         |   80805    | Germany     |
| 26         | France restauration                  | Carine Schmitt       | 54, rue Royale                                 | Nantes          |   44000    | France      |
| 27         | Franchi S.p.A.                       | Paolo Accorti        | Via Monte Bianco 34                            | Torino          |   10100    | Italy       |
| 28         | Furia Bacalhau e Frutos do Mar       | Lino Rodriguez       | Jardim das rosas n. 32                         | Lisboa          |    1675    | Portugal    |
| 29         | Galería del gastrónomo               | Eduardo Saavedra     | Rambla de Cataluña, 23                         | Barcelona       |   08022    | Spain       |
| 30         | Godos Cocina Típica                  | José Pedro Freyre    | C/ Romero, 33                                  | Sevilla         |   41101    | Spain       |
| 31         | Gourmet Lanchonetes                  | André Fonseca        | Av. Brasil, 442                                | Campinas        | 04876-786  | Brazil      |
| 32         | Great Lakes Food Market              | Howard Snyder        | 2732 Baker Blvd.                               | Eugene          |   97403    | USA         |
| 33         | GROSELLA-Restaurante                 | Manuel Pereira       | 5ª Ave. Los Palos Grandes                      | Caracas         |    1081    | Venezuela   |
| 34         | Hanari Carnes                        | Mario Pontes         | Rua do Paço, 67                                | Rio de Janeiro  | 05454-876  | Brazil      |
| 35         | HILARIÓN-Abastos                     | Carlos Hernández     | Carrera 22 con Ave. Carlos Soublette #8-35     | San Cristóbal   |    5022    | Venezuela   |
| 36         | Hungry Coyote Import Store           | Yoshi Latimer        | City Center Plaza 516 Main St.                 | Elgin           |   97827    | USA         |
| 37         | Hungry Owl All-Night Grocers         | Patricia McKenna     | 8 Johnstown Road                               | Cork            |            | Ireland     |
| 38         | Island Trading                       | Helen Bennett        | Garden House Crowther Way                      | Cowes           |  PO31 7PJ  | UK          |
| 39         | Königlich Essen                      | Philip Cramer        | Maubelstr. 90                                  | Brandenburg     |   14776    | Germany     |
| 40         | La corne d'abondance                 | Daniel Tonini        | 67, avenue de l'Europe                         | Versailles      |   78000    | France      |
| 41         | La maison d'Asie                     | Annette Roulet       | 1 rue Alsace-Lorraine                          | Toulouse        |   31000    | France      |
| 42         | Laughing Bacchus Wine Cellars        | Yoshi Tannamuri      | 1900 Oak St.                                   | Vancouver       |  V3F 2K1   | Canada      |
| 43         | Lazy K Kountry Store                 | John Steel           | 12 Orchestra Terrace                           | Walla Walla     |   99362    | USA         |
| 44         | Lehmanns Marktstand                  | Renate Messner       | Magazinweg 7                                   | Frankfurt a.M.  |   60528    | Germany     |
| 45         | Let's Stop N Shop                    | Jaime Yorres         | 87 Polk St. Suite 5                            | San Francisco   |   94117    | USA         |
| 46         | LILA-Supermercado                    | Carlos González      | Carrera 52 con Ave. Bolívar #65-98 Llano Largo | Barquisimeto    |    3508    | Venezuela   |
| 47         | LINO-Delicateses                     | Felipe Izquierdo     | Ave. 5 de Mayo Porlamar                        | I. de Margarita |    4980    | Venezuela   |
| 48         | Lonesome Pine Restaurant             | Fran Wilson          | 89 Chiaroscuro Rd.                             | Portland        |   97219    | USA         |
| 49         | Magazzini Alimentari Riuniti         | Giovanni Rovelli     | Via Ludovico il Moro 22                        | Bergamo         |   24100    | Italy       |
| 50         | Maison Dewey                         | Catherine Dewey      | Rue Joseph-Bens 532                            | Bruxelles       |   B-1180   | Belgium     |
| 51         | Mère Paillarde                       | Jean Fresnière       | 43 rue St. Laurent                             | Montréal        |  H1J 1C3   | Canada      |
| 52         | Morgenstern Gesundkost               | Alexander Feuer      | Heerstr. 22                                    | Leipzig         |   04179    | Germany     |
| 53         | North/South                          | Simon Crowther       | South House 300 Queensbridge                   | London          |  SW7 1RZ   | UK          |
| 54         | Océano Atlántico Ltda.               | Yvonne Moncada       | Ing. Gustavo Moncada 8585 Piso 20-A            | Buenos Aires    |    1010    | Argentina   |
| 55         | Old World Delicatessen               | Rene Phillips        | 2743 Bering St.                                | Anchorage       |   99508    | USA         |
| 56         | Ottilies Käseladen                   | Henriette Pfalzheim  | Mehrheimerstr. 369                             | Köln            |   50739    | Germany     |
| 57         | Paris spécialités                    | Marie Bertrand       | 265, boulevard Charonne                        | Paris           |   75012    | France      |
| 58         | Pericles Comidas clásicas            | Guillermo Fernández  | Calle Dr. Jorge Cash 321                       | México D.F.     |   05033    | Mexico      |
| 59         | Piccolo und mehr                     | Georg Pipps          | Geislweg 14                                    | Salzburg        |    5020    | Austria     |
| 60         | Princesa Isabel Vinhoss              | Isabel de Castro     | Estrada da saúde n. 58                         | Lisboa          |    1756    | Portugal    |
| 61         | Que Delícia                          | Bernardo Batista     | Rua da Panificadora, 12                        | Rio de Janeiro  | 02389-673  | Brazil      |
| 62         | Queen Cozinha                        | Lúcia Carvalho       | Alameda dos Canàrios, 891                      | São Paulo       | 05487-020  | Brazil      |
| 63         | QUICK-Stop                           | Horst Kloss          | Taucherstraße 10                               | Cunewalde       |   01307    | Germany     |
| 64         | Rancho grande                        | Sergio Gutiérrez     | Av. del Libertador 900                         | Buenos Aires    |    1010    | Argentina   |
| 65         | Rattlesnake Canyon Grocery           | Paula Wilson         | 2817 Milton Dr.                                | Albuquerque     |   87110    | USA         |
| 66         | Reggiani Caseifici                   | Maurizio Moroni      | Strada Provinciale 124                         | Reggio Emilia   |   42100    | Italy       |
| 67         | Ricardo Adocicados                   | Janete Limeira       | Av. Copacabana, 267                            | Rio de Janeiro  | 02389-890  | Brazil      |
| 68         | Richter Supermarkt                   | Michael Holz         | Grenzacherweg 237                              | Genève          |    1203    | Switzerland |
| 69         | Romero y tomillo                     | Alejandra Camino     | Gran Vía, 1                                    | Madrid          |   28001    | Spain       |
| 70         | Santé Gourmet                        | Jonas Bergulfsen     | Erling Skakkes gate 78                         | Stavern         |    4110    | Norway      |
| 71         | Save-a-lot Markets                   | Jose Pavarotti       | 187 Suffolk Ln.                                | Boise           |   83720    | USA         |
| 72         | Seven Seas Imports                   | Hari Kumar           | 90 Wadhurst Rd.                                | London          |  OX15 4NB  | UK          |
| 73         | Simons bistro                        | Jytte Petersen       | Vinbæltet 34                                   | København       |    1734    | Denmark     |
| 74         | Spécialités du monde                 | Dominique Perrier    | 25, rue Lauriston                              | Paris           |   75016    | France      |
| 75         | Split Rail Beer & Ale                | Art Braunschweiger   | P.O. Box 555                                   | Lander          |   82520    | USA         |
| 76         | Suprêmes délices                     | Pascale Cartrain     | Boulevard Tirou, 255                           | Charleroi       |   B-6000   | Belgium     |
| 77         | The Big Cheese                       | Liz Nixon            | 89 Jefferson Way Suite 2                       | Portland        |   97201    | USA         |
| 78         | The Cracker Box                      | Liu Wong             | 55 Grizzly Peak Rd.                            | Butte           |   59801    | USA         |
| 79         | Toms Spezialitäten                   | Karin Josephs        | Luisenstr. 48                                  | Münster         |   44087    | Germany     |
| 80         | Tortuga Restaurante                  | Miguel Angel Paolino | Avda. Azteca 123                               | México D.F.     |   05033    | Mexico      |
| 81         | Tradição Hipermercados               | Anabela Domingues    | Av. Inês de Castro, 414                        | São Paulo       | 05634-030  | Brazil      |
| 82         | Trail's Head Gourmet Provisioners    | Helvetius Nagy       | 722 DaVinci Blvd.                              | Kirkland        |   98034    | USA         |
| 83         | Vaffeljernet                         | Palle Ibsen          | Smagsløget 45                                  | Århus           |    8200    | Denmark     |
| 84         | Victuailles en stock                 | Mary Saveley         | 2, rue du Commerce                             | Lyon            |   69004    | France      |
| 85         | Vins et alcools Chevalier            | Paul Henriot         | 59 rue de l'Abbaye                             | Reims           |   51100    | France      |
| 86         | Die Wandernde Kuh                    | Rita Müller          | Adenauerallee 900                              | Stuttgart       |   70563    | Germany     |
| 87         | Wartian Herkku                       | Pirkko Koskitalo     | Torikatu 38                                    | Oulu            |   90110    | Finland     |
| 88         | Wellington Importadora               | Paula Parente        | Rua do Mercado, 12                             | Resende         | 08737-363  | Brazil      |
| 89         | White Clover Markets                 | Karl Jablonski       | 305 - 14th Ave. S. Suite 3B                    | Seattle         |   98128    | USA         |
| 90         | Wilman Kala                          | Matti Karttunen      | Keskuskatu 45                                  | Helsinki        |   21240    | Finland     |
| 91         | Wolski                               | Zbyszek              | ul. Filtrowa 68                                | Walla           |   01-012   | Poland      |

## EXEMPLOS SEMELHANTES A SQL

A seguinte instrução SQL seleciona todos os clientes com um CustomerName começando com "a":

### Exemplo

**SELECT** *** FROM** Customers
**WHERE** CustomerName **LIKE** 'a%';

[Experimente você mesmo »](https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like)

A seguinte instrução SQL seleciona todos os clientes com um Nome do Cliente terminando com "a":

### Exemplo

**SELECT * FROM** Customers
**WHERE** CustomerName **LIKE** '%a';

A seguinte instrução SQL seleciona todos os clientes com um CustomerName que tenha "ou" em qualquer posição:

### Exemplo

**SELECT * FROM** Customers
**WHERE** CustomerName **LIKE** '%or%';

A seguinte instrução SQL seleciona todos os clientes com um CustomerName que tenha "r" na segunda posição:

### Exemplo

**SELECT * FROM** Customers

A seguinte instrução SQL seleciona todos os clientes com um CustomerName que começa com "a" e tem pelo menos 3 caracteres de comprimento:

### Exemplo

**SELECT * FROM** Customers

**WHERE** CustomerName **LIKE** 'a__%';

A seguinte instrução SQL seleciona todos os clientes com um ContactName que começa com "a" e termina com "o":

### Exemplo

**SELECT * FROM** Customers
**WHERE** ContactName **LIKE** 'a%o';

A seguinte instrução SQL seleciona todos os clientes com um CustomerName que NÃO começa com "a":

### Exemplo

**SELECT * FROM** Customers
**WHERE** CustomerName **NOT LIKE** 'a%';****

---------------------------------------------------------------------------//----------------------------------------------------------------------------------

## Personagens curinga SQL

Um personagem curinga é usado para substituir um ou mais caracteres em uma sequência.

Personagens curinga são usados com o operador. O operador é usado em uma cláusula para procurar um padrão especificado em uma coluna.` LIKE``LIKE`` WHERE`

### Personagens curinga no acesso a MS

| Symbol | Description                                                | Example                                                      |
| :----- | :--------------------------------------------------------- | :----------------------------------------------------------- |
| *      | Represents zero or more characters                         | bl* finds bl, black, blue, and blob                          |
| ?      | Represents a single character                              | h?t finds hot, hat, and hit                                  |
| []     | Represents any single character within the brackets        | h[oa]t finds hot and hat, but not hit                        |
| !      | Represents any character not in the brackets               | h[!oa]t finds hit, but not hot and hat                       |
| -      | Represents any single character within the specified range | c[a-b]t finds cat and cbt                                    |
| #      | Represents any single numeric character                    | 2#5 finds 205, 215, 225, 235, 245, 255, 265, 275, 285, and 295 |

### Personagens curinga no sql server

| Symbol | Description                                                | Example                                |
| :----- | :--------------------------------------------------------- | :------------------------------------- |
| %      | Represents zero or more characters                         | bl% finds bl, black, blue, and blob    |
| _      | Represents a single character                              | h_t finds hot, hat, and hit            |
| []     | Represents any single character within the brackets        | h[oa]t finds hot and hat, but not hit  |
| ^      | Represents any character not in the brackets               | h[^oa]t finds hit, but not hot and hat |
| -      | Represents any single character within the specified range | c[a-b]t finds cat and cbt              |

Todos os curingas também podem ser usados em combinações!

Aqui estão alguns exemplos mostrando diferentes operadores com curingas '%' e '_':`LIKE`

| LIKE Operator                  | Description                                                  |
| :----------------------------- | :----------------------------------------------------------- |
| WHERE CustomerName LIKE 'a%'   | Finds any values that starts with "a"                        |
| WHERE CustomerName LIKE '%a'   | Finds any values that ends with "a"                          |
| WHERE CustomerName LIKE '%or%' | Finds any values that have "or" in any position              |
| WHERE CustomerName LIKE '_r%'  | Finds any values that have "r" in the second position        |
| WHERE CustomerName LIKE 'a__%' | Finds any values that starts with "a" and are at least 3 characters in length |
| WHERE ContactName LIKE 'a%o'   | Finds any values that starts with "a" and ends with "o"      |

------

## Banco de dados de demonstração

A tabela abaixo mostra a tabela completa "Clientes" do banco de dados de amostras Northwind:

| CustomerID | CustomerName                         | ContactName          | Address                                        | City            | PostalCode | Country     |
| :--------- | :----------------------------------- | :------------------- | :--------------------------------------------- | :-------------- | :--------- | :---------- |
| 1          | Alfreds Futterkiste                  | Maria Anders         | Obere Str. 57                                  | Berlin          | 12209      | Germany     |
| 2          | Ana Trujillo Emparedados y helados   | Ana Trujillo         | Avda. de la Constitución 2222                  | México D.F.     | 05021      | Mexico      |
| 3          | Antonio Moreno Taquería              | Antonio Moreno       | Mataderos 2312                                 | México D.F.     | 05023      | Mexico      |
| 4          | Around the Horn                      | Thomas Hardy         | 120 Hanover Sq.                                | London          | WA1 1DP    | UK          |
| 5          | Berglunds snabbköp                   | Christina Berglund   | Berguvsvägen 8                                 | Luleå           | S-958 22   | Sweden      |
| 6          | Blauer See Delikatessen              | Hanna Moos           | Forsterstr. 57                                 | Mannheim        | 68306      | Germany     |
| 7          | Blondel père et fils                 | Frédérique Citeaux   | 24, place Kléber                               | Strasbourg      | 67000      | France      |
| 8          | Bólido Comidas preparadas            | Martín Sommer        | C/ Araquil, 67                                 | Madrid          | 28023      | Spain       |
| 9          | Bon app'                             | Laurence Lebihans    | 12, rue des Bouchers                           | Marseille       | 13008      | France      |
| 10         | Bottom-Dollar Marketse               | Elizabeth Lincoln    | 23 Tsawassen Blvd.                             | Tsawassen       | T2F 8M4    | Canada      |
| 11         | B's Beverages                        | Victoria Ashworth    | Fauntleroy Circus                              | London          | EC2 5NT    | UK          |
| 12         | Cactus Comidas para llevar           | Patricio Simpson     | Cerrito 333                                    | Buenos Aires    | 1010       | Argentina   |
| 13         | Centro comercial Moctezuma           | Francisco Chang      | Sierras de Granada 9993                        | México D.F.     | 05022      | Mexico      |
| 14         | Chop-suey Chinese                    | Yang Wang            | Hauptstr. 29                                   | Bern            | 3012       | Switzerland |
| 15         | Comércio Mineiro                     | Pedro Afonso         | Av. dos Lusíadas, 23                           | São Paulo       | 05432-043  | Brazil      |
| 16         | Consolidated Holdings                | Elizabeth Brown      | Berkeley Gardens 12 Brewery                    | London          | WX1 6LT    | UK          |
| 17         | Drachenblut Delikatessend            | Sven Ottlieb         | Walserweg 21                                   | Aachen          | 52066      | Germany     |
| 18         | Du monde entier                      | Janine Labrune       | 67, rue des Cinquante Otages                   | Nantes          | 44000      | France      |
| 19         | Eastern Connection                   | Ann Devon            | 35 King George                                 | London          | WX3 6FW    | UK          |
| 20         | Ernst Handel                         | Roland Mendel        | Kirchgasse 6                                   | Graz            | 8010       | Austria     |
| 21         | Familia Arquibaldo                   | Aria Cruz            | Rua Orós, 92                                   | São Paulo       | 05442-030  | Brazil      |
| 22         | FISSA Fabrica Inter. Salchichas S.A. | Diego Roel           | C/ Moralzarzal, 86                             | Madrid          | 28034      | Spain       |
| 23         | Folies gourmandes                    | Martine Rancé        | 184, chaussée de Tournai                       | Lille           | 59000      | France      |
| 24         | Folk och fä HB                       | Maria Larsson        | Åkergatan 24                                   | Bräcke          | S-844 67   | Sweden      |
| 25         | Frankenversand                       | Peter Franken        | Berliner Platz 43                              | München         | 80805      | Germany     |
| 26         | France restauration                  | Carine Schmitt       | 54, rue Royale                                 | Nantes          | 44000      | France      |
| 27         | Franchi S.p.A.                       | Paolo Accorti        | Via Monte Bianco 34                            | Torino          | 10100      | Italy       |
| 28         | Furia Bacalhau e Frutos do Mar       | Lino Rodriguez       | Jardim das rosas n. 32                         | Lisboa          | 1675       | Portugal    |
| 29         | Galería del gastrónomo               | Eduardo Saavedra     | Rambla de Cataluña, 23                         | Barcelona       | 08022      | Spain       |
| 30         | Godos Cocina Típica                  | José Pedro Freyre    | C/ Romero, 33                                  | Sevilla         | 41101      | Spain       |
| 31         | Gourmet Lanchonetes                  | André Fonseca        | Av. Brasil, 442                                | Campinas        | 04876-786  | Brazil      |
| 32         | Great Lakes Food Market              | Howard Snyder        | 2732 Baker Blvd.                               | Eugene          | 97403      | USA         |
| 33         | GROSELLA-Restaurante                 | Manuel Pereira       | 5ª Ave. Los Palos Grandes                      | Caracas         | 1081       | Venezuela   |
| 34         | Hanari Carnes                        | Mario Pontes         | Rua do Paço, 67                                | Rio de Janeiro  | 05454-876  | Brazil      |
| 35         | HILARIÓN-Abastos                     | Carlos Hernández     | Carrera 22 con Ave. Carlos Soublette #8-35     | San Cristóbal   | 5022       | Venezuela   |
| 36         | Hungry Coyote Import Store           | Yoshi Latimer        | City Center Plaza 516 Main St.                 | Elgin           | 97827      | USA         |
| 37         | Hungry Owl All-Night Grocers         | Patricia McKenna     | 8 Johnstown Road                               | Cork            |            | Ireland     |
| 38         | Island Trading                       | Helen Bennett        | Garden House Crowther Way                      | Cowes           | PO31 7PJ   | UK          |
| 39         | Königlich Essen                      | Philip Cramer        | Maubelstr. 90                                  | Brandenburg     | 14776      | Germany     |
| 40         | La corne d'abondance                 | Daniel Tonini        | 67, avenue de l'Europe                         | Versailles      | 78000      | France      |
| 41         | La maison d'Asie                     | Annette Roulet       | 1 rue Alsace-Lorraine                          | Toulouse        | 31000      | France      |
| 42         | Laughing Bacchus Wine Cellars        | Yoshi Tannamuri      | 1900 Oak St.                                   | Vancouver       | V3F 2K1    | Canada      |
| 43         | Lazy K Kountry Store                 | John Steel           | 12 Orchestra Terrace                           | Walla Walla     | 99362      | USA         |
| 44         | Lehmanns Marktstand                  | Renate Messner       | Magazinweg 7                                   | Frankfurt a.M.  | 60528      | Germany     |
| 45         | Let's Stop N Shop                    | Jaime Yorres         | 87 Polk St. Suite 5                            | San Francisco   | 94117      | USA         |
| 46         | LILA-Supermercado                    | Carlos González      | Carrera 52 con Ave. Bolívar #65-98 Llano Largo | Barquisimeto    | 3508       | Venezuela   |
| 47         | LINO-Delicateses                     | Felipe Izquierdo     | Ave. 5 de Mayo Porlamar                        | I. de Margarita | 4980       | Venezuela   |
| 48         | Lonesome Pine Restaurant             | Fran Wilson          | 89 Chiaroscuro Rd.                             | Portland        | 97219      | USA         |
| 49         | Magazzini Alimentari Riuniti         | Giovanni Rovelli     | Via Ludovico il Moro 22                        | Bergamo         | 24100      | Italy       |
| 50         | Maison Dewey                         | Catherine Dewey      | Rue Joseph-Bens 532                            | Bruxelles       | B-1180     | Belgium     |
| 51         | Mère Paillarde                       | Jean Fresnière       | 43 rue St. Laurent                             | Montréal        | H1J 1C3    | Canada      |
| 52         | Morgenstern Gesundkost               | Alexander Feuer      | Heerstr. 22                                    | Leipzig         | 04179      | Germany     |
| 53         | North/South                          | Simon Crowther       | South House 300 Queensbridge                   | London          | SW7 1RZ    | UK          |
| 54         | Océano Atlántico Ltda.               | Yvonne Moncada       | Ing. Gustavo Moncada 8585 Piso 20-A            | Buenos Aires    | 1010       | Argentina   |
| 55         | Old World Delicatessen               | Rene Phillips        | 2743 Bering St.                                | Anchorage       | 99508      | USA         |
| 56         | Ottilies Käseladen                   | Henriette Pfalzheim  | Mehrheimerstr. 369                             | Köln            | 50739      | Germany     |
| 57         | Paris spécialités                    | Marie Bertrand       | 265, boulevard Charonne                        | Paris           | 75012      | France      |
| 58         | Pericles Comidas clásicas            | Guillermo Fernández  | Calle Dr. Jorge Cash 321                       | México D.F.     | 05033      | Mexico      |
| 59         | Piccolo und mehr                     | Georg Pipps          | Geislweg 14                                    | Salzburg        | 5020       | Austria     |
| 60         | Princesa Isabel Vinhoss              | Isabel de Castro     | Estrada da saúde n. 58                         | Lisboa          | 1756       | Portugal    |
| 61         | Que Delícia                          | Bernardo Batista     | Rua da Panificadora, 12                        | Rio de Janeiro  | 02389-673  | Brazil      |
| 62         | Queen Cozinha                        | Lúcia Carvalho       | Alameda dos Canàrios, 891                      | São Paulo       | 05487-020  | Brazil      |
| 63         | QUICK-Stop                           | Horst Kloss          | Taucherstraße 10                               | Cunewalde       | 01307      | Germany     |
| 64         | Rancho grande                        | Sergio Gutiérrez     | Av. del Libertador 900                         | Buenos Aires    | 1010       | Argentina   |
| 65         | Rattlesnake Canyon Grocery           | Paula Wilson         | 2817 Milton Dr.                                | Albuquerque     | 87110      | USA         |
| 66         | Reggiani Caseifici                   | Maurizio Moroni      | Strada Provinciale 124                         | Reggio Emilia   | 42100      | Italy       |
| 67         | Ricardo Adocicados                   | Janete Limeira       | Av. Copacabana, 267                            | Rio de Janeiro  | 02389-890  | Brazil      |
| 68         | Richter Supermarkt                   | Michael Holz         | Grenzacherweg 237                              | Genève          | 1203       | Switzerland |
| 69         | Romero y tomillo                     | Alejandra Camino     | Gran Vía, 1                                    | Madrid          | 28001      | Spain       |
| 70         | Santé Gourmet                        | Jonas Bergulfsen     | Erling Skakkes gate 78                         | Stavern         | 4110       | Norway      |
| 71         | Save-a-lot Markets                   | Jose Pavarotti       | 187 Suffolk Ln.                                | Boise           | 83720      | USA         |
| 72         | Seven Seas Imports                   | Hari Kumar           | 90 Wadhurst Rd.                                | London          | OX15 4NB   | UK          |
| 73         | Simons bistro                        | Jytte Petersen       | Vinbæltet 34                                   | København       | 1734       | Denmark     |
| 74         | Spécialités du monde                 | Dominique Perrier    | 25, rue Lauriston                              | Paris           | 75016      | France      |
| 75         | Split Rail Beer & Ale                | Art Braunschweiger   | P.O. Box 555                                   | Lander          | 82520      | USA         |
| 76         | Suprêmes délices                     | Pascale Cartrain     | Boulevard Tirou, 255                           | Charleroi       | B-6000     | Belgium     |
| 77         | The Big Cheese                       | Liz Nixon            | 89 Jefferson Way Suite 2                       | Portland        | 97201      | USA         |
| 78         | The Cracker Box                      | Liu Wong             | 55 Grizzly Peak Rd.                            | Butte           | 59801      | USA         |
| 79         | Toms Spezialitäten                   | Karin Josephs        | Luisenstr. 48                                  | Münster         | 44087      | Germany     |
| 80         | Tortuga Restaurante                  | Miguel Angel Paolino | Avda. Azteca 123                               | México D.F.     | 05033      | Mexico      |
| 81         | Tradição Hipermercados               | Anabela Domingues    | Av. Inês de Castro, 414                        | São Paulo       | 05634-030  | Brazil      |
| 82         | Trail's Head Gourmet Provisioners    | Helvetius Nagy       | 722 DaVinci Blvd.                              | Kirkland        | 98034      | USA         |
| 83         | Vaffeljernet                         | Palle Ibsen          | Smagsløget 45                                  | Århus           | 8200       | Denmark     |
| 84         | Victuailles en stock                 | Mary Saveley         | 2, rue du Commerce                             | Lyon            | 69004      | France      |
| 85         | Vins et alcools Chevalier            | Paul Henriot         | 59 rue de l'Abbaye                             | Reims           | 51100      | France      |
| 86         | Die Wandernde Kuh                    | Rita Müller          | Adenauerallee 900                              | Stuttgart       | 70563      | Germany     |
| 87         | Wartian Herkku                       | Pirkko Koskitalo     | Torikatu 38                                    | Oulu            | 90110      | Finland     |
| 88         | Wellington Importadora               | Paula Parente        | Rua do Mercado, 12                             | Resende         | 08737-363  | Brazil      |
| 89         | White Clover Markets                 | Karl Jablonski       | 305 - 14th Ave. S. Suite 3B                    | Seattle         | 98128      | USA         |
| 90         | Wilman Kala                          | Matti Karttunen      | Keskuskatu 45                                  | Helsinki        | 21240      | Finland     |
| 91         | Wolski                               | Zbyszek              | ul. Filtrowa 68                                | Walla           | 01-012     | Poland      |

------



## Usando o % Curinga

A seguinte instrução SQL seleciona todos os clientes com uma cidade começando com "ber":

### Exemplo

**SELECT * FROM** Customers
**WHERE** City **LIKE** 'ber%';

A seguinte instrução SQL seleciona todos os clientes com uma cidade contendo o padrão "es":

### Exemplo

**SELECT * FROM** Customers
**WHERE** City **LIKE** '%es%';

------

## Usando o _ Curinga

A seguinte instrução SQL seleciona todos os clientes com uma cidade começando com qualquer personagem, seguido por "ondon":

### Exemplo

**SELECT * FROM** Customers
**WHERE** City **LIKE** '_ondon';

A seguinte instrução SQL seleciona todos os clientes com uma Cidade começando com "L", seguido por qualquer personagem, seguido por "n", seguido por qualquer personagem, seguido por "on":

### Exemplo

**SELECT * FROM** Customers
**WHERE** City **LIKE** 'L_n_on';

------

## Usando o Curinga [charlista]

A seguinte instrução SQL seleciona todos os clientes com uma cidade começando com "b", "s" ou "p":

### Exemplo

**SELECT * FROM** Customers
**WHERE** City **LIKE** '[bsp]%';

A seguinte instrução SQL seleciona todos os clientes com uma cidade começando com "a", "b" ou "c":

### Exemplo

**SELECT * FROM** Customers
**WHERE** City **LIKE** '[a-c]%';

------

## Using the [!charlist] Wildcard

The two following SQL statements select all customers with a City NOT starting with "b", "s", or "p":

### Example

**SELECT * FROM** Customers
**WHERE** City LIKE '[!bsp]%';

Or:

### Exemplo

**SELECT * FROM** Customers
**WHERE** City **NOT LIKE** '[bsp]%';



## -----------------------------O SQL IN Operador------------------------------

O operador permite especificar vários valores em uma cláusula.`IN`` WHERE`

O operador é uma abreviação para múltiplas condições.`IN`` OR`

### IN Sintaxe

**SELECT** *column_name(s)*
**FROM** *table_name*
**WHERE** *column_name* **IN** (*value1*, *value2*, ...);

ouro:

**SELECT** *column_name(s)*
**FROM** *table_name*
**WHERE** *column_name* **IN** (*SELECT STATEMENT*);

------

## Banco de dados de demonstração

A tabela abaixo mostra a tabela completa "Clientes" do banco de dados de amostras Northwind:

| CustomerID | CustomerName                         | ContactName          | Address                                        | City            | PostalCode | Country     |
| :--------- | :----------------------------------- | :------------------- | :--------------------------------------------- | :-------------- | :--------- | :---------- |
| 1          | Alfreds Futterkiste                  | Maria Anders         | Obere Str. 57                                  | Berlin          | 12209      | Germany     |
| 2          | Ana Trujillo Emparedados y helados   | Ana Trujillo         | Avda. de la Constitución 2222                  | México D.F.     | 05021      | Mexico      |
| 3          | Antonio Moreno Taquería              | Antonio Moreno       | Mataderos 2312                                 | México D.F.     | 05023      | Mexico      |
| 4          | Around the Horn                      | Thomas Hardy         | 120 Hanover Sq.                                | London          | WA1 1DP    | UK          |
| 5          | Berglunds snabbköp                   | Christina Berglund   | Berguvsvägen 8                                 | Luleå           | S-958 22   | Sweden      |
| 6          | Blauer See Delikatessen              | Hanna Moos           | Forsterstr. 57                                 | Mannheim        | 68306      | Germany     |
| 7          | Blondel père et fils                 | Frédérique Citeaux   | 24, place Kléber                               | Strasbourg      | 67000      | France      |
| 8          | Bólido Comidas preparadas            | Martín Sommer        | C/ Araquil, 67                                 | Madrid          | 28023      | Spain       |
| 9          | Bon app'                             | Laurence Lebihans    | 12, rue des Bouchers                           | Marseille       | 13008      | France      |
| 10         | Bottom-Dollar Marketse               | Elizabeth Lincoln    | 23 Tsawassen Blvd.                             | Tsawassen       | T2F 8M4    | Canada      |
| 11         | B's Beverages                        | Victoria Ashworth    | Fauntleroy Circus                              | London          | EC2 5NT    | UK          |
| 12         | Cactus Comidas para llevar           | Patricio Simpson     | Cerrito 333                                    | Buenos Aires    | 1010       | Argentina   |
| 13         | Centro comercial Moctezuma           | Francisco Chang      | Sierras de Granada 9993                        | México D.F.     | 05022      | Mexico      |
| 14         | Chop-suey Chinese                    | Yang Wang            | Hauptstr. 29                                   | Bern            | 3012       | Switzerland |
| 15         | Comércio Mineiro                     | Pedro Afonso         | Av. dos Lusíadas, 23                           | São Paulo       | 05432-043  | Brazil      |
| 16         | Consolidated Holdings                | Elizabeth Brown      | Berkeley Gardens 12 Brewery                    | London          | WX1 6LT    | UK          |
| 17         | Drachenblut Delikatessend            | Sven Ottlieb         | Walserweg 21                                   | Aachen          | 52066      | Germany     |
| 18         | Du monde entier                      | Janine Labrune       | 67, rue des Cinquante Otages                   | Nantes          | 44000      | France      |
| 19         | Eastern Connection                   | Ann Devon            | 35 King George                                 | London          | WX3 6FW    | UK          |
| 20         | Ernst Handel                         | Roland Mendel        | Kirchgasse 6                                   | Graz            | 8010       | Austria     |
| 21         | Familia Arquibaldo                   | Aria Cruz            | Rua Orós, 92                                   | São Paulo       | 05442-030  | Brazil      |
| 22         | FISSA Fabrica Inter. Salchichas S.A. | Diego Roel           | C/ Moralzarzal, 86                             | Madrid          | 28034      | Spain       |
| 23         | Folies gourmandes                    | Martine Rancé        | 184, chaussée de Tournai                       | Lille           | 59000      | France      |
| 24         | Folk och fä HB                       | Maria Larsson        | Åkergatan 24                                   | Bräcke          | S-844 67   | Sweden      |
| 25         | Frankenversand                       | Peter Franken        | Berliner Platz 43                              | München         | 80805      | Germany     |
| 26         | France restauration                  | Carine Schmitt       | 54, rue Royale                                 | Nantes          | 44000      | France      |
| 27         | Franchi S.p.A.                       | Paolo Accorti        | Via Monte Bianco 34                            | Torino          | 10100      | Italy       |
| 28         | Furia Bacalhau e Frutos do Mar       | Lino Rodriguez       | Jardim das rosas n. 32                         | Lisboa          | 1675       | Portugal    |
| 29         | Galería del gastrónomo               | Eduardo Saavedra     | Rambla de Cataluña, 23                         | Barcelona       | 08022      | Spain       |
| 30         | Godos Cocina Típica                  | José Pedro Freyre    | C/ Romero, 33                                  | Sevilla         | 41101      | Spain       |
| 31         | Gourmet Lanchonetes                  | André Fonseca        | Av. Brasil, 442                                | Campinas        | 04876-786  | Brazil      |
| 32         | Great Lakes Food Market              | Howard Snyder        | 2732 Baker Blvd.                               | Eugene          | 97403      | USA         |
| 33         | GROSELLA-Restaurante                 | Manuel Pereira       | 5ª Ave. Los Palos Grandes                      | Caracas         | 1081       | Venezuela   |
| 34         | Hanari Carnes                        | Mario Pontes         | Rua do Paço, 67                                | Rio de Janeiro  | 05454-876  | Brazil      |
| 35         | HILARIÓN-Abastos                     | Carlos Hernández     | Carrera 22 con Ave. Carlos Soublette #8-35     | San Cristóbal   | 5022       | Venezuela   |
| 36         | Hungry Coyote Import Store           | Yoshi Latimer        | City Center Plaza 516 Main St.                 | Elgin           | 97827      | USA         |
| 37         | Hungry Owl All-Night Grocers         | Patricia McKenna     | 8 Johnstown Road                               | Cork            |            | Ireland     |
| 38         | Island Trading                       | Helen Bennett        | Garden House Crowther Way                      | Cowes           | PO31 7PJ   | UK          |
| 39         | Königlich Essen                      | Philip Cramer        | Maubelstr. 90                                  | Brandenburg     | 14776      | Germany     |
| 40         | La corne d'abondance                 | Daniel Tonini        | 67, avenue de l'Europe                         | Versailles      | 78000      | France      |
| 41         | La maison d'Asie                     | Annette Roulet       | 1 rue Alsace-Lorraine                          | Toulouse        | 31000      | France      |
| 42         | Laughing Bacchus Wine Cellars        | Yoshi Tannamuri      | 1900 Oak St.                                   | Vancouver       | V3F 2K1    | Canada      |
| 43         | Lazy K Kountry Store                 | John Steel           | 12 Orchestra Terrace                           | Walla Walla     | 99362      | USA         |
| 44         | Lehmanns Marktstand                  | Renate Messner       | Magazinweg 7                                   | Frankfurt a.M.  | 60528      | Germany     |
| 45         | Let's Stop N Shop                    | Jaime Yorres         | 87 Polk St. Suite 5                            | San Francisco   | 94117      | USA         |
| 46         | LILA-Supermercado                    | Carlos González      | Carrera 52 con Ave. Bolívar #65-98 Llano Largo | Barquisimeto    | 3508       | Venezuela   |
| 47         | LINO-Delicateses                     | Felipe Izquierdo     | Ave. 5 de Mayo Porlamar                        | I. de Margarita | 4980       | Venezuela   |
| 48         | Lonesome Pine Restaurant             | Fran Wilson          | 89 Chiaroscuro Rd.                             | Portland        | 97219      | USA         |
| 49         | Magazzini Alimentari Riuniti         | Giovanni Rovelli     | Via Ludovico il Moro 22                        | Bergamo         | 24100      | Italy       |
| 50         | Maison Dewey                         | Catherine Dewey      | Rue Joseph-Bens 532                            | Bruxelles       | B-1180     | Belgium     |
| 51         | Mère Paillarde                       | Jean Fresnière       | 43 rue St. Laurent                             | Montréal        | H1J 1C3    | Canada      |
| 52         | Morgenstern Gesundkost               | Alexander Feuer      | Heerstr. 22                                    | Leipzig         | 04179      | Germany     |
| 53         | North/South                          | Simon Crowther       | South House 300 Queensbridge                   | London          | SW7 1RZ    | UK          |
| 54         | Océano Atlántico Ltda.               | Yvonne Moncada       | Ing. Gustavo Moncada 8585 Piso 20-A            | Buenos Aires    | 1010       | Argentina   |
| 55         | Old World Delicatessen               | Rene Phillips        | 2743 Bering St.                                | Anchorage       | 99508      | USA         |
| 56         | Ottilies Käseladen                   | Henriette Pfalzheim  | Mehrheimerstr. 369                             | Köln            | 50739      | Germany     |
| 57         | Paris spécialités                    | Marie Bertrand       | 265, boulevard Charonne                        | Paris           | 75012      | France      |
| 58         | Pericles Comidas clásicas            | Guillermo Fernández  | Calle Dr. Jorge Cash 321                       | México D.F.     | 05033      | Mexico      |
| 59         | Piccolo und mehr                     | Georg Pipps          | Geislweg 14                                    | Salzburg        | 5020       | Austria     |
| 60         | Princesa Isabel Vinhoss              | Isabel de Castro     | Estrada da saúde n. 58                         | Lisboa          | 1756       | Portugal    |
| 61         | Que Delícia                          | Bernardo Batista     | Rua da Panificadora, 12                        | Rio de Janeiro  | 02389-673  | Brazil      |
| 62         | Queen Cozinha                        | Lúcia Carvalho       | Alameda dos Canàrios, 891                      | São Paulo       | 05487-020  | Brazil      |
| 63         | QUICK-Stop                           | Horst Kloss          | Taucherstraße 10                               | Cunewalde       | 01307      | Germany     |
| 64         | Rancho grande                        | Sergio Gutiérrez     | Av. del Libertador 900                         | Buenos Aires    | 1010       | Argentina   |
| 65         | Rattlesnake Canyon Grocery           | Paula Wilson         | 2817 Milton Dr.                                | Albuquerque     | 87110      | USA         |
| 66         | Reggiani Caseifici                   | Maurizio Moroni      | Strada Provinciale 124                         | Reggio Emilia   | 42100      | Italy       |
| 67         | Ricardo Adocicados                   | Janete Limeira       | Av. Copacabana, 267                            | Rio de Janeiro  | 02389-890  | Brazil      |
| 68         | Richter Supermarkt                   | Michael Holz         | Grenzacherweg 237                              | Genève          | 1203       | Switzerland |
| 69         | Romero y tomillo                     | Alejandra Camino     | Gran Vía, 1                                    | Madrid          | 28001      | Spain       |
| 70         | Santé Gourmet                        | Jonas Bergulfsen     | Erling Skakkes gate 78                         | Stavern         | 4110       | Norway      |
| 71         | Save-a-lot Markets                   | Jose Pavarotti       | 187 Suffolk Ln.                                | Boise           | 83720      | USA         |
| 72         | Seven Seas Imports                   | Hari Kumar           | 90 Wadhurst Rd.                                | London          | OX15 4NB   | UK          |
| 73         | Simons bistro                        | Jytte Petersen       | Vinbæltet 34                                   | København       | 1734       | Denmark     |
| 74         | Spécialités du monde                 | Dominique Perrier    | 25, rue Lauriston                              | Paris           | 75016      | France      |
| 75         | Split Rail Beer & Ale                | Art Braunschweiger   | P.O. Box 555                                   | Lander          | 82520      | USA         |
| 76         | Suprêmes délices                     | Pascale Cartrain     | Boulevard Tirou, 255                           | Charleroi       | B-6000     | Belgium     |
| 77         | The Big Cheese                       | Liz Nixon            | 89 Jefferson Way Suite 2                       | Portland        | 97201      | USA         |
| 78         | The Cracker Box                      | Liu Wong             | 55 Grizzly Peak Rd.                            | Butte           | 59801      | USA         |
| 79         | Toms Spezialitäten                   | Karin Josephs        | Luisenstr. 48                                  | Münster         | 44087      | Germany     |
| 80         | Tortuga Restaurante                  | Miguel Angel Paolino | Avda. Azteca 123                               | México D.F.     | 05033      | Mexico      |
| 81         | Tradição Hipermercados               | Anabela Domingues    | Av. Inês de Castro, 414                        | São Paulo       | 05634-030  | Brazil      |
| 82         | Trail's Head Gourmet Provisioners    | Helvetius Nagy       | 722 DaVinci Blvd.                              | Kirkland        | 98034      | USA         |
| 83         | Vaffeljernet                         | Palle Ibsen          | Smagsløget 45                                  | Århus           | 8200       | Denmark     |
| 84         | Victuailles en stock                 | Mary Saveley         | 2, rue du Commerce                             | Lyon            | 69004      | France      |
| 85         | Vins et alcools Chevalier            | Paul Henriot         | 59 rue de l'Abbaye                             | Reims           | 51100      | France      |
| 86         | Die Wandernde Kuh                    | Rita Müller          | Adenauerallee 900                              | Stuttgart       | 70563      | Germany     |
| 87         | Wartian Herkku                       | Pirkko Koskitalo     | Torikatu 38                                    | Oulu            | 90110      | Finland     |
| 88         | Wellington Importadora               | Paula Parente        | Rua do Mercado, 12                             | Resende         | 08737-363  | Brazil      |
| 89         | White Clover Markets                 | Karl Jablonski       | 305 - 14th Ave. S. Suite 3B                    | Seattle         | 98128      | USA         |
| 90         | Wilman Kala                          | Matti Karttunen      | Keskuskatu 45                                  | Helsinki        | 21240      | Finland     |
| 91         | Wolski                               | Zbyszek              | ul. Filtrowa 68                                | Walla           | 01-012     | Poland      |

------



## In Operator Exemplos

A seguinte instrução SQL seleciona todos os clientes que estão localizados em "Alemanha", "França" ou "Reino Unido":

### Exemplo

**SELECT * FROM** Customers
**WHERE** Country **IN** ('Germany', 'France', 'UK');

A seguinte instrução SQL seleciona todos os clientes que NÃO estão localizados em "Alemanha", "França" ou "Reino Unido":

### Exemplo

**SELECT * FROM** Customers
**WHERE** Country **NOT IN** ('Germany', 'France', 'UK');

A seguinte instrução SQL seleciona todos os clientes que são dos mesmos países que os fornecedores:

### Exemplo

**SELECT * FROM** Customers
**WHERE** Country **IN** (SELECT Country FROM Suppliers);



## -----------------O SQL BETWEEN (entre) Operador--------------------

O operador seleciona valores dentro de um determinado intervalo. Os valores podem ser números, texto ou datas.`BETWEEN`

O operador é inclusivo: os valores de início e final estão incluídos. `BETWEEN`

### ENTRE a Sintaxe

**SELECT** *column_name(s)*
**FROM** *table_name*
**WHERE** *column_name* **BETWEEN** *value1* **AND** *value2;*

------

## Banco de dados de demonstração

Abaixo está uma seleção da tabela "Produtos" no banco de dados de amostras northwind:

| ProductID | ProductName                  | SupplierID | CategoryID | Unit                | Price |
| :-------- | :--------------------------- | :--------- | :--------- | :------------------ | :---- |
| 1         | Chais                        | 1          | 1          | 10 boxes x 20 bags  | 18    |
| 2         | Chang                        | 1          | 1          | 24 - 12 oz bottles  | 19    |
| 3         | Aniseed Syrup                | 1          | 2          | 12 - 550 ml bottles | 10    |
| 4         | Chef Anton's Cajun Seasoning | 1          | 2          | 48 - 6 oz jars      | 22    |
| 5         | Chef Anton's Gumbo Mix       | 1          | 2          | 36 boxes            | 21.35 |

------

## ENTRE exemplo

A seguinte instrução SQL seleciona todos os produtos com um preço entre 10 e 20:

### Exemplo

**SELECT * FROM** Products
**WHERE** Price **BETWEEN** 10 **AND** 20;

------



## NÃO ENTRE exemplo

Para exibir os produtos fora da gama do exemplo anterior, use :` NOT BETWEEN`

### Exemplo

**SELECT * FROM** Products
**WHERE** Price **NOT BETWEEN** 10 AND 20;

------

## ENTRE com IN Exemplo

A seguinte instrução SQL seleciona todos os produtos com um preço entre 10 e 20. Além disso; não apresentam produtos com uma categoriaID de 1,2 ou 3:

### Exemplo

**SELECT * FROM** Products
**WHERE** Price **BETWEEN** 10 **AND** 20
**AND** CategoryID **NOT IN** (1,2,3);

[Experimente você mesmo »](https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_between_in)

------

## Entre o exemplo de valores de texto

A seguinte instrução SQL seleciona todos os produtos com um Nome de Produto entre Carnarvon Tigers e Mozzarella di Giovanni:

### Exemplo

**SELECT * FROM** Products
**WHERE** ProductName **BETWEEN** 'Carnarvon Tigers' **AND** 'Mozzarella di Giovanni'
**ORDER BY** ProductName;

A seguinte instrução SQL seleciona todos os produtos com um Nome de Produto entre Carnarvon Tigers e Chef Anton's Cajun Seasoning:

### Exemplo

**SELECT * FROM** Products
**WHERE** ProductName **BETWEEN** "Carnarvon Tigers" **AND** "Chef Anton's Cajun Seasoning"
**ORDER BY** ProductName;

------

## NOT BETWEEN Text Values Example

The following SQL statement selects all products with a ProductName not between Carnarvon Tigers and Mozzarella di Giovanni:

### Exemplo

**SELECT * FROM** Products
**BETWEEN** ProductName **NOT BETWEEN** 'Carnarvon Tigers' **AND** 'Mozzarella di Giovanni'
**ORDER BY** ProductName;

[Experimente você mesmo »](https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_not_between_text)

------

## Tabela de Amostra

Abaixo está uma seleção da tabela "Ordens" no banco de dados de amostras northwind:

| OrderID | CustomerID | EmployeeID | OrderDate | ShipperID |
| :------ | :--------- | :--------- | :-------- | :-------- |
| 10248   | 90         | 5          | 7/4/1996  | 3         |
| 10249   | 81         | 6          | 7/5/1996  | 1         |
| 10250   | 34         | 4          | 7/8/1996  | 2         |
| 10251   | 84         | 3          | 7/9/1996  | 1         |
| 10252   | 76         | 4          | 7/10/1996 | 2         |

------

## Entre datas exemplo

A seguinte instrução SQL seleciona todas as ordens com um OrderDate entre '01-Julho-1996' e '31-Julho-1996':

### Exemplo

**SELECT * FROM** Orders
**WHERE** OrderDate **BETWEEN** #07/01/1996# **AND** #07/31/1996#;

Ou:

### Exemplo

**SELECT * FROM** Orders
**WHERE** OrderDate **BETWEEN** '1996-07-01' **AND** '1996-07-31';



