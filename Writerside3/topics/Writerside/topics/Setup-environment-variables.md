# Setup environment variables

<list type="decimal" id="list-of-steps">
    <li>
        Copy the `.env.sample` variables into `.env`
        You can do this with either of these methods:
        <list type="alpha-lower">
            <li>
                <procedure title="Using the terminal">
                    <code-block lang="shell">cp .env.sample .env</code-block>
                </procedure>
            </li>
            <li>
                <procedure title="Manually copy over the contents." collapsible="true" default-state="collapsed">
                    <step>
                        Go into <path>.env.sample</path>, press <shortcut>CTRL + A</shortcut>, then <shortcut>CTRL + C</shortcut>
                        <chapter title="View help image" collapsible="true">
                            <img src="copy-sample-env" border-effect="rounded">
                        </chapter>
                    </step>
                    <step>
                        Then create a file `.env`
                    </step>
                    <step>
                    Then go into the file and press `CTRL + V`
                    </step>
                </procedure>
            </li>
        </list>
    </li>
</list>