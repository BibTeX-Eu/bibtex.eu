---
slug: email
title: "BibTeX field type: email"
sidebar_label: email
---

# BibTeX field type: email

Email includes the email address of the stated authors if you want to indicate them. It's not a common field and might not be supported.

To specify email addresses, the following variants are recommended:

**As a note to display at the end of the reference:**


```tex
@book{ ... ,
 author = {Muller, John},

 ...

 note = "{\tt john.muller@example.com}"
}
```

**To display behind the family name:**

```tex

@book{ ... ,
 author = {Muller {\tt john.muller@example.com}, John },

 ...

}
```
