\# AI Workflow Comparison



\## Overview



For this exercise, I implemented the same settings form feature using two different AI prompting approaches. The goal was to compare the quality of the generated code and understand how prompt quality affects the development process.



\## Round One – Vague Prompt



In the first branch, I used a simple prompt asking the AI to create a settings form without providing detailed requirements. The AI generated a basic working form, but several important aspects were missing. Input validation was limited, accessibility features were incomplete, and the generated code did not explain how it should be tested. The form worked for basic input, but it required manual review to identify missing functionality and edge cases.



\## Round Two – Precise Prompt



In the second branch, I provided a detailed prompt with clear requirements. I specified the required fields, validation rules, accessibility requirements, expected behavior, and asked the AI to review its own implementation after generating the code. This version included required field validation, proper email validation, clearer error messages, semantic HTML, improved accessibility, and a cleaner overall structure. The AI also explained how the implementation was verified and suggested possible improvements.



\## Comparison



The difference between the two branches was significant. The vague prompt produced a functional starting point but required much more manual review and additional changes. The precise prompt resulted in code that was more complete, easier to understand, and closer to production quality. It handled validation more effectively, considered accessibility, and reduced the amount of manual debugging required.



\## AI Mistake I Caught



One issue I noticed in the first version was that the AI did not properly validate all email input and did not provide accessible feedback for validation errors. This required manual correction. The second version addressed these issues after the requirements were clearly specified.



\## Lessons Learned



This exercise demonstrated that detailed prompts produce much better results than vague prompts. Providing clear requirements, constraints, expected behavior, accessibility considerations, and verification instructions helped the AI generate higher-quality code and reduced the overall review effort. I learned that AI is most effective when guided with precise specifications rather than general requests.

