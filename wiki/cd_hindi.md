# [Linux] Bash cd उपयोग: फ़ोल्डर बदलने का कमांड

## Overview
`cd` कमांड का उपयोग वर्तमान कार्यशील निर्देशिका (current working directory) को बदलने के लिए किया जाता है। यह आपको फ़ाइल सिस्टम में विभिन्न फ़ोल्डरों के बीच नेविगेट करने की अनुमति देता है।

## Usage
`cd` कमांड की मूल संरचना निम्नलिखित है:

```bash
cd [options] [arguments]
```

## Common Options
- `-`: पिछले निर्देशिका में वापस जाने के लिए।
- `..`: एक स्तर ऊपर जाने के लिए।
- `~`: उपयोगकर्ता के होम निर्देशिका में जाने के लिए।

## Common Examples
- अपने होम निर्देशिका में जाने के लिए:
  ```bash
  cd ~
  ```

- एक स्तर ऊपर जाने के लिए:
  ```bash
  cd ..
  ```

- किसी विशेष फ़ोल्डर में जाने के लिए (उदाहरण: Documents):
  ```bash
  cd Documents
  ```

- पिछले फ़ोल्डर में वापस जाने के लिए:
  ```bash
  cd -
  ```

## Tips
- हमेशा सुनिश्चित करें कि आप सही फ़ोल्डर में जा रहे हैं। `pwd` कमांड का उपयोग करके वर्तमान कार्यशील निर्देशिका की जांच करें।
- फ़ोल्डर नामों में स्पेस होने पर उन्हें उद्धरण में डालें, जैसे:
  ```bash
  cd "My Folder"
  ```
- `cd` कमांड का उपयोग करते समय टाइपिंग में सावधानी बरतें, क्योंकि गलत फ़ोल्डर नाम आपको त्रुटि दे सकता है।