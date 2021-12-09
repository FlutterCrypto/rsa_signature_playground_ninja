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

```plaintext
-----BEGIN PRIVATE KEY-----
MIIEvAIBADANBgkqhkiG9w0BAQEFAASCBKYwggSiAgEAAoIBAQCQ/UGcr4P3Z/5s
mH60TDNLwc1oKVWKmG4ceEHoh8Tub95HOyPboNi2QsNaqdL+kFiiOE4HH+5YM+my
cYFuQNOCmOCdhq7d+CM8fg4ayH3utKH4BGw6tWME/R3pGBAtpZ23GVCfDkcwFRZw
d3aYrpcpB1omCd0y8+gPsVxIO5/Qo7IJsBDgEKh7Y3GLfG0ReHln5xMRwN3zCRoq
AIrLbk3tf2BgVC4bw47Hjw0ow/23r4ONPNgi3TSNcaJMHus1kFv5pLDHziCKXtBU
zmQXD0r78V1SXh3xst/4YQyL4rqdmmacCIgKWLZ9pvpcALShELz9Bc1DMNigPc33
Dz7YCZrJAgIQAQKCAQAnxwLREhjVFvghyrwZOFWOMQuNHIXw6UWi9dC5A7GPVT1r
NUdCkLpsXQxK3GxflSMAU+4qkdoKE52nXS/xgjHnd/wjd/38iY8SaHDXzAfORC0v
fD7vLVOW5QckxI4npDhD+nK4eiNmu12ygaAxYtLN1Wcmfc0WagfN0Y556r3vIY9K
rsN6rqPutRc5D3wu4sL76/KrC+6fTBbaOZT6JvcICmHblmuaxpum6esjwCNzq2uk
Acv39M328V6JfPn5DFQ7in0Ktg8Em/Z287v4WRpSkQfuVlW4XI7hQPoiLguAfEPy
R0RFHY+k4TPlKij/Q7bl2Vgw5/RlIDE84H+NLfnRAoGBANPsH/+/6FplkZio/q+n
IITGPvS66BUgx45hNvwGF9djte60JHaqEXa2nZOePFBB2pU3aGJOhrxv4Zl8/Tj0
ceghfELSmF1ciexj/k78qmnrWBwc/28M/eV6gSM2Jfhhus/oH0PlSxzFGuRlRpss
w4O9mg/Ld8/+YcZvrhN8ZaZXAoGBAK8lQff5WUoV/Ypi5zt/q/tZSn1ljotaJDpP
D9AWjaxpEANp2Y2D6Y1aOCsoVR97tztkdnO2cLNHOx1Q39lOKNuwyAG8oVgNxWZb
BE6q5cqvQgJdJy4Dy3XKpH4I+vWwpvAeaSRaUly2VWVU5eQiB18Jj2p47r5SDS3K
9mKhPNPfAoGBAIHvsKTOZJkmt98hshaYFXAWkzLjch3TPS5+ts0i6nBxH4FsY5aM
4+ePhastWCe1568ICoOh7oKoctP0aAVtkwIsZm6UPi1e6qdO3giQa3w9kTAqxfq7
TAD8EXGBHTeAd4oIuqD5j3etZqenodMNQxOaDdrSG1jZdF9shvmDshvhAoGARWzu
2OPOqfUYtNLpf38mvbwLSAND0AM9KUvECMBlJYlPRGYxXoXkuz+RTAe9RCdKsWE+
4vKmhKxzKO0B8Il0m9DaPwxZMtZIX48dQ1yMUxdLNzx7QQpwhCuVfqCldhIpDaM0
fKIFh2nUPmlCkcphRhnovisP93YQ2JpvCSpa+FECgYAOiMLpvb3Esb8BAW2Jy7lY
hk727Q2lRc9O8yILkp8Yty5/or5jGa6tmYHorvOk9D+xpFlt9Tr84jXSR98SCE+p
ls/XFEdn9U1pFK9DWVjCs7M+4srxt+o6HyV49r/sMh24gZRdo+v2ScIVuporIMhL
eijiCrQrsX0R15TtAK2p0g==
-----END PRIVATE KEY-----
```

```plaintext
-----BEGIN PUBLIC KEY-----
MIIBITANBgkqhkiG9w0BAQEFAAOCAQ4AMIIBCQKCAQEAkP1BnK+D92f+bJh+tEwz
S8HNaClViphuHHhB6IfE7m/eRzsj26DYtkLDWqnS/pBYojhOBx/uWDPpsnGBbkDT
gpjgnYau3fgjPH4OGsh97rSh+ARsOrVjBP0d6RgQLaWdtxlQnw5HMBUWcHd2mK6X
KQdaJgndMvPoD7FcSDuf0KOyCbAQ4BCoe2Nxi3xtEXh5Z+cTEcDd8wkaKgCKy25N
7X9gYFQuG8OOx48NKMP9t6+DjTzYIt00jXGiTB7rNZBb+aSwx84gil7QVM5kFw9K
+/FdUl4d8bLf+GEMi+K6nZpmnAiICli2fab6XAC0oRC8/QXNQzDYoD3N9w8+2Ama
yQICEAE=
-----END PUBLIC KEY-----
```

Klartext:
```plaintext
The quick brown fox jumps over the lazy dog
```

PSS signature:
```plaintext
{
  "algorithm": "RSA-2048 PSS",
  "plaintext": "VGhlIHF1aWNrIGJyb3duIGZveCBqdW1wcyBvdmVyIHRoZSBsYXp5IGRvZw==",
  "signature": "QhsEb1tgmHqQ0ayvZOX7f+WlJ1dvt1H89LA69epf83J6MHAYcKq0af1xAf+BBUtLe5a9iPSERotD1+7os4ByZpJAHFcXoJAcHucUIkN9MKaxh4vF9K2hBXR0isLPosE2EjtsjXwBVvBWw6TFmIpD8aa4Nj+RryFNLbf2IMxIBCyzFXgBCZKSA123jeP9Ffu3Ua2a2BsvCM0bQFLz/bEJmoszg+9ptAhN+lWyJpzNtgXXYMg9OMyuJbUy4sNJUtpfhLLAnf8wuLWYDoqjlDfCuZvelb0cKiZcHU1YafRF1JD089Y/rbk8/3aS7DQYANxI6E9auDO9KnIIhQQsm9Bs8g=="
}
```
PKCS 1.5 signature:
```plaintext
{
  "algorithm": "RSA-2048 PKCS 1.5",
  "plaintext": "VGhlIHF1aWNrIGJyb3duIGZveCBqdW1wcyBvdmVyIHRoZSBsYXp5IGRvZw==",
  "signature": "Ms4XUiyrX5sxByDJaelqAiQPTGSlJweXJHeKRdf9lPPNF6D1jHBFP6rPbfkqHEc7lYrcivnPZv+p7CVt/EWI32pA3dDzV3HNdCbGhzm75QQwg+jRNj1cSuNxJFVY9Qw5G1vvx27c5XPOkYe01IVMaD/UsvQpTljoWdEXRKd5RLEqHEsUJFg41xaey5A6uM9PzkY+iLmnNIc4MEfcgKfG/iCff4IM5oUJrwifLHTXW6+uzz9U7itGPAiqbtt/obwpgQOTwb0DaZycD3L+ThBxN+Xwg/zJP4PUJ3pRRK4PxfOrsRBssvjTRivgsGkCucGD4BMCzGBuvFNa3YyhfaSlcQ=="
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
