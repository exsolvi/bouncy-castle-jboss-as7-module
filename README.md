bouncy-castle-jboss-as7-module
==============================

JBoss AS7 module for Bouncy Castle

To use the Bouncy Castle module, perform the following steps.

1. Build the project with Maven 
   ( mvn clean install )
2. Copy the bouncycastle directory from target/modules to the JBoss modules dir.
   ( cp -a target/module/org/bouncycastle <jboss-as-basedir>/modules/org/ )
3. Add a jboss-deployment-structure.xml to your project containing:

<jboss-deployment-structure>
    <deployment>
        <dependencies>
            <module name="org.bouncycastle" slot="main" export="true" />
        </dependencies>
    </deployment>
</jboss-deployment-structure>


That's it. You should now be able to use Bouncy Castle functionality in your projects.


Last updated: 2012-07-17 (David Boman)

