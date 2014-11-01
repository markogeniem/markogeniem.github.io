title: Automaatio ketterän kehityksen tukena
output: index.html
author:
	name: Marko Lenkkeri
	url: http://www.geniem.com/
	twitter: markogeniem

--

## QASW-Summit
## Automaatio ketterän kehityksen tukena

--

### Geniem

http://www.geniem.com/

* J2EE
* WP
* NodeJS
* Mobiili
* Appever

--

### Automaatio

Jokainen käsin tehty operaatio:
- Hidastaa kehityssykliä
- Luo virhemahdollisuuksia
- Aiheuttaa henkilöriippuvuuksia

--

### Automaatio

Perustyyppejä:
- On-demand
- Ajastettu
- Liipaistu

--

### Automaatio

On-demand
- Komentoriviltä tai työkalusta
- Vaatii käyttäjäaloitteen
- Kehitysvaiheeseen
- Toiminnallisuuden testaamiseen
- Testien ajo
- Lokaali deployment

--

### Automaatio

Ajastettu
- Tietyin aikavälein ajettava
- Ei käyttäjäinteraktiota
- Päivittäinen build
- Projektin tilan seuranta
- Ei varsinainen deployment

--

### Automaatio

Liipaistu
- Automaattisesti
- Ei käyttäjäinteraktiota
- Versionhallinnasta
- Tuotantodeployment

--

### Automaatio-recap

Enemmän logiikkaa, vähemmän käsitöitä


--

### Työkaluja
* [Ant](ant.apache.org)
* [Maven](maven.apache.org)
* [Gradle](www.gradle.org)
* [Chef](www.getchef.com)
* [Puppet](www.puppetlabs.com)
* [Grunt](gruntjs.com)

--

### Ant

* XML-pohjainen
	- Raskas syntaksi
	- Paljon tekstiä, vähän sisältöä
* Ei sisäänrakennettua riippuvuuksienhallintaa
* Rajoittunut ongelmanhallinta
* Ei tilanseurantaa
* Monialustainen
* Laaja IDE-tuki

--

### Ant
```
<?xml version="1.0"?> 
<project name="Summit" default="compile" xmlns:ivy="antlib:org.apache.ivy.ant">
   <target name="clean">
       <delete dir="classes"/>
       <delete dir="dist"/>
   </target>

   <target name="resolve">
       <ivy:resolve />
   </target>

   <target name="compile" depends="clean,resolve">
       <mkdir dir="classes"/>
       <javac srcdir="." destdir="classes"/>
   </target>

   <target name="jar" depends="compile">
       <mkdir dir="dist"/>
       <jar destfile="dist/summit.jar">
           <fileset dir="classes" includes="**/*.class"/>
           <manifest>
               <attribute name="Main-Class" value="AntExample"/>
           </manifest>
       </jar>
   </target>
</project>
```
--
### Ant/Ivy
```
<?xml version="1.0"?> 
<ivy-module version="2.0">
    <info organisation="com.geniem.summit" module="summit"/>
    <dependencies>
        <dependency org="commons-lang" name="commons-lang" rev="2.0"/>
        <dependency org="commons-cli" name="commons-cli" rev="1.0"/>
	<dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>3.8.1</version>
            <scope>test</scope>
        </dependency>
    </dependencies>
</ivy-module>
```
--

### Maven

* XML-pohjainen
	- Raskas syntaksi
	- Paljon tekstiä, vähän sisältöä
* Riippuvuuksienhallinta
* Projekteilla erityinen rakenne
	- Automatisoituja toimintoja rakenteen pohjalta
* Monialustainen
* Laaja IDE-tuki

--

### Maven
```
<project>
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.geniem.summit</groupId>
  <artifactId>summit</artifactId>
  <version>1.0</version>

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>3.8.1</version>
      <scope>test</scope>
    </dependency>
  </dependencies>
</project>
```
--

### Gradle

* Groovy-pohjainen
* Riippuvuuksienhallinta
* Laajennettavissa
* Taaksepäin yhteensopiva

--

### Gradle

```
apply plugin: 'java'
```

--

### Käyttäjät

* Hibernate
* Spring
* **Grails**
* Android

--

### Groovy?

Java-johdannainen
* Dynaaminen
* Modernien kielien ominaisuuksia
* Kevyempi syntaksi
* Nopeasti opittavissa
* Java-kirjastojen käyttö natiivisti

--

### Natiivirakenteet, closuret	

```
for (String it : new String[] {"Rod", "Carlos", "Chris"})
     if (it.length() <= 4)
         System.out.println(it);
```

```
["Rod", "Carlos", "Chris"].findAll{it.size() <= 4}.each{println it}
```
--

### Yksiselitteisen syntaksin edut

```
take(coffee).with(sugar, milk).and(liquor);
```

```
take coffee with sugar, milk and liquor
```
--

### Groovy.

Java-pohjainen dynaaminen kieli, jonka Java-kehittäjät oppivat nopeasti.

Groovy- ja Java-koodia voi sekoittaa.

Paljon muuta.

http://groovy.codehaus.org/

--

### Gradle Riippuvuuksienhallinta

```
repositories {
    mavenCentral()
}

dependencies {
    runtime(group: 'com.geniem.util', name:'monitoring-utils', version: '1.5.0');
    compile group: 'org.hibernate', name: 'hibernate-core', version: '3.6.7.Final'
    testCompile group: 'junit', name: 'junit', version: '4.+'
}
```

--

### Pluginit

http://plugins.gradle.org/

* Ohjelmointikielet
	* Java
	* Groovy
	* Scala
	* Assembler (Incubating)
	* C / C++ / Objective C / Objective C++ (Incubating)
--

### Pluginit

* Integraatio
	* J2EE WAR/EAR
	* Jetty
	* Maven
	* OSGi
	* ivy-publish (Incubating)
--

### Pluginit

* Kehitys
	* Eclipse
	* Checkstyle
	* CodeNarc
	* IntelliJ IDEA
	* Sonar
	* Visual Studio (Incubating)
--

### Pluginit

* Frontend
	* Grunt/Gulp/Node
	* lint/minify/gzip js
	* Docker
	* Vagrant
	* Markdown
--

### Yhteensopivuus

Ant ja Maven ovat monessa paikassa käytettyjä. Miksi siis haaskata tehtyä työtä?

--

### Yhteensopivuus

Ant-skriptat ovat käytettävissä Gradle-skriptasta

```
ant.importBuild 'build.xml'
```

Ant-toiminnot ovat käytettävissä Gradle-skriptasta
```
task hello << {
    ant.echo('hello from Ant')
}
```

Ant-muuttujat ovat käytettävissä Gradle-skriptasta
```
ant.buildDir = 'esimerkki'
println ant.buildDir
```
--

### Yhteensopivuus

Maven-skriptat voi konvertoida suoraan Gradle-skriptoiksi
* maven2gradle
* Build Init Plugin

--

### Gradle kokonaisuutena

--

### Gradle kokonaisuutena

--

### Gradle kokonaisuutena

--

### Gradle kokonaisuutena

--

### Automaatio muualla

--

### Grails

--

### Grails

--

### Grails

--

### Grails

--