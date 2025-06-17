Test Case: File Upload Validation

Scenario: User uploads a file to the system, which must meet format and size rules.

Steps (Same for all test cases)
1. Access the file upload page.
2. Click "Choose File".
3. Select the specified file.
4. Click "Upload".

## Test Variations

| File Type | File Size | Expected Result                                      |
|-----------|-----------|------------------------------------------------------|
| `.pdf`    | 9MB       | Upload successful                                    |
| `.jpg`    | 12MB      | Error: File size exceeds limit (10MB)               |
| `.zip`    | 3MB       | Error: Invalid file type                             |
| `.exe`    | 11MB      | Error: Invalid file type and size exceeds limit      |
| `.png`    | 10MB      | Upload successful                                    |

## Acceptance Criteria
- Accepts only `.pdf`, `.jpg`, `.png`
- Maximum size: 10MB
- Returns clear error messages for size/type violations
