# Molecule Testing

This directory contains Molecule configuration for testing the ansible-acct role.

## Test Platforms

This role is designed for Ubuntu/Debian-based systems using the apt package manager. The testing focuses on Ubuntu LTS versions to ensure compatibility and reliability.

- Ubuntu 20.04 (Focal Fossa) LTS
- Ubuntu 22.04 (Jammy Jellyfish) LTS
- Ubuntu 24.04 (Noble Numbat) LTS

## Running Tests

### Prerequisites

```bash
pip install molecule[docker] docker ansible
```

### Run Tests

```bash
# Run full test suite
molecule test

# Test individual steps
molecule create
molecule converge
molecule verify
molecule destroy
```

## Test Structure

- `molecule.yml`: Main configuration
- `converge.yml`: Playbook that applies the role
- `verify.yml`: Verification tests that ensure acct is properly installed and configured