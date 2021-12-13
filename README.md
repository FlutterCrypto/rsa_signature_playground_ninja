# rsa_signature_playground_ninja

For more information see here: http://fluttercrypto.bplaced.net/rsa-signature-playground-ninja/

https://pub.dev/packages/ninja

https://github.com/ninja-dart/ninja

ninja: ^3.0.7

https://pub.dev/packages/url_launcher

url_launcher: ^6.0.12

https://pub.dev/packages/path_provider

path_provider: ^2.0.5

in AndroidManifest.xml ergänzen:

    <queries>
        <!-- If your app opens https URLs -->
        <intent>
            <action android:name="android.intent.action.VIEW" />
            <data android:scheme="https" />
        </intent>
    </queries>

Sample data:

RSA Private key 2048:
```plaintext
-----BEGIN PRIVATE KEY-----
MIIEvAIBADANBgkqhkiG9w0BAQEFAASCBKYwggSiAgEAAoIBAQCLDyhmmZIjFWyF
lLV2gZ57BqQ1cZz496t1vDjwejMKbqry0Hb4gakf/JCSsM2x6SftRQ647pTnHMwf
BPqTF90ZTdA056Y4AgAKx+eIA3xTDFA/6OOFP1UW6zFG8tJva2QVdHAOJe+ysuU7
8V+e3c7tY7WBWyGaCH11pm2WWdnxqi15H/+ewzshjT3W3oZQiG85AugyHShlFruU
IYwo+83SsBKyr6JW5jnhB1G2laq4pw16wt0heokdhln3dR6h0oTsaK/ccT7VsdIo
MfbtLa+Aruam0jblY3N/qvfwiuX8nY/qrwJOK1pdDII3I0lKl/m+sb2xHe/xBLF1
k9Vfg++RAgIQAQKCAQBeFiC1ZBfkv/OyK8ESYhJfnETc3VWmIzqVxEVEamxkCSSe
iavo7zDB2Y8+UkIQhgHlNKjsGLS6HJtaSHoMax+vZPLYoDs5s79LVxP/jGMdAkUq
7a0fGyqjGHmRqro+Q4lC8N3HtrEMnse2VbSa+eyrXQTFfpSUNPuYJV9UCw4N6oxv
DQm83SrPPGyXaDzfIvijBqTdZDcKsmmsQWFe5IY90wII6cLN02ThG73qP7XVCiVU
JRIvffHZNhMRYcPd0laKrpjMsPCYDPmT2CRR7mo6qgFLyPWmsHQqXTsnroUwpZGi
K2KemJmszhM78a1nI+55+AIexKJx3//xeerY+QURAoGBAMw/yIAEf0K/RI/A0k9l
IQ3E1Z2hAbDPFChlkgmnZ51x96OTz2WgADrwUL11weOsmv9pG92ZXEjAb1/AUeNL
8dKzwoA4PhZFgYhihMiy9C0aUjhv8pZ9+LZtGZfSOeRwAI/DIss4vxh9sW/HFqAy
gboqGfSrHNbOiLD0tcUqX8F7AoGBAK5K9URrZCa7z7JYQRzb+cnjpB4xgtMeHoef
EVNJF2Uq1uosfAboZcyQy4uJbO7ZNdslQ4JMdBUv6JRWDyI//TYxIHBYHWNxZeKA
rnaDzxErLYMcGs++52sll9Wd8PWVhZD9Zz5aHkspvYTJOvL232MVtAkfRVqK/GIc
bb+5iUdjAoGAUptj1gxw9GE6GMXktfL5/4H4iwvBgv6VrjyzGNY7dun8HlqV7S23
PGQRaI5qWQTzJMCpS0CmWsisg2QG4BVnrVIDPsrT8KNz/3xjET/Q6nBO3gbpJG8O
/Fy83q0Qum3oW6KmmOyWBPgJly6HLruC4rF9CDn1O1I4CJV1cTvgnqsCgYAUVboD
u8yTO/cdfjS18syZpdZpn20tkErLZvm1/MfOcXi9CCB3RupymDw9JNdI6wp4S3SJ
jBNKxEr/n5ELDobERrc9qG3nHGn9LvFs/dHtAhnOEAaglF37wUcDnZSlXn0OeqrB
uqiee5dEarUVyTK+hEAejp1OHBZyi+iQNsN4/QKBgQC5bey866DVsii3FDqiULlc
IRlaB5ADzVhP75fCwtC3tmUfwgLLlXFJuLrmboQDoDLwEgEEU3LODkGd5wjQv0RN
HXF9lVZu5nQWWKCNmsJDenZ4QV4VJQfs7wLre+VvA5ey4+E5QCBT+ohExSh2bfQh
YcK0VNJWM2n8Fvq9rxuZ4g==
-----END PRIVATE KEY-----
```

RSA Public key 2048:
```plaintext
-----BEGIN PUBLIC KEY-----
MIIBITANBgkqhkiG9w0BAQEFAAOCAQ4AMIIBCQKCAQEAiw8oZpmSIxVshZS1doGe
ewakNXGc+Perdbw48HozCm6q8tB2+IGpH/yQkrDNsekn7UUOuO6U5xzMHwT6kxfd
GU3QNOemOAIACsfniAN8UwxQP+jjhT9VFusxRvLSb2tkFXRwDiXvsrLlO/Ffnt3O
7WO1gVshmgh9daZtllnZ8aoteR//nsM7IY091t6GUIhvOQLoMh0oZRa7lCGMKPvN
0rASsq+iVuY54QdRtpWquKcNesLdIXqJHYZZ93UeodKE7Giv3HE+1bHSKDH27S2v
gK7mptI25WNzf6r38Irl/J2P6q8CTitaXQyCNyNJSpf5vrG9sR3v8QSxdZPVX4Pv
kQICEAE=
-----END PUBLIC KEY-----
```

Klartext:
```plaintext
Mein wichtiges Geheimnis
```

PSS signature:
```plaintext
{
  "algorithm": "RSA-2048 PSS",
  "plaintext": "TWVpbiB3aWNodGlnZXMgR2VoZWltbmlz",
  "signature": "U7U57nZ5HtPQwdne4EFlKnlLTmxqyp9ye62XWij3B+4ATNSJee3nGyfHd27isIeJDR2so+NvNORUQBRdBI3X8yESg0kwWYuEx3Y9wpKzYbjuO4FHAmbCYoSWpkFpjlEK5sniGZWBdNIeVsBfTRwCu3GEx71Bx/wcpjjFzOztr0FerIdJHEH+p5nRw6nwH0cWAKlp0VsX5Otgs2YXL4UEpzkBUXdkjdhAvV8xfqmZu1xqrGj22ev8NhTQNLAVZ3w1nWZEJPvrE2cBJCKyzxBuGBvb3y7uD2c2fdkyiDoRDKRSyM6b+F1zueFLwBfqhrRLLdkcael2EWxXNMcwLB6bXQ=="
}
```
PKCS 1.5 signature:
```plaintext
{
  "algorithm": "RSA-2048 PKCS 1.5",
  "plaintext": "TWVpbiB3aWNodGlnZXMgR2VoZWltbmlz",
  "signature": "cWxasw8VTy0Tw7xpHgB9VypFaC8N+19KIRIFjro+/Y5GW/TIB1XU3TqZ4W39jbMx8MfOZ5LcYe2rogdus7yDTw9TZSALJul2PKBYgdygNmmNSS1MxiphOtcwlRP5/f/b4GJuUuOLuzMjFvfFTE1P5LaF+6AP6BHNlNWjZfuVohtnYu0dB3KRr03KBXA3WvqVNuqIvxLT+XNDyOHLg47DT5DO1IINtXORjH3RN8qsVnHN6Ve3Pvk3dD05EP7ZcPpiLBIAfR32dnlpWUBM/ZKXVqvVPVuLMrpKP/SjfV0MlpoYJ5zEUtUHQyTpCC43dFCnlMtneDKg9+yzUU52ughm1A=="
}
```

development environment:
```plaintext
Android Studio Arctic Fox Version 2020.3.1 Patch 3
Build #AI-203.7717.56.2031.7784292
Runtime version: 11.0.10+0-b96-7249189 aarch64
VM: OpenJDK 64-Bit Server VM
Flutter 2.5.3 channel stable Framework Revision 18116933e7
Dart 2.14.4
```

tested on:
```plaintext
Android Simulator: 
  Android 11 (SDK 30) Emulator,
  Android 12 SV2 (SDK 31) Emulator, 
  Android 6 (SDK 23) Emulator,
  Android 5 (SDK 21) Emulator.
iOS Simulator:  
  iOS 15 Emulator
  iOS 11.4 Emulator 
```



RSA signature with Ninja

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
