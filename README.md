# CI/CD Pipeline Implementation Demo 🚀

A sample Python project demonstrating the implementation of Continuous Integration (CI) using GitHub Actions.

## Project Overview 📋

This project showcases:
- Basic Python application using Streamlit
- Unit testing implementation with pytest
- GitHub Actions workflow for CI
- Automated testing on push/PR

## Repository Structure 📁

```
CI-Pipeline/
│
├── app.py                    # Main Streamlit application
├── _test.py                 # Unit tests
├── .github/
│   └── workflows/
│       └── ci.yaml          # CI pipeline configuration
├── LICENSE                  # MIT license
└── README.md               # Project documentation
```

## CI Pipeline Features ⚡

Our GitHub Actions workflow includes:

```yaml
name: CI Pipeline
on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Set up Python
      uses: actions/setup-python@v2
      with:
        python-version: '3.9'
    - name: Install dependencies
      run: pip install pytest streamlit
    - name: Run tests
      run: pytest _test.py
```

## Local Development 💻

```bash
# Clone repository
git clone <repository-url>
cd CI-Pipeline

# Install dependencies
pip install pytest streamlit

# Run tests
pytest _test.py

# Start application
streamlit run app.py
```

## Test Coverage 🧪

Tests verify:
- Power calculation functions
- Error handling
- Basic functionality requirements

## Contributing 🤝

1. Fork the repository
2. Create a feature branch
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Make changes and add tests
4. Ensure CI pipeline passes
5. Submit a pull request

## License 📄

MIT License - see [LICENSE](LICENSE) file for details.

---
*Note: This project serves as an educational example for implementing CI pipelines with GitHub Actions.*
