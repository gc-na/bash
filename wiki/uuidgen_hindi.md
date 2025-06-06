# [Linux] Bash uuidgen का उपयोग: यूनिक आईडी जनरेट करना

## Overview
`uuidgen` एक Bash कमांड है जिसका उपयोग यूनिक यूनिवर्सली यूनिक आइडेंटिफायर (UUID) बनाने के लिए किया जाता है। UUID एक 128-बिट का संख्या है जो किसी भी वस्तु को अद्वितीय पहचान देने के लिए उपयोग की जाती है।

## Usage
`uuidgen` कमांड का मूल सिंटैक्स इस प्रकार है:

```bash
uuidgen [options] [arguments]
```

## Common Options
- `-r`, `--random`: यादृच्छिक UUID उत्पन्न करता है।
- `-v`, `--version`: UUID के संस्करण को निर्दिष्ट करता है।
- `-h`, `--help`: कमांड के उपयोग के बारे में सहायता प्रदर्शित करता है।

## Common Examples
यहाँ कुछ सामान्य उदाहरण दिए गए हैं:

### उदाहरण 1: साधारण UUID जनरेट करना
```bash
uuidgen
```

### उदाहरण 2: यादृच्छिक UUID जनरेट करना
```bash
uuidgen -r
```

### उदाहरण 3: UUID को फ़ाइल में सहेजना
```bash
uuidgen > my-uuid.txt
```

### उदाहरण 4: कई UUID जनरेट करना
```bash
for i in {1..5}; do uuidgen; done
```

## Tips
- UUID का उपयोग तब करें जब आपको किसी वस्तु की अद्वितीय पहचान की आवश्यकता हो, जैसे कि डेटाबेस रिकॉर्ड या फाइलें।
- UUID को फ़ाइलों के नाम में शामिल करने से फ़ाइलों के बीच टकराव से बचा जा सकता है।
- यदि आप एक ही UUID को बार-बार जनरेट करना चाहते हैं, तो `-r` विकल्प का उपयोग करें।