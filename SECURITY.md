# LOVE PDF — Security & Retention Policy

1. **Encryption**: All connections enforced over TLS 1.3 / SSL.
2. **File Processing**: PDF files are processed in isolated worker streams.
3. **Data Retention**: Temporary files removed automatically after 24 hours.
4. **Secret Management**: API keys and merchant secrets read exclusively from process environment.
