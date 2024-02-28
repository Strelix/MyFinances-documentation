# Setup Django

<warning>Make sure you have followed the previous steps for setting up our project.</warning>
<p>
To setup Django, which is our backend library, the main thing you need to do is install dependencies.
After that you can configure the project variables, and run the app!
</p>
<list type="decimal">
    <li>
        <procedure title="Setup a virtual environment">
            <code-block lang="shell">
                python3 -m venv venv
            </code-block>
        </procedure>
    </li>
    <li>
        <procedure title="Install poetry and run poetry install">
            <step>
                <procedure type="choices">
                    <step>
                    <code-block lang="shell" prompt="$">
                        pip install -U pip setuptools poetry
                    </code-block>
                    </step>
                    <step>
                        Or you can use their <a href="https://python-poetry.org/docs/#installing-manually">official guide</a>
                    </step>
                </procedure>
            </step>
            <step>
                <code-block>
                    poetry install
                </code-block>
                <note>
                    If you would like to run a database other than Sqlite3, run the appropriate command found below:
                    <code-block lang="shell">
                        poetry install --only postgres
                        poetry install --only mysql
                    </code-block>
                </note>
            </step>
            <step>
                Setup an administrator account. This can be done with the <path>createsuperuser</path> command:
                <code-block lang="shell" prompt="$">
                    python manage.py createsuperuser
                </code-block>
            </step>
            <step>
                Run the server
                <code-block lang="shell" prompt="$">
                    python manage.py runserver
                </code-block>
            </step>
        </procedure>
    </li>
</list>