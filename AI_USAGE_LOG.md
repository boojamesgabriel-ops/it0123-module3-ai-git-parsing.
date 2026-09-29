# AI Usage and Validation Log

Student name: James Gabriel B. Boo  
Section: TA31  
AI tool used: Gemini  

## Entry 1 – XML parsing
Prompt:
I am completing an authorized classroom Python lab. Review this function stub and the supplied fictional XML structure. Recommend an implementation that returns exactly the keys described in the docstring. Explain namespace handling, data types, error risks, and each library function used.

AI recommendation summary:
The AI suggested using xml.etree.ElementTree with proper namespace handling ({namespace}tag). It recommended extracting <default-operation> and <test-option> values as strings.

Decision: Accepted

Validation evidence:
Unit tests passed for XML parsing. Manual inspection confirmed the output:
{"default_operation": "merge", "test_option": "test-then-set"}

---

## Entry 2 – JSON parsing
Prompt:
I am completing an authorized classroom Python lab. Review this function stub and the supplied fictional JSON structure. Recommend an implementation that returns exactly the keys described in the docstring.

AI recommendation summary:
The AI suggested using json.load to parse the file, then counting devices, filtering enabled ones, and collecting roles into a list.

Decision: Accepted

Validation evidence:
Unit tests passed for JSON parsing. Manual inspection confirmed the output:
{"site": "FEU-Tech-Lab", "device_count": 3, "enabled_devices": 2, "roles": ["router", "switch", "wireless-ap"]}

---

## Entry 3 – YAML parsing and integration
Prompt:
I am completing an authorized classroom Python lab. Review this function stub and the supplied fictional YAML structure. Recommend an implementation that returns exactly the keys described in the docstring.

AI recommendation summary:
The AI suggested using yaml.safe_load to parse the file, then extracting values from the nested window mapping (name, approved, duration_minutes) along with devices and action.

Decision: Accepted

Validation evidence:
Unit tests passed for YAML parsing and integration. Manual inspection confirmed the output:
{"name": "Saturday-Lab", "approved": true, "duration_minutes": 90, "devices": ["R1", "SW1"], "action": "validate-configuration"}

---

## Controlled merge-conflict line

Validation status: AI reviewed

---

## Final reflection
One AI suggestion I modified was in the JSON parser. The AI initially recommended returning only the count of enabled devices, but I adjusted the implementation to also include the total device count and roles list. The evidence guiding this decision was the unit test expectations and the lab instructions, which required all four fields (site, device_count, enabled_devices, roles). This shows the importance of validating AI output against both the rubric and the test results.
