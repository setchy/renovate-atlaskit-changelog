# Atlaskit Design Tokens - Renovate

ideally there would be a shared rule that uses templatized sourceDirectory

```
    {
      "extends": ["packages:atlaskit"],
      "sourceUrl": "https://bitbucket.org/atlassian/atlassian-frontend-mirror",
      "sourceDirectory": "design-system/{{ lookup (split packageName '/') 1 }}"
    }
```

or

```
    {
      "matchPackageNames": ["@atlaskit/heading", "@atlaskit/logo", ...],
      "sourceUrl": "https://bitbucket.org/atlassian/atlassian-frontend-mirror",
      "sourceDirectory": "design-system/{{ lookup (split packageName '/') 1 }}"
    }
```