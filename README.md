# AI-Assisted Git Workflow and Python Data Parsing

Student name: James Gabriel B. Boo
Section: TA31

## Project purpose

Briefly explain how this repository combines Git version control with XML, JSON, and YAML parsing.

## How to run

```bash
python3 parser_template.py
python3 -m unittest -v
```

## Git workflow summary

Development was managed through feature branches. The branch feature/data-parsers was used to implement XML, JSON, and YAML parsers with three separate commits. The branch docs/ai-note was created to document AI review status. The main branch integrated changes and triggered a controlled merge conflict. The conflict was created by editing the same line in AI_USAGE_LOG.md differently on main and docs/ai-note. Git reported a conflict, which was resolved by combining both changes into the final line:

Validation status: AI reviewed and tests passed

## Parser results

The XML parser returned default_operation as “merge” and test_option as “test-then-set”.
The JSON parser returned site as “FEU-Tech-Lab”, device_count as 3, enabled_devices as [“R1”, “SW1”], and roles as [“router”, “switch”, “wireless-ap”].

The YAML parser returned name as “Saturday-Lab”, approved as true, duration_minutes as 90, devices as [“R1”, “SW1”], and action as “validate-configuration”.

The combined summary integrated all three results into one dictionary.

## AI disclosure

The approved AI tool used was Gemini. Recommendations were validated against unit tests and lab instructions. Some suggestions were modified, such as the JSON parser which initially returned only a count of enabled devices but was adjusted to return hostnames instead. No recommendations were accepted without validation. Documentation of prompts, decisions, and evidence is included in AI_USAGE_LOG.md.

## Safety statement

Only the fictional classroom data provided (network_config.xml, devices.json, maintenance.yaml) was used. No credentials, tokens, private repository data, or personal information were submitted to AI. All outputs were validated locally with unit tests before committing.
