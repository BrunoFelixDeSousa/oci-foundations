[⬅️ Voltar para o README](../README.md)

# Tagging in OCI

Tags are key-value pairs used to better organize and manage your resources in Oracle Cloud Infrastructure (OCI). They offer several benefits, such as:

- Customizing the organization of resources
- Enhancing cost management
- Enabling tag-based access control (policies can be written based on tags)

In OCI, there are two types of tags:

1. **Free-Form Tags**
2. **Defined Tags** (recommended)

![Tagging](../images/tagging.png)

## Free-Form Tags

### Characteristics:
- Basic implementation
- Comprises only a key and a value
- No defined schema or access restrictions

**Example:**
```plaintext
Environment = "Production"
```

## Defined Tags (Recommended)

### Characteristics:
- More features and control
- Contained within namespaces
- Defined schema
- Secured with policies

**Example:**
```plaintext
Operations.Environment = "Production"
```

You can also define the type of values allowed for defined tags, such as:

- Allowing any string value
- Restricting to specific values (users can only select from predefined options)

![Tag Namespace](../images/tag_namespace.png)