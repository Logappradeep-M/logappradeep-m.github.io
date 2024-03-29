---
title: "Debit Card Exp Date Format"
date: 2024-01-25 12:30:00 +/-0800   
categories: [Pega,Edit validate rule]
math: true
mermaid: true
tags: [Pega,Credit / Debit Card Exp Date Format,Edit validate rule,Pattern Validation]
# image: "/assets/img/post/LV.png"
# image:
#   path:  /assets/img/post/LV.png
#   width: 1000   # in pixels
#   height: 400   # in pixels
#   alt: Login Validation
---
## Edit Validate rules
## Format
* Ex: `05 24`

```bash
//In format (MM YY)
// Regex to check valid Exp Date
String regex= ("^(0[1-9]|1[0-2])\\s([0-9]{2})$");
// Compile the ReGex
  java.util.regex.Pattern p=java.util.regex.Pattern.compile(regex);

// If the string is empty, return false
if (theValue == null || theValue.trim().equals("")) return false;
theProperty.addMessage("Please Enter Valid Expiry date");

// Pattern class contains matches() method to match the given string and regular expression
java.util.regex.Matcher m = p.matcher(theValue);
return m.matches();
```

## Reference 
[Click Here](https://docs-previous.pega.com/reference/87/about-edit-validate-rules?){:target="_blank"} - **More details from pega academy for Edit Validate rules** 