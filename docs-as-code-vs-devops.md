# Docs-as-Code vs DevOps for Documentation

Docs-as-Code and DevOps for documentation are closely related concepts, but they are not the same.

## Docs-as-Code

**Docs-as-Code** is an approach where documentation is created and maintained using the same tools and workflows commonly used for software development.

Typical practices include:

- Writing documentation in Markdown, AsciiDoc, or reStructuredText
- Storing documentation in Git repositories
- Using branches for documentation changes
- Creating pull requests or merge requests
- Reviewing documentation through Git-based workflows
- Tracking documentation changes through version control
- Building and publishing documentation using documentation tools

### Example workflow

```text
Writer creates or updates documentation
        ↓
Writes content in Markdown
        ↓
Commits changes to Git
        ↓
Creates a Pull Request
        ↓
Developer / SME reviews the changes
        ↓
Changes are merged
        ↓
Documentation is built and published
```

### Definition

> Docs-as-Code is an approach where documentation is created, version-controlled, reviewed, and maintained using the same tools and workflows used for software development, such as Markdown, Git, branches, and pull requests.

---

## DevOps for Documentation

**DevOps for documentation** applies DevOps principles such as automation, continuous integration, and continuous delivery to the documentation lifecycle.

Documentation can become part of the same CI/CD processes used for software.

For example, when documentation changes are committed, a pipeline can automatically:

1. Validate the documentation
2. Check links and formatting
3. Build the documentation site
4. Generate API documentation
5. Run quality checks
6. Publish or deploy the documentation

### Example workflow

```text
Documentation or product change
        ↓
Commit to Git
        ↓
CI/CD pipeline starts
        ↓
Documentation validation
        ↓
Build documentation
        ↓
Run automated checks
        ↓
Deploy / publish documentation
```

---

## Key Differences

| Docs-as-Code | DevOps for Documentation |
|---|---|
| Focuses on how documentation is authored and maintained | Focuses on automating and integrating documentation delivery |
| Treats documentation like source code | Applies DevOps practices to documentation |
| Uses Git, Markdown, branches, and pull requests | Uses CI/CD pipelines, automated builds, tests, and deployments |
| Encourages collaboration between writers, developers, and SMEs | Integrates documentation into the software delivery lifecycle |
| Can be used without a complete CI/CD pipeline | Commonly relies on CI/CD and automation |

---

## Simple Example

Suppose you are documenting an API.

You write the documentation in Markdown:

```markdown
## GET /v1/servers

Returns information about available servers.
```

You commit the Markdown file to Git and create a pull request for review.

**This is Docs-as-Code.**

After the pull request is merged, suppose a CI/CD pipeline automatically:

- Validates the Markdown
- Checks links
- Generates the documentation website
- Builds API reference documentation
- Deploys the updated documentation

**This is DevOps applied to documentation.**

---

## Relationship Between the Two

A simple way to remember the relationship is:

```text
Docs-as-Code
    ↓
Git + Markdown + Branches + Pull Requests + Reviews

DevOps for Documentation
    ↓
CI/CD + Automated Validation + Builds + Testing + Deployment
```

Docs-as-Code provides a code-like documentation workflow, while DevOps practices can automate and operationalize that workflow.

## Interview Summary

> **Docs-as-Code** is an approach where documentation is treated like source code. Writers use tools such as Markdown, Git, branches, and pull requests to create, version, review, and maintain documentation.
>
> **DevOps for documentation** extends this workflow by integrating documentation into CI/CD pipelines, allowing validation, building, testing, and publishing activities to be automated.
>
> In simple terms, **Docs-as-Code focuses on how documentation is managed, while DevOps focuses on automating and integrating its delivery into the development lifecycle.**
