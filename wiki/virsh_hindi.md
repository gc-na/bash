# [Linux] Bash virsh उपयोग: वर्चुअल मशीन प्रबंधन के लिए कमांड

## Overview
`virsh` एक कमांड-लाइन टूल है जिसका उपयोग वर्चुअल मशीनों (VMs) और उनके संबंधित संसाधनों के प्रबंधन के लिए किया जाता है। यह KVM, Xen, और अन्य वर्चुअलाइजेशन तकनीकों के साथ काम करता है, जिससे उपयोगकर्ता वर्चुअल मशीनों को बनाने, शुरू करने, रोकने और प्रबंधित करने की अनुमति मिलती है।

## Usage
`virsh` कमांड का मूल सिंटैक्स इस प्रकार है:

```bash
virsh [options] [arguments]
```

## Common Options
- `list`: चल रही वर्चुअल मशीनों की सूची दिखाता है।
- `start <domain>`: निर्दिष्ट वर्चुअल मशीन को शुरू करता है।
- `shutdown <domain>`: निर्दिष्ट वर्चुअल मशीन को शटडाउन करता है।
- `destroy <domain>`: निर्दिष्ट वर्चुअल मशीन को समाप्त करता है।
- `create <xml-file>`: एक नई वर्चुअल मशीन को XML फ़ाइल से बनाता है।
- `define <xml-file>`: एक वर्चुअल मशीन को XML फ़ाइल से परिभाषित करता है।

## Common Examples
1. चल रही वर्चुअल मशीनों की सूची देखने के लिए:
   ```bash
   virsh list
   ```

2. एक वर्चुअल मशीन को शुरू करने के लिए:
   ```bash
   virsh start my-vm
   ```

3. एक वर्चुअल मशीन को शटडाउन करने के लिए:
   ```bash
   virsh shutdown my-vm
   ```

4. एक वर्चुअल मशीन को समाप्त करने के लिए:
   ```bash
   virsh destroy my-vm
   ```

5. एक नई वर्चुअल मशीन बनाने के लिए:
   ```bash
   virsh create /path/to/vm.xml
   ```

## Tips
- सुनिश्चित करें कि आप वर्चुअल मशीन के नाम को सही तरीके से टाइप कर रहे हैं, क्योंकि यह केस-सेंसिटिव होता है।
- `virsh` कमांड का उपयोग करते समय, आपको उचित अनुमतियों की आवश्यकता होती है, इसलिए सुनिश्चित करें कि आप सही उपयोगकर्ता के रूप में लॉग इन हैं।
- वर्चुअल मशीन के प्रदर्शन की निगरानी के लिए `virsh dominfo <domain>` का उपयोग करें, जो आपको वर्चुअल मशीन की स्थिति और संसाधनों की जानकारी देगा।