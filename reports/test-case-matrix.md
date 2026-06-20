# Test Case Matrix

| ID | Endpoint | Scenario | Expected |
|----|-----------|-----------|----------|
| TC01 | GET /health | Service healthy | 200 |
| TC02 | POST /vision/detect | Valid request | 202 |
| TC03 | POST /vision/detect | Missing correlationId | 400 |
| TC04 | POST /vision/detect | Invalid cameraId | 400 |
| TC05 | POST /vision/detect | Invalid imageUrl | 400 |
| TC06 | GET /vision/detections/{id} | Existing detection | 200 |
| TC07 | GET /vision/detections/{id} | Unknown detection | 404 |
| TC08 | GET /vision/models/info | Success | 200 |
| TC09 | No token | Unauthorized | 401 |
| TC10 | Long cameraId | Validation error | 400 |
| TC11 | Old timestamp | Validation error | 400 |
| TC12 | Smoke workflow | End-to-end | Pass |