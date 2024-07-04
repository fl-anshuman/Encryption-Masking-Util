# Encryption-Masking Custom Jar

## Introduction

The Encryption-Masking custom jar provides functionality for encrypting and decrypting fields using a custom annotation named `@EncryptedField`. Additionally, it offers the ability to mask fields using `@MaskedField`. This jar can be seamlessly integrated into your project as a dependency.

## Usage

### Step 1: Add Dependency

Add the following dependency to your project's `pom.xml` file:

```xml
<dependency>
    <groupId>com.EncryptionMasking</groupId>
    <artifactId>Encryption-Masking</artifactId>
    <version>1.0.0</version>
</dependency>
```

### Step 2: Application Configuration
In your application's main class annotated with @SpringBootApplication, ensure that you include the com.EncryptionMasking.Encryption_Masking package in the scanBasePackages attribute:

```xml
@SpringBootApplication(scanBasePackages = {"Base Package", "com.EncryptionMasking.Encryption_Masking"})
public class YourApplication {
    // Your application code
}
```
### Step 3: Using Custom Annotations
Once the dependency is added and the application is configured, you can utilize the @EncryptedField and @MaskedField annotations in your project. Simply annotate the fields you want to encrypt or mask with the appropriate annotation and the Encryption-Masking custom jar will handle the rest.


```xml
import com.EncryptionMasking.Encryption_Masking.EncryptedField;
import com.EncryptionMasking.Encryption_Masking.MaskedField;

public class User {
    @EncryptedField
    private String creditCardNumber;
    
    @MaskedField
    private String email;
    
    // Other fields and methods
}
```
In this example, the User class contains fields annotated with @EncryptedField and @MaskedField. The Encryption-Masking custom jar will take care of encrypting and masking these fields according to the defined behavior.

Conclusion
By following the above steps, you can easily incorporate the Encryption-Masking custom jar into your project, allowing you to encrypt and decrypt fields using the @EncryptedField annotation and mask fields using the @MaskedField annotation.
