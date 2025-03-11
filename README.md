# Smali SSL Patterns

A collection of Smali patterns to detect SSL pinning implementations in Android applications. This repository helps security analysts and reverse engineers identify various SSL pinning techniques used in Android apps.

## Features
- Detect SSL pinning patterns across multiple frameworks.
- Covers common SSL pinning libraries and techniques such as OkHttp, TrustManager, Conscrypt, Trustkit, and more.
- Useful for bypassing SSL pinning during security testing.

## Pattern Structure
The patterns are organized in a JSON format, with each key representing a framework or method and the corresponding value listing the Smali patterns.

### Example
```json
{
    "OkHttp Certificate Pinning": [
        "com/squareup/okhttp/CertificatePinner;",
        "okhttp3/CertificatePinner;",
        "->setCertificatePinner$okhttp",
        "okhttp/CertificatePinner;->check",
        "okhttp3/CertificatePinner;->check",
        "okhttp3/OkHttpClient$Builder;->certificatePinner"
    ]
}
```

## Usage
1. Use these patterns to scan Smali code for SSL pinning implementations.
2. Integrate them into static analysis tools or custom scripts.
3. Modify or extend the patterns based on specific requirements.

## Contribution
Contributions are welcome! Feel free to open issues or submit pull requests to enhance the pattern database.

## License
This project is licensed under the MIT License.
