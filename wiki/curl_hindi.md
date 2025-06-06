# [लिनक्स] Bash curl का उपयोग: HTTP अनुरोध भेजने के लिए एक उपकरण

## Overview
`curl` एक कमांड-लाइन उपकरण है जिसका उपयोग URL के माध्यम से डेटा को भेजने और प्राप्त करने के लिए किया जाता है। यह HTTP, HTTPS, FTP और अन्य प्रोटोकॉल का समर्थन करता है, जिससे यह वेब से डेटा डाउनलोड करने और API के साथ बातचीत करने के लिए एक लोकप्रिय विकल्प बन जाता है।

## Usage
`curl` का मूल सिंटैक्स इस प्रकार है:

```bash
curl [options] [arguments]
```

## Common Options
- `-X`: HTTP विधि निर्दिष्ट करने के लिए (जैसे GET, POST)।
- `-d`: डेटा भेजने के लिए, आमतौर पर POST अनुरोधों में उपयोग होता है।
- `-H`: कस्टम हेडर जोड़ने के लिए।
- `-o`: आउटपुट फ़ाइल का नाम निर्दिष्ट करने के लिए।
- `-I`: केवल हेडर प्राप्त करने के लिए।

## Common Examples
1. **साधारण GET अनुरोध:**
   ```bash
   curl https://example.com
   ```

2. **POST अनुरोध के साथ डेटा भेजना:**
   ```bash
   curl -X POST -d "name=John&age=30" https://example.com/api
   ```

3. **कस्टम हेडर के साथ अनुरोध:**
   ```bash
   curl -H "Authorization: Bearer token" https://example.com/protected
   ```

4. **आउटपुट को फ़ाइल में सहेजना:**
   ```bash
   curl -o myfile.html https://example.com
   ```

5. **केवल हेडर प्राप्त करना:**
   ```bash
   curl -I https://example.com
   ```

## Tips
- हमेशा `-o` विकल्प का उपयोग करें यदि आप आउटपुट को फ़ाइल में सहेजना चाहते हैं, ताकि आप डेटा को बाद में देख सकें।
- API के साथ काम करते समय, `-H` विकल्प का उपयोग करके सही हेडर सेट करना न भूलें।
- यदि आप एक लंबा अनुरोध कर रहे हैं, तो `-v` विकल्प का उपयोग करें ताकि आप अनुरोध और प्रतिक्रिया के बारे में विस्तृत जानकारी प्राप्त कर सकें।