# [लिनक्स] Bash docker उपयोग: कंटेनर प्रबंधन के लिए एक उपकरण

## Overview
Docker एक ओपन-सोर्स प्लेटफार्म है जो डेवलपर्स को एप्लिकेशन को कंटेनर में पैकेज करने, वितरित करने और चलाने की अनुमति देता है। यह विभिन्न वातावरणों में एप्लिकेशन की स्थिरता और पोर्टेबिलिटी सुनिश्चित करता है।

## Usage
Docker कमांड का मूल सिंटैक्स इस प्रकार है:

```bash
docker [options] [arguments]
```

## Common Options
- `run`: एक नया कंटेनर बनाता और उसे चलाता है।
- `ps`: चल रहे कंटेनरों की सूची दिखाता है।
- `images`: उपलब्ध इमेजेस की सूची दिखाता है।
- `pull`: एक इमेज को रिमोट रेपोजिटरी से डाउनलोड करता है।
- `build`: एक Dockerfile से इमेज बनाता है।

## Common Examples
यहाँ कुछ सामान्य उदाहरण दिए गए हैं:

1. **नया कंटेनर चलाना:**
   ```bash
   docker run hello-world
   ```

2. **चल रहे कंटेनरों की सूची देखना:**
   ```bash
   docker ps
   ```

3. **इमेजेस की सूची देखना:**
   ```bash
   docker images
   ```

4. **इमेज को डाउनलोड करना:**
   ```bash
   docker pull ubuntu
   ```

5. **Dockerfile से इमेज बनाना:**
   ```bash
   docker build -t my-image .
   ```

## Tips
- हमेशा अपने कंटेनरों को नियमित रूप से अपडेट करें ताकि सुरक्षा और प्रदर्शन में सुधार हो सके।
- Dockerfile में कैशिंग का उपयोग करें ताकि इमेज निर्माण की गति बढ़ सके।
- कंटेनरों के लिए उचित नामकरण प्रथाओं का पालन करें ताकि प्रबंधन सरल हो सके।