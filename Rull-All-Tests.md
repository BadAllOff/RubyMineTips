**Rationale**

Usually I want to run the spec where my cursor is located. Sometimes I want to run all the specs in a file. I do not want to have to first navigate to the outermost describe block to do this.

**Mechanism**

Save a macro that navigates to the top of the file, invokes all the tests, and then navigates back to the cursor.

Add the following macro to `~/Library/Preferences/RubyMineXX/options/macros.xml`:

````
<application>
  <component name="ActionMacroManager">
    <macro name="Run All Tests in File">
      <action id="EditorTextStart" />
      <action id="RunClass" />
      <action id="Back" />
    </macro>
  </component>
</application>
````

I bind this macro to `Control + Command + T`.