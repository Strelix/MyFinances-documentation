# Setup a database

<tabs id="setup-database">
    <tab title="Sqlite">
        <p>Sqlite is a popular option for local development as it has <control>no installation needed</control>,
        and is fast and compact for small data sources (like our project!).
        </p>
        <procedure title="Installation">
            <step>
                Add <code>DATABASE_TYPE=sqlite</code> to your environment variables.
                <tip>
                    More information can be found on environment variables
                    <a href="Setup-environment-variables.md">here</a>!
                </tip>
            </step>
            <step>
                Run django migrations
                <code-block lang="shell">
                    python manage.py migrate
                </code-block>
            </step>
        </procedure>
        And that's it! Now you'll have a database called db.sqlite3 in your root directory.
        You can connect to it with the required sqlite drivers manually - but django will do this for you!
    </tab>
    <tab title="Mysql">
        <p>
            MySQL is a popular option for local development and production deployments as it is <control>efficient</control>,
            and is a great fit for small data sources and also large sources! So you can easily run this app and scale to
            thousands of users.
        </p>
        <procedure title="Installation">
            <step>
                Add these to your environment variables:
                <code-block>
                    DATABASE_TYPE=mysql
                    DATABASE_HOST=
                    DATABASE_PORT=3306
                    DATABASE_NAME=myfinances # you can choose this, but must first create it (STEP 2)
                    DATABASE_USER=root
                    DATABASE_PASS=
                </code-block>
                <deflist collapsible="true" default-state="collapsed" type="wide">
                    <def title="DATABASE_HOST" id="db-host">
                        This is the location of your database. Some examples of a host:
                        <list>
                            <li>127.0.0.1 - this is if the database is on your local machine</li>
                            <li>mydb.123456789012.eu-west-2.rds.amazonaws.com - this is if you use AWS RDS</li>
                        </list>
                    </def>
                    <def title="DATABASE_PORT">
                        Each database will have a port. Typically, Mysql by default uses port <control>3306</control>.
                        If you have changed the port, put the number here. Examples are below:
                        <list>
                            <li>3306</li>
                            <li>1234</li>
                        </list>
                    </def>
                    <def title="DATABASE_NAME" id="db-name">
                        This is the name of your database that you created. You will have to do this manually.
                        <tip>We suggest using the DB name "MyFinances" to keep things simple!</tip>
                    </def>
                    <def title="DATABASE_USER" id="db-user">
                        This is the name of your database user. Generally this is called "root" or "admin" but you'll have to check!
                        <tip>
                            When you are in production, please make sure to use a seperate user which only has access
                            to the MyFinances database and no other.
                        </tip>
                    </def>
                </deflist>
                <tip>
                    More information can be found on environment variables
                    <a href="Setup-environment-variables.md">here</a>!
                </tip>
            </step>
            <step>
                Now lets connect to our database.
                <code-block lang="shell" prompt=">>>">
                    mysql -h {DATABASE_HOST} -u {DATABSE_USER} -p {DATABASE_PASS} # manually fill out the values in brackets {}
                </code-block>
            </step>
            <step>
                While <control>inside of the mysql terminal</control> run the SQL Query:
                <code-block lang="SQL">
                    CREATE DATABASE [NAME]
                </code-block>
                <tip>
                    This will be the NAME that you put inside <path>DATABASE_NAME</path>
                    E.g.
                    <code-block lang="sql">
                        CREATE DATABASE myfinances
                    </code-block>
                </tip>
            </step>
            <step>
                Exit the mysql terminal
                <code-block lang="sql">
                    EXIT;
                </code-block>
            </step>
            <step>
                Run django migrations
                <code-block lang="shell">
                    python manage.py migrate
                </code-block>
            </step>
        </procedure>
        And that's it!
    </tab>
    <tab title="Postgresql">
        <p>
            Postgres is a popular option for local development and production deployments as it is <control>efficient</control>,
            and is a great fit for small data sources and also large sources! So you can easily run this app and scale to
            thousands of users.
        </p>
        <procedure title="Installation">
            <step>
                Add these to your environment variables:
                <code-block>
                    DATABASE_TYPE=postgres
                    DATABASE_HOST=
                    DATABASE_PORT=5432
                    DATABASE_NAME=myfinances # you can choose this, but must first create it (STEP 2)
                    DATABASE_USER=root
                    DATABASE_PASS=
                </code-block>
                <deflist collapsible="true" default-state="collapsed" type="wide">
                    <include from="pycharm-Setup-a-database.md" element-id="db-host"></include>
                    <def title="DATABASE_PORT">
                        Each database will have a port. Typically, Postgres by default uses port <control>5432</control>
                        If you have changed the port, put the number here. <emphasis>Examples</emphasis> are below:
                        <list>
                            <li>5432</li>
                            <li>1234</li>
                        </list>
                    </def>
                    <include from="pycharm-Setup-a-database.md" element-id="db-name"></include>
                    <include from="pycharm-Setup-a-database.md" element-id="db-user"></include>
                </deflist>
                <tip>
                    More information can be found on environment variables
                    <a href="Setup-environment-variables.md">here</a>!
                </tip>
            </step>
            <step>
                Now lets connect to our database.
                <code-block lang="shell" prompt=">>>">
                    mysql -h {DATABASE_HOST} -u {DATABSE_USER} -p {DATABASE_PASS} # manually fill out the values in brackets {}
                </code-block>
            </step>
            <step>
                While <control>inside of the mysql terminal</control> run the SQL Query:
                <code-block lang="SQL">
                    CREATE DATABASE [NAME]
                </code-block>
                <tip>
                    This will be the NAME that you put inside <path>DATABASE_NAME</path>
                    E.g.
                    <code-block lang="sql">
                        CREATE DATABASE myfinances
                    </code-block>
                </tip>
            </step>
            <step>
                Exit the mysql terminal
                <code-block lang="sql">
                    EXIT;
                </code-block>
            </step>
            <step>
                Run django migrations
                <code-block lang="shell">
                    python manage.py migrate
                </code-block>
            </step>
        </procedure>
        And that's it!
    </tab>
</tabs>