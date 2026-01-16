# Data Cleaning
## Parsing contact information from the command line

### 1. Extract all email addresses from the text.
**Code:**
```
grep -Eo '[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}' csv/contacts.csv
```
**Output:**
```
augue.ac@hotmail.couk
adipiscing.lacus.ut@protonmail.net
placerat.velit@protonmail.com
sodales.elit@outlook.com
tristique.neque@hotmail.org
purus.in@yahoo.net
a@yahoo.edu
placerat@hotmail.net
pede@protonmail.com
eros.non.enim@icloud.edu
sem.mollis@protonmail.edu
dui.fusce.diam@hotmail.couk
in.consequat@icloud.net
in.lorem.donec@aol.ca
dictum.eu@aol.edu
placerat@hotmail.com
tellus@google.net
luctus.sit@outlook.org
et.magnis@aol.edu
mattis.semper@google.couk
maecenas.libero.est@google.couk
metus.in.lorem@outlook.ca
nullam.velit.dui@aol.couk
vestibulum.ante.ipsum@aol.com
a.dui@protonmail.com
phasellus.fermentum@hotmail.com
massa.non@google.net
nunc.pulvinar@hotmail.ca
id.ante@hotmail.com
nulla.integer.vulputate@icloud.edu
suspendisse.sed.dolor@protonmail.couk
mauris.non@protonmail.net
enim@icloud.couk
dui.nec@yahoo.net
orci.ut@protonmail.com
vel.nisl.quisque@aol.edu
interdum@aol.ca
amet.luctus.vulputate@google.ca
ipsum.dolor.sit@aol.org
nostra.per@aol.com
ac.ipsum@yahoo.ca
eu.enim.etiam@icloud.ca
et.rutrum@icloud.couk
convallis.convallis@yahoo.ca
ipsum.primis@hotmail.org
ac@aol.net
aenean.massa@aol.edu
phasellus@outlook.net
pellentesque.massa@outlook.com
malesuada@outlook.com
massa@icloud.org
id@google.net
lacus.ut@protonmail.couk
cursus.integer@hotmail.com
sem.semper@hotmail.couk
aenean.euismod@yahoo.org
lobortis.class@yahoo.ca
risus.donec@aol.net
sagittis.placerat.cras@yahoo.com
aliquam.adipiscing.lobortis@google.ca
nullam@outlook.net
sed.dictum@aol.net
commodo.hendrerit@hotmail.couk
non.magna@outlook.edu
aenean@google.edu
leo.vivamus.nibh@aol.org
placerat.augue@aol.net
montes.nascetur@icloud.couk
auctor.quis.tristique@hotmail.org
fermentum.fermentum@google.com
sagittis.lobortis@hotmail.edu
posuere.vulputate@icloud.com
semper@icloud.org
sit.amet@protonmail.couk
senectus.et.netus@icloud.com
cubilia.curae.phasellus@hotmail.net
vitae.semper@google.org
aliquet.molestie@protonmail.ca
semper.auctor@yahoo.couk
tristique.senectus@outlook.edu
felis.purus.ac@protonmail.net
mauris.sapien.cursus@icloud.org
posuere.cubilia.curae@protonmail.couk
cras@hotmail.ca
aliquet.odio@yahoo.couk
volutpat.nulla@google.net
convallis.convallis@icloud.ca
etiam.bibendum@hotmail.com
odio@yahoo.edu
eget.nisi@icloud.net
sed.nunc@aol.couk
dui.augue@outlook.org
auctor.nunc@google.org
est.ac@protonmail.edu
at@yahoo.edu
ultricies@yahoo.com
aliquam@hotmail.org
sed.pede.nec@aol.couk
varius.nam.porttitor@protonmail.edu
leo.morbi@aol.com
```

