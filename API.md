# LOVE PDF — API Documentation

## Authentication
API requests require a Bearer token in the `Authorization` header:
`Authorization: Bearer lp_live_YOUR_KEY`

## Endpoints

### 1. Merge PDFs
`POST /api/v1/pdf/merge`
Form-Data parameters:
- `files`: PDF files

### 2. Compress PDF
`POST /api/v1/pdf/compress`
Form-Data parameters:
- `file`: PDF file
- `level`: `maximum` | `recommended` | `high`

### 3. Watermark PDF
`POST /api/v1/pdf/watermark`
Form-Data parameters:
- `file`: PDF file
- `text`: Watermark text string
