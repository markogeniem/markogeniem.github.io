title: Automaatio ketterän kehityksen tukena

author:
	name: Marko Lenkkeri
	url: http://www.geniem.com/
	twitter: markogeniem
	email: marko@geniem.com
output: index.html
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

Jokainen käsin tehty operaatio
- hidastaa kehityssykliä
- luo virhemahdollisuuksia
- aiheuttaa henkilöriippuvuuksia

--

### Automaatio

Perustyyppejä
- on-demand
- ajastettu
- liipaistu

--

### Automaatio

On-demand
- komentoriviltä tai työkalusta
- vaatii käyttäjäaloitteen
- kehitysvaiheeseen
- toiminnallisuuden testaamiseen
- testien ajo
- lokaali deployment

--

### Automaatio

Ajastettu
- tietyin aikavälein ajettava
- ei käyttäjäinteraktiota
- päivittäinen build
- projektin tilan seuranta
- ei varsinainen deployment

--

### Automaatio

Liipaistu
- automaattisesti
- ei käyttäjäinteraktiota
- versionhallinnasta
- tuotantodeployment

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
	- raskas syntaksi
	- paljon tekstiä, vähän sisältöä
* ei sisäänrakennettua riippuvuuksienhallintaa
* rajoittunut ongelmanhallinta
* ei tilanseurantaa
* monialustainen
* Llaaja IDE-tuki

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
	- raskas syntaksi
	- paljon tekstiä, vähän sisältöä
* riippuvuuksienhallinta
* projekteilla erityinen rakenne
	- automatisoituja toimintoja rakenteen pohjalta
* monialustainen
* laaja IDE-tuki

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
* riippuvuuksienhallinta
* laajennettavissa
* taaksepäin yhteensopiva

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
* dynaaminen
* modernien kielien ominaisuuksia
* kevyempi syntaksi
* nopeasti opittavissa
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

Paljon muuta : http://groovy.codehaus.org/

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
	* Ivy-publish (Incubating)
--

### Pluginit

* Kehitys
	* Eclipse
	* Checkstyle
	* CodeNarc
	* IntelliJ IDEA
	* Sonar
	* Sublime
	* Visual Studio (Incubating)
--

### Pluginit

* Frontend
	* Grunt/Gulp/Node
	* Lint/Minify/Gzip JS
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

Maven-tyyliset hakemistorakenteet automaattisesti tuettuina.

Migraation jälkeen build comparison varmistaa, että uusi ja vanha järjestelmä luovat yhtenevät lopputulokset.

--


### Gradle kokonaisuutena 1/3

Gradlen hyötykäyttö ohjelmistokehitysprosessissa
* kehitysympäristön pohjatyöt
* projektin aloittaminen
* riippuvuuksien hallinta

--

### Gradle kokonaisuutena 2/3

Gradlen hyötykäyttö ohjelmistokehitysprosessissa
* kehitysympäristön ajaminen
* testien ajaminen
* uusien kehitysympäristöjen luonti

--

### Gradle kokonaisuutena 3/3

Gradlen hyötykäyttö ohjelmistokehitysprosessissa
* deploy/publish
* ohjelmiston tason seuranta
* raportointi

--

### Automaatio muualla

Jos kehitysympäristön ja sen ympärillä tapahtuvat asiat voi automatisoida, niin miksi ei sovelluksen sisälläkin tapahtuvat asiat?

--

### Grails

Mikä on Grails ?
* J2EE Web development framework
* Hibernate ja Spring frameworkkien tiukka integraatio
* Java/Groovy/Scala
* DSL, CoC, DRY, MVC

--

### Grails

Hyötyjä
* Riippuvuuksien injektointi
* Domain-luokkien ja tietokannan tiukka sidonta
* Plugin-järjestelmä
* Scaffolding
* Templatet
* Riippuvuuksien hallinta

--

### Grails esimerkkejä 1/2

```
class EntryPointAccess {
	Date created
	boolean passwordSet
	EntryPoint entryPoint

	static belongsTo = [user:User]

	static constraints = {
		created nullable:true
		passwordSet nullable:false
		entryPoint nullable:false
    	}
	
	static mapping = {
		user index:'user_and_passwordSet_idx'
		passwordSet index:'user_and_passwordSet_idx'
		created index:'created_idx'
	}
	
	def beforeInsert()
	{
		created = new Date()
	}
}
```

--

### Grails esimerkkejä 2/2

```
class EntryPointAccessController
{
	def show(EntryPointAccess entryPointAccessInstance) {
		respond entryPointAccessInstance
	}

	def create() {
		respond new EntryPointAccess(params)
	}

	@Transactional
	def update(EntryPointAccess entryPointAccessInstance) {
		if (entryPointAccessInstance == null) {
			notFound()
			return
		}

		if (entryPointAccessInstance.hasErrors()) {
			respond entryPointAccessInstance.errors, view:'edit'
			return
		}

		entryPointAccessInstance.save flush:true
		respond entryPointAccessInstance, [status: OK]
	}
}
```

--

### Kysymyksiä?

http://www.gradle.org

http://www.grails.org

marko@geniem.com

@markogeniem

