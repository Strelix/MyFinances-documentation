# Setup Tailwind

To setup Tailwind, which is our frontend CSS library and DaisyUI which is our tailwind component library.

<procedure title="Install NPM">
    <step>
        Install NodeJS + NPM. You can follow a guide such as
        <a href="https://docs.npmjs.com/downloading-and-installing-node-js-and-npm">this</a>.
    </step>
    <step>
        Run this command
        <code-block lang="shell">
            npm install
        </code-block>
    </step>
</procedure>

<procedure title="Build tailwind">
    <warning>
        Please <control>never</control> edit the <path>output.css</path> file,
        always edit the <path>input.css</path> file if you need to make manual CSS changes.
    </warning>
    <step>
        <code-block lang="shell">
            npm run tailwind-build
        </code-block>
    </step>
</procedure>
<note>
    You must run tailwind build every time you want to work on the frontend, otherwise some
    some tailwind classes won't be included.
</note>