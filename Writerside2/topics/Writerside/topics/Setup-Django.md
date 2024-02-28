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
                <deflist>
                    <def>Env: Virtualenv Environmnet</def>
                </deflist>
            </step>
        </procedure>
    </li>
</list>