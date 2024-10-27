# AnonyMate

**AnonyMate** is a Python toolkit that provides a powerful suite of tools for data anonymization, masking, encryption, and fake data generation. Designed for developers working with sensitive information, AnonyMate helps ensure compliance with data privacy regulations (e.g., GDPR, HIPAA) while simplifying the anonymization process for testing, analysis, and data sharing.

## Key Features

- **Data Masking**: Mask sensitive data (e.g., names, emails, IDs) with custom characters, ensuring data cannot be directly identified.
- **Data Hashing**: One-way hashing for sensitive data, using SHA-256 to provide a non-reversible transformation for securely storing confidential data.
- **Encryption & Decryption**: Securely encrypt and decrypt sensitive data using symmetric encryption, allowing data to be accessed only by authorized parties.
- **Synthetic Data Generation**: Generate realistic fake data (e.g., names, emails, addresses) for testing and development without exposing actual sensitive data.
- **Partial Masking and Validation**: Support for partial masking (e.g., "123-***-789") for specific use cases and simple validation tools for email formats.
- **Compliance-Friendly**: Helps organizations meet data privacy and security requirements, making it suitable for various industries, including healthcare, finance, and e-commerce.

## Installation

Install AnonyMate using pip:

```bash
pip install AnonyMate



```bash
from anonymate.anonymizer import Anonymizer
from anonymate.faker_util import generate_fake_name, generate_fake_email, generate_fake_address

# Initialize Anonymizer
anonymizer = Anonymizer()

# Mask, hash, encrypt, and decrypt data
masked = anonymizer.mask_text("SensitiveData")
hashed = anonymizer.hash_text("SensitiveData")
encrypted = anonymizer.encrypt_text("SensitiveData")
decrypted = anonymizer.decrypt_text(encrypted)

# Generate fake data
fake_name = generate_fake_name()
fake_email = generate_fake_email()
fake_address = generate_fake_address()

# Display results
print("Masked:", masked)
print("Hashed:", hashed)
print("Encrypted:", encrypted)
print("Decrypted:", decrypted)
print("Fake Name:", fake_name)
print("Fake Email:", fake_email)
print("Fake Address:", fake_address)
