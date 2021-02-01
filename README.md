# BEM-opgave
Beskrivelse til hvad sker i Matt Stauffer videoen.

3.50-4.00: Object-oriented code; han beskriver som en masse cirkler af objecter, som alle sammen arbejder sammen.

4.00-4.30: Han taler om decoupling, som gør at en del er mindre knyttet til de andre dele.

4.33-5.20: Single Responsibility Principle, som siger at hver at objecterne skal have deres ansvar, hvilket så gør at når du begynder at dele objecterne og beskriver dem burde du kunne fortælle hvad det obejct gør.
Separation of Concerns er noglelunde det samme hvis der er for mange ting den skal gøre, er det nok for stort og derfor ødelægger idéen om Single Responsibility Principle og Separation of Concerns.

5.20-5.45: Encapsulation, som er at man ikke kun har skilt dem ad men man burde også kunne bruge dem i mange forskellige projekter, hvilket gør at hvis man har for mange snore til og fra forskellige steder kan man ikke trække i det uden at det bliver en stor forvirring.

6.20-8.47: Nicole Sullivan startede med at beskrive at man skulle finde mønstre i objecterne som man gør i back-end code, skulle man også gøre i front-end code.
Så hun kiggede på facebooks layout, og fandt ud af det er fuld af gentagede mønstre 

8.50-11.30:SMACSS (Scalable Modular Architecture for Css)
Base css er vores basic HTML som h1, h2, a, li osv.
Layout css som ville være vores header, footer, sidebar, sections.
Module css er det som Nicole Sullivan også taler om.
State css er hvor man tager et eksisterende module og åbner eller lukker et flag på det module for at fortælle dens state er anderledes på nuværrende tidspunkt.
Theme css er valgfri.

11.30-15.40: BEM er en metode til at navngive klasser så det nemmere giver mening til andre personer fx. 
.{Block}__{Element},
.{Block}__{Element}--{Modifier},
.{Block}--{Modifier}
Block er det vi kaldte module tidligere,
Element er en af Block's børn og så kan man have
Modifier som er på Block eller Elementet
Børnebørn er en dårlig ide at bruge, start hellere en ny Block.

18.30-25.30: Flade selectors grunden til at man de fleste gange har problemmer med css er det på grund af hierarkiet, som er hvilket css der bliver set som vigtigere end andre.
Hvilket betyder at hvis du skriver;
a{
    color: blue;
}
og bagefter skriver klassen på a (awesome)
.awesome{
    color: red;
}
Så vil hierarkiet gøre så a bliver rød.
Hierarkiet vil også gøre at nu mere specifikt man skriver så kommer det til at være den regl der vinder.

Når man bruger id til css er det næsten umuligt at overskrive, så derfor skal man kun bruge klasser.

Css læser bagud så når den leder efter fx.
.body ul li{
    color: red;
}
Så vil den starter med at finde at li tags efterfølgende vil den finde alle li tags som er inde i ul tags og til sidst vil den finde alle li tags som er inde i ul tags som er inde i en body class.
Derfor er der også hurtigere at finde en klasse, selvom den måske har et navn der virker langt for os.

Jeg lærte at jeg aldrig skal bruge id når jeg laver css, da der er meget besværlig hvis man skal lave det om, så har jeg også lært at så længe jeg kan finde på et eller class navn selvom det måske virker lidt indviklet ved første kig er det meget bedre i længden og at jeg skal give alt jeg gerne vil style classes.
