# [Linux] Bash caller उपयोग: फ़ंक्शन कॉल करना

## Overview
Bash में `caller` कमांड का उपयोग फ़ंक्शन कॉल की जानकारी प्राप्त करने के लिए किया जाता है। यह विशेष रूप से तब उपयोगी होता है जब आप यह जानना चाहते हैं कि किसी फ़ंक्शन को किस स्थान से कॉल किया गया है।

## Usage
`caller` कमांड का मूल सिंटैक्स इस प्रकार है:

```bash
caller [options]
```

## Common Options
- `-p`: यह विकल्प फ़ंक्शन के पैरामीटर को प्रदर्शित करता है।
- `-n`: यह विकल्प कॉलिंग फ़ंक्शन के नाम को प्रदर्शित करता है।

## Common Examples
1. **बिना किसी विकल्प के कॉलर का उपयोग करना:**

   ```bash
   function my_function {
       caller
   }
   my_function
   ```

   इस उदाहरण में, `caller` कमांड उस स्थान की जानकारी देगा जहाँ `my_function` को कॉल किया गया था।

2. **पैरामीटर के साथ कॉलर का उपयोग करना:**

   ```bash
   function my_function {
       echo "Caller info: $(caller -p)"
   }
   my_function
   ```

   यहाँ, `-p` विकल्प का उपयोग करते हुए, यह कॉलिंग फ़ंक्शन के पैरामीटर को प्रदर्शित करेगा।

3. **कॉलिंग फ़ंक्शन का नाम दिखाना:**

   ```bash
   function my_function {
       echo "Called from: $(caller -n)"
   }
   my_function
   ```

   इस उदाहरण में, `-n` विकल्प का उपयोग करके, यह कॉलिंग फ़ंक्शन का नाम दिखाएगा।

## Tips
- जब आप स्क्रिप्ट में डिबगिंग कर रहे हों, तो `caller` का उपयोग करके यह जानना आसान होता है कि फ़ंक्शन को कहाँ से कॉल किया गया है।
- `caller` का उपयोग करते समय, सुनिश्चित करें कि आप इसे फ़ंक्शन के भीतर ही उपयोग कर रहे हैं, क्योंकि यह केवल फ़ंक्शन कॉल के संदर्भ में जानकारी प्रदान करता है।