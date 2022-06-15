# hse22_project
колаб https://colab.research.google.com/drive/1Hh7yOfWvD3B9yhd8biqx9jXgl6XJnMdV?usp=sharing

| Организм              | Число генов| Длина генома | Длина участков с экзонами |	Доля покрытия экзонами	| Участки с zh-score |	Zh-score > 500 |	Длина участков ZH |
| --------------------- | ------------ | ------------------------- | ------------------------ | ------------------ | --------------- | ------------------- | ------------- |
| Gemella_asaccharolyta |	1273.0	     | 1289860.0	               | 1154572.0	              | 89.5	             | 99118           |	1	         | 10        |
| Gemella_haemolysans   |	1831.0	     | 1892523.0	               | 1625794.0	              | 85.9	             | 2011	           | 0	| 0 |
| Gemella_massiliens	  | 1714.0	     | 1804814.0	               | 1543947.0	              | 85.5	             | 803	           | 0	| 0 |
| Gemella_sanguinis	    | 1714.0	     | 1795201.0	               | 1571300.0	              | 87.5	             | 260123	         | 45	| 448 |
| Gemella_palaticanis  | 1875.0	     | 1802210.0	               | 1598667.0	              | 88.7	             | 436	           | 21	| 194 |

<img width="443" alt="Screenshot 2022-06-15 at 17 07 58" src="https://user-images.githubusercontent.com/57015713/173848130-a602546f-7e3b-4b07-a1a4-37e41823e9b2.png">
<img width="446" alt="Screenshot 2022-06-15 at 17 08 07" src="https://user-images.githubusercontent.com/57015713/173848128-368f4519-5df4-48e6-95cf-4ed2cf2551f1.png">
<img width="445" alt="Screenshot 2022-06-15 at 17 08 14" src="https://user-images.githubusercontent.com/57015713/173848124-1e05cda1-6f8d-4b75-b357-0d81e86483ac.png">
<img width="444" alt="Screenshot 2022-06-15 at 17 08 35" src="https://user-images.githubusercontent.com/57015713/173848116-9d69f7cf-f040-41cb-8041-eb5219480855.png">
<img width="446" alt="Screenshot 2022-06-15 at 17 08 40" src="https://user-images.githubusercontent.com/57015713/173847961-a223365f-00a1-4089-a421-4b923c5b1550.png">

Как можно заметить, в этом роде бактерий не очень распространены Z-DNA

Попытаемся найти кластеры

<img width="763" alt="Screenshot 2022-06-15 at 17 15 49" src="https://user-images.githubusercontent.com/57015713/173849828-fdd72da2-3700-4c8b-9edb-395c3e3a0cd8.png">

Пока выглядит все хорошо

Теперь найдем кластеры, у которых есть z-dna хоть в каких-то бактериях

<img width="249" alt="Screenshot 2022-06-15 at 17 18 38" src="https://user-images.githubusercontent.com/57015713/173850245-cd4316ca-76ab-403a-a45c-fb90d4bf5dc3.png">

Ни в одном из кластеров нет z-dna в более, чем одной бактерии
Получается, что таких кластеров, у которых у гомологичных белков сохраняется участки Z-DNA в разных геномах - нет

Визуализация для некоторых кластеров (для оставшихся есть в колабе. иногда зднк находится рядом с протеином, чтобы возможность наличия нескольких днк была больше, но это не помогло)
<img width="1083" alt="Screenshot 2022-06-15 at 22 29 52" src="https://user-images.githubusercontent.com/57015713/173916104-864887de-521a-40f1-97ac-a6612c2453c7.png">
<img width="1084" alt="Screenshot 2022-06-15 at 22 28 49" src="https://user-images.githubusercontent.com/57015713/173916127-75075e12-218a-4a8d-9904-f61ce2de584c.png">
<img width="1093" alt="Screenshot 2022-06-15 at 22 29 38" src="https://user-images.githubusercontent.com/57015713/173916151-0c7bad60-3d83-455b-941c-edb7a3f1fa93.png">


|# Species	|Genes	|Alg.-Conn.	|protein.As.faa	|protein.Ha.faa	|protein.Ma.faa	|protein.Pa.faa	|protein.Sa.faa	|# Zdna	|function	|Z-DNA start	|Z-DNA end	|Z-DNA score	|Cluster start	|Cluster end|
| -------- | -------- | ------------------ | --------------- | ------------------- | ------------- |-------- | ------------------ | --------------- | ------------------- | ------------- |-------- | -------- | ------------------ | ------ |
|5	|5	|1.0	|KXB58042.1	|KXB59111.1	|WP_021752439.1	|WP_179940320.1	|WP_031551257.1	|1	|acyl-CoA |thioesterase	|144956|	144964	|650.9198	|144949	|145449|
|5	|5	|1.0	|KXB58649.1	|KXB61962.1|	WP_062173118.1|	WP_179940720.1	|WP_031550108.1	|1	|cell cycle protein, FtsW/RodA/SpoVE family|	178584	|178596	|2091.0830	|177395	|178600|
|5	|5	|1.0	|KXB58987.1	|KXB57588.1|	WP_072520414.1|	WP_179940754.1	|WP_031552763.1	|1	|thioesterase family protein	|57634	|57647|	3428.5290|	57652	|58035|
|5	|5	|1.0	|KXB57676.1	|KXB58262.1|	WP_062173854.1	|WP_179940864.1	|WP_031551840.1	|1	|tRNA threonylcarbamoyladenosine dehydratase|	112188	|112200	|2943.4610	|112166	|112933"
|5	|5	|1.0	|KXB56657.1	|KXB57232.1	|WP_021753553.1|	WP_179941091.1|	WP_003144216.1|	1	|ribosomal protein L23	|57634|	57647	|3428.5290|	57570	|57851|
|5	|5	|1.0|	KXB56649.1	|KXB57240.1	|WP_021753546.1|	WP_179941101.1|	WP_003144098.1|1	|ribosomal protein L14|	61045|	61055	|980.8116|	61115|	61483|
|5	|5	|1.0	|KXB58523.1	|KXB62137.1	|WP_062173198.1	|WP_179941475.1	|WP_031550272.1	|1	|RNA polymerase sigma factor RpoD|	112188|	112200|	2943.4610|	111135|	112223|
|5	|5	|1.0	|KXB58861.1|	KXB61222.1	|WP_072520432.1|	WP_179941840.1	|WP_031550288.1|	1	|AI-2E family transporter	|107889	|107901|	712.1870	|106778	|107938|


## Квадруплексы
Ни для одного генома квадруплексов не нашлось.

<img width="763" alt="Screenshot 2022-06-15 at 22 55 52" src="https://user-images.githubusercontent.com/57015713/173916057-d5710928-313e-4799-bd91-b651078d6d8a.png">