### 2. Extract all phone numbers from the text.
**Code:**
```
grep -Eo '(\+?[0-9]{1,2}[[:space:]-]?)?(\([0-9]{3}\)[[:space:]-]?|[0-9]{3}[[:space:]-]?)[0-9]{3}[[:space:]-]?[0-9]{4}' csv/contacts.csv
```
**Output:**
```
(836) 811-6616
(221) 605-4530
(424) 937-3765
(751) 973-6476
(235) 444-8645
1-216-210-2453
1-498-278-1558
1-668-811-3565
1-400-336-6506
(645) 267-2154
(633) 561-2222
1-946-737-5281
1-323-567-8621
(764) 385-4170
(573) 457-2876
1-703-319-7464
1-388-313-1996
(463) 754-2505
(745) 151-1748
(136) 311-1164
1-445-247-4964
1-832-643-6786
(430) 249-1364
(619) 782-3186
(314) 352-5426
1-781-822-4103
(746) 275-2337
(975) 531-7436
1-406-523-1871
(873) 788-9710
1-762-979-5720
1-648-738-4794
(712) 943-2762
1-152-482-1963
(626) 124-2043
(811) 308-2587
(635) 457-8823
1-897-878-2723
(710) 187-2256
(675) 372-1176
(740) 362-4105
(767) 708-7483
(678) 955-5583
1-324-652-0461
1-614-767-1851
(758) 738-8672
1-403-632-6348
1-628-537-7213
(387) 415-4632
1-236-479-3538
1-111-205-4254
(513) 848-1824
(801) 923-6268
(696) 773-5037
1-298-228-9308
(555) 767-3243
(343) 698-0617
1-852-835-9403
1-127-824-4671
(553) 534-2804
1-485-516-7822
(113) 393-3065
(836) 763-3572
1-745-788-9398
(841) 768-0531
(638) 185-3708
1-613-182-8301
1-555-600-4713
1-517-442-9773
(813) 856-5256
(503) 606-1859
1-379-352-9451
1-638-850-8809
1-867-232-7225
1-452-216-8119
1-615-465-5506
(716) 111-7225
(366) 231-7987
1-938-513-2615
1-607-566-7804
(227) 715-5459
(866) 170-3628
(277) 572-2391
1-756-534-6948
(448) 542-7818
(956) 351-3724
(477) 415-3275
1-869-798-0813
1-868-331-1980
(533) 237-8554
1-301-323-0477
1-788-814-5232
1-681-363-6861
(243) 677-3406
(416) 844-3108
(108) 368-3267
1-455-448-1775
(273) 843-5131
(572) 547-5575
(433) 308-6684
```

### 3. Extract all names that start with the letter ‘J’.
**Code:**
```
grep -Eo '\bJ[A-Za-z]+[[:space:]]+[A-Za-z]+\b' csv/contacts.csv
```
**Output:**
```
James Monroe
John O
Jameson Wallace
Jamal Parsons
Judah Branch
Jaquelyn Le
Jenna Herrera
```

### 4. Extract all street names that contain the word 'St'.
**Code:**
```
grep -Eo '\b[0-9]+[[:space:]][A-Za-z0-9[:space:]]*\bSt\b\.?' csv/contacts.csv
```
**Output:**
```
4035 Mi St.
5917 Erat St.
5182 Penatibus St.
8170 Libero St.
3764 Est St.
6239 Augue St.
627 Consequat St.
6549 Morbi St.
9528 Aliquet St.
2908 Erat St.
7116 Amet St.
5863 At St.
4695 Aliquam St.
8053 Dapibus St.
8548 Sed St.
9709 Quisque St.
```

### 5. Extract the last names of all people.
**Code:**
```
grep -Eo '\b[A-Z][a-z]+[[:space:]]+[A-Z][a-z]+\b' csv/contacts.csv \
  | awk '{print $2}'
```
**Output:**
```
Rios
Patel
Avenue
Mckee
Av
Melendez
St
Carter
Patrick
St
Holmes
Rd
Hodge
St
Monroe
Avenue
Osborn
Rd
Street
Sellers
Rd
Key
Road
Mcintyre
Avenue
Newman
Ochoa
Road
Booker
Mcbride
Rd
Shannon
Avenue
Randolph
Rd
Diaz
Street
Reed
St
Mitchell
St
Langley
Brooks
Rd
Road
Palmer
Rd
Mcintosh
Robertson
Day
Street
Richards
Road
Parks
St
Walsh
Wallace
Street
Gill
Ave
Wise
Street
Chang
Simmons
Av
Oneil
St
Mooney
Castro
St
Velez
Reid
Price
Road
Herman
Hart
Rd
Nunez
Avenue
Mclean
Av
Levy
Cervantes
St
Hyde
Parsons
Rd
Ortega
Avenue
Wilder
Blankenship
Vinson
Morgan
Rd
Torres
Avenue
Thornton
Street
Serrano
Street
Daniel
St
Howe
Ave
Hartman
St
Winters
Rd
Rivers
St
Owen
Rd
Head
Ave
Branch
Ave
Page
Underwood
Rd
Holloway
Ave
Logan
Rd
Rodgers
St
Mcdaniel
Waller
Street
Booker
St
Osborne
Cantu
Avenue
Carney
Rd
Sanders
Rd
Le
Wise
Av
Hawkins
Delaney
Bradshaw
Avery
St
Boone
Rd
Kinney
Drake
St
Meadows
Ave
Cochran
Hansen
Street
Richard
Av
Herrera
Rd
Duffy
Ave
Mcfadden
Rd
West
Cooley
Road
Leblanc
Rd
Marks
```
> This needs to be fixed! Also gives out Names from the address. Needs to be optimixed but no time. :(

### 6. Extract all email domains (part after the @ sign).
**Code:**
```
grep -Eo '[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}' csv/contacts.csv \
  | sed -E 's/.*@//'
```
**Output:**
```
hotmail.couk
protonmail.net
protonmail.com
outlook.com
hotmail.org
yahoo.net
yahoo.edu
hotmail.net
protonmail.com
icloud.edu
protonmail.edu
hotmail.couk
icloud.net
aol.ca
aol.edu
hotmail.com
google.net
outlook.org
aol.edu
google.couk
google.couk
outlook.ca
aol.couk
aol.com
protonmail.com
hotmail.com
google.net
hotmail.ca
hotmail.com
icloud.edu
protonmail.couk
protonmail.net
icloud.couk
yahoo.net
protonmail.com
aol.edu
aol.ca
google.ca
aol.org
aol.com
yahoo.ca
icloud.ca
icloud.couk
yahoo.ca
hotmail.org
aol.net
aol.edu
outlook.net
outlook.com
outlook.com
icloud.org
google.net
protonmail.couk
hotmail.com
hotmail.couk
yahoo.org
yahoo.ca
aol.net
yahoo.com
google.ca
outlook.net
aol.net
hotmail.couk
outlook.edu
google.edu
aol.org
aol.net
icloud.couk
hotmail.org
google.com
hotmail.edu
icloud.com
icloud.org
protonmail.couk
icloud.com
hotmail.net
google.org
protonmail.ca
yahoo.couk
outlook.edu
protonmail.net
icloud.org
protonmail.couk
hotmail.ca
yahoo.couk
google.net
icloud.ca
hotmail.com
yahoo.edu
icloud.net
aol.couk
outlook.org
google.org
protonmail.edu
yahoo.edu
yahoo.com
hotmail.org
aol.couk
protonmail.edu
aol.com
```

### 7. Find all entries where the phone number ends with ‘7’.
**Code:**
```
grep -En '[0-9]{3}-[0-9]{3}-[0-9]{3}7\b' csv/contacts.csv
```
**Output:**
```
92:Aileen Cochran,Ap #806-7090 Massa. St.,sed.nunc@aol.couk,1-301-323-0477
```

### 8. Extract all instances of first names that end with the letter 'e'.
**Code:**
```
grep -Eo '\b[A-Z][a-z]+[[:space:]]+[A-Z][a-z]+\b' csv/contacts.csv \
  | awk '{print $1}' \
  | grep -E 'e$'
```
**Output:**
```
Vance
Reese
Kaye
Augue
Quisque
Bruce
Brielle
Brielle
Curae
Kylie
Reece
Bree
Neque
Curae
Cade
Quisque
Clare
```
