# [लिनक्स] Bash lsusb उपयोग: USB डिवाइसों की जानकारी प्राप्त करें

## Overview
`lsusb` एक कमांड है जो आपके सिस्टम में जुड़े USB डिवाइसों की जानकारी प्रदर्शित करता है। यह डिवाइसों के बारे में विवरण जैसे कि निर्माता, उत्पाद आईडी, और अन्य तकनीकी जानकारी प्रदान करता है।

## Usage
`lsusb` कमांड का मूल सिंटैक्स इस प्रकार है:

```bash
lsusb [options] [arguments]
```

## Common Options
- `-v`: विस्तृत जानकारी प्रदर्शित करता है।
- `-t`: USB ट्री संरचना दिखाता है।
- `-s [bus]:[device]`: विशेष USB डिवाइस की जानकारी दिखाने के लिए।
- `-d [vendor]:[product]`: विशेष विक्रेता और उत्पाद आईडी के साथ डिवाइस की जानकारी दिखाता है।

## Common Examples
यहाँ कुछ सामान्य उदाहरण दिए गए हैं:

1. सभी जुड़े USB डिवाइसों की सूची प्राप्त करने के लिए:
   ```bash
   lsusb
   ```

2. विस्तृत जानकारी के साथ USB डिवाइसों की सूची प्राप्त करने के लिए:
   ```bash
   lsusb -v
   ```

3. विशेष USB डिवाइस की जानकारी प्राप्त करने के लिए (उदाहरण: बस 001, डिवाइस 002):
   ```bash
   lsusb -s 001:002
   ```

4. विशेष विक्रेता और उत्पाद आईडी के साथ डिवाइस की जानकारी प्राप्त करने के लिए (उदाहरण: विक्रेता 1234, उत्पाद 5678):
   ```bash
   lsusb -d 1234:5678
   ```

## Tips
- `lsusb` का उपयोग करते समय, यदि आप विस्तृत जानकारी चाहते हैं, तो `-v` विकल्प का उपयोग करें, लेकिन ध्यान रखें कि यह बहुत सारी जानकारी प्रदर्शित कर सकता है।
- USB डिवाइसों की पहचान करने में मदद के लिए, डिवाइस के नाम और आईडी को नोट करें।
- यदि आप USB डिवाइसों की संरचना को समझना चाहते हैं, तो `-t` विकल्प का उपयोग करें।