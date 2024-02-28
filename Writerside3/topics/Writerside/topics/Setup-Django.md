# Setup Django

To setup Django, which is our backend library, the main thing you need to do is install dependencies.
After that you can configure the project variables, and run the app!

<list type="decimal">
    <li>
        <procedure title="Create a python interpreter">
            <step>
                Go into `Settings`
                 <procedure title="View help image" collapsible="true">
                    <img src="dropdown-choose-settings"  border-effect="rounded">
                </procedure>
            </step>
        </procedure>
    </li>
    <li>
        <procedure>
            <step>
                Go into <path>Project: MyFinances</path>
            </step>
            <step>
                Go into <path>Python Interpreter</path>
                <procedure title="View help image" collapsible="true">
                    <img src="python-interpreter-dropdown"  border-effect="rounded">
                </procedure>
            </step>
            <step>
                Now press 
                <ui-path>
                    Add Interpreter | Add Local Interpreter
                </ui-path>
                <procedure title="View help image" collapsible="true">
                    <img src="add-local-interpreter"  border-effect="rounded">
                </procedure>
            </step>
            <step>
                Choose these settings:
                <deflist type="medium">
                    <def title="Env">Virtualenv Environment</def>
                    <def title="Environment">New</def>
                    <def title="Location"><path>YourPath/venv</path></def>
                    <def title="Base Interpreter">Python 3.9 or above. <tip>We suggest using the latest python version.</tip></def>
                </deflist>
            </step>
            <step>
                Now install our dependencies with python poetry
                <code-block lang="shell" prompt="$">
                    pip install poetry
                    poetry install
                </code-block>
            </step>
            <step>
                Make sure the PyCharm Djnago settings are up to date. You can do this in
                <ui-path>Languages and Frameworks | Django</ui-path> and enable <path>Enable Django Support</path>.
                After this you can now fill out the rest of the fields to match your project. Some example settings are below.
                <deflist>
                    <def title="Django Project Root">
                        Where you cloned our project, e.g. <path>E:\projects\MyFinances\</path>
                    </def>
                </deflist>
            </step>
        </procedure>
    </li>
</list>