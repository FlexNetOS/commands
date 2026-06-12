<command>
<name>meta-analyze</name>
<description>Invokes the meta-repo-analyzer deep research skill to evaluate a target repository and align it with the Meta framework.</description>
<prompt>
I need you to perform a deep research analysis on the target repository using the `meta-repo-analyzer` skill.

Please activate the `meta-repo-analyzer` skill and apply it to the target specified by the user arguments.
Follow the methodology outlined in the skill to analyze the architecture, determine the L1/L2/L3 abstraction fit, and provide organization recommendations for the `.meta.yaml` file.

Target: {{args}}
</prompt>
</command>