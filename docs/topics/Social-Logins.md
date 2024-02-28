# Social Logins

MyFinances supports two external login providers; Github and Google OAuth.
This allows a password-less yet still secure authentication.
<tabs>
    <tab title="Social Login with Github">
        <p>
            Github has an OAuth system which allows you to log into MyFinances with your Github Account.
        </p>
        <procedure title="Setup">
            <step>
                <a href="https://github.com/settings/applications/new">Click here</a> or go to github.com and go to:
                <ui-path>Settings | Developer Settings | OAuth Apps | Register a new application/New OAuth App</ui-path>
                <p>And fill in these fields:</p>
                <deflist>
                    <def title="Homepage URL">
                        If you are running MyFinances locally <control>ONLY</control> then you can set this to
                        http://127.0.0.1:8000. Otherwise, if you are running with a domain, set this to your domain/subdomain.
                    </def>
                    <def title="Authorization Callback URL">
                        The path should be <ui-path>/login/external/complete/github/</ui-path>. Examples below.
                        <list>
                            <li>http://127.0.0.1:8000/login/external/complete/github/</li>
                            <li>https://myfinances.domain.com/login/external/complete/github/</li>
                        </list>
                    </def>
                </deflist>
            </step>
            <step>
                You will be redirected to the new github application. Now click <path>Generate a new client secret</path>.
                Note down the <path>client ID</path> and <path>client secret</path> for in a minute.
            </step>
            <step>
                Add them values to your Environment Variables.
                <code-block>
                    GITHUB_KEY=[GitHub_client_ID]
                    GITHUB_SECRET=[GitHub_client_secret]
                </code-block>
                <tip>
                    More information can be found on environment variables
                    <a href="other-Setup-environment-variables.md">here</a>!
                </tip>
            </step>
            <step>
                Restart MyFinances to take effect.
            </step>
        </procedure>
    </tab>
    <tab title="Social Login with Google">
        <p>
            Google has an OAuth system which allows you to log into MyFinances with your Google Account.
        </p>
        <procedure title="Setup">
            <step>
                <a href="https://console.cloud.google.com/">Click here</a> to go to the Google Cloud Console.
                Here you will need to create a new project for MyFinances and note the details.
                <procedure title="Setup on Google Cloud" type="steps" collapsible="true">
                    <step>
                        Create a new project that will represent MyFinances.
                        Go to the <a href="https://console.cloud.google.com/projectcreate">GCC New Project page</a>
                        Refer to the GC Documentation for further individual fields 
                        (<a href="https://developers.google.com/workspace/guides/create-project">here</a>)
                    </step>
                    <step>
                        Configure the consent screen that will be shown to users when they try to log in to MyFinances.
                        Click <a href="https://console.cloud.google.com/apis/credentials/consent">here</a>
                        to go to the OAuth consent screen page.
                        For more information on how to fill in the individual fields, refer to the Google Cloud documentation.
                        (<a href="https://developers.google.com/workspace/guides/create-project">here</a>)
                    </step>
                    <step>
                        Go to the <a href="https://console.cloud.google.com/apis/credentials">Credentials Page</a>, and add these values. 
                        <p>And fill in these fields:</p>
                        <deflist>
                            <def title="Application Type">
                                This should be set to <control><emphasis>Web Application</emphasis></control>
                            </def>
                            <def title="Authorized Javascript Origins">
                                If you are running MyFinances locally <control>ONLY</control> then you can set this to
                                http://127.0.0.1:8000. Otherwise, if you are running with a domain, set this to your domain/subdomain.
                            </def>
                            <def title="Authorization redirect URL">
                                The path should be <ui-path>/login/external/complete/google-oauth2/</ui-path>. Examples below.
                                <list>
                                    <li>http://127.0.0.1:8000/login/external/complete/google-oauth2/</li>
                                    <li>https://myfinances.domain.com/login/external/complete/google-oauth2/</li>
                                </list>
                            </def>
                        </deflist>
                    </step>
                    <step>Note down the client ID and client secret</step>
                </procedure>
            </step>
            <step>
                Add the client ID and client secret values to your Environment Variables.
                <code-block>
                    GOOGLE_CLIENT_ID=[Google_client_ID]
                    GOOGLE_CLIENT_SECRET=[Google_client_secret]
                </code-block>
                <tip>
                    More information can be found on environment variables
                    <a href="other-Setup-environment-variables.md">here</a>!
                </tip>
            </step>
            <step>
                Restart MyFinances to take effect.
            </step>
        </procedure>
    </tab>
</tabs>