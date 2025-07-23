---
title: FPD Toolkit
description: This rule provides comprehensive documentation for the FPD Toolkit, a professional CLI tool designed to generate high-quality Flutter and Dart packages that adhere to industry best practices. It covers a wide range of topics including installation, usage commands (create, validate, guide), advanced validation for pub.dev, standardized project structure, interactive guides, CI/CD integration, and a development roadmap. Consult this rule when you need to: Generate a new Flutter application, plugin, or Dart package. Validate an existing project against pub.dev standards. Understand the recommended architecture and best practices for Flutter/Dart development. Find examples for common patterns (e.g., state management, testing). Automate package validation in your CI/CD pipeline.
alwaysApply: false
globs:
  - '**/pubspec.yaml'
  - '**/analysis_options.yaml'
  - '**/README.md'
  - '**/lib/**'
  - '**/tool/**'
  - '**/test/**'
---
# FPD Toolkit

# **Professional CLI Toolkit for High-Quality Flutter/Dart Packages**

**FPD Toolkit** is a comprehensive tool that enables you to create Flutter/Dart packages following all `pub.dev` standards and industry best practices. It includes automatic generation, validation, interactive documentation, and practical examples.

## Quick Start

```bash
# Install
dart pub global activate fpd_toolkit

# Create your first package
fpd-toolkit create package my_package --description "My first package"

# Validate
fpd-toolkit validate my_package

# Ready to publish!
cd my_package
dart pub publish --dry-run
```

## Key Features

### Automatic Generation

* **Flutter Applications** – Full apps with Material Design structure
* **Flutter Plugins** – Cross-platform plugins with native interface
* **Dart Packages** – Pure Dart libraries optimized for pub.dev

### Advanced Validation

* **pub.dev Scoring** – Automatic scoring reaching 125+ points
* **Code Analysis** – Detects issues and suggestions
* **Structure Verification** – Ensures required files are in place

### Interactive Documentation

* **Step-by-Step Guides** – Interactive development tutorials
* **Practical Examples** – Example code using best practices
* **Architecture Patterns** – Clean Architecture, MVVM, BLoC

### Template Management

* **Custom Templates** – Create and reuse templates
* **Flexible Configuration** – Adapt generation to your needs
* **Multiple Platforms** – Supports Android, iOS, Web, Desktop

## Installation

### Global Activation

```bash
dart pub global activate fpd_toolkit
```

### Direct Usage

```bash
dart pub global run fpd_toolkit
```

## **Usage Guide**

### Create a New Package

```bash
# Create Dart package
fpd-toolkit create package my_package --description "My awesome package"

# Create Flutter app
fpd-toolkit create app my_app --description "My Flutter application"

# Create Flutter plugin
fpd-toolkit create plugin my_plugin --platforms android,ios --description "My native plugin"
```

### Validate a Package

```bash
fpd-toolkit validate my_package
# Output: 125/130 pub.dev points
```

### Access Interactive Guides

```bash
fpd-toolkit guide architecture    # Architecture guide
fpd-toolkit guide testing         # Testing guide
fpd-toolkit guide state-mgmt      # State management
fpd-toolkit guide performance     # Optimization
```

### View Code Examples

```bash
fpd-toolkit example widget        # Widget examples
fpd-toolkit example state         # State management
fpd-toolkit example animation     # Animations
fpd-toolkit example testing       # Advanced testing
```

## **Available Commands**

| Command    | Description                       | Example                             |
| ---------- | --------------------------------- | ----------------------------------- |
| `create`   | Generate new package/app/plugin   | `fpd-toolkit create package my_lib` |
| `validate` | Validate package for pub.dev      | `fpd-toolkit validate my_lib`       |
| `guide`    | Interactive development guides    | `fpd-toolkit guide architecture`    |
| `example`  | Code examples and design patterns | `fpd-toolkit example widget`        |
| `template` | Manage custom templates           | `fpd-toolkit template list`         |
| `init`     | Initialize existing project       | `fpd-toolkit init`                  |


## **Generated Project Structure**

```
my_package/
├── lib/
│   ├── my_package.dart          # Entry point
│   └── src/
│       └── my_package_base.dart # Core logic
├── test/
│   └── my_package_test.dart     # Unit tests
├── example/                     # Usage examples
├── pubspec.yaml                 # Optimized configuration
├── README.md                    # Full documentation
├── CHANGELOG.md                 # Change history
├── LICENSE                      # MIT License
└── analysis_options.yaml        # Code analysis settings
```

## **pub.dev Scoring**

Generated packages reach **125+ points** on pub.dev:

* **Conventions** (30/30) – Naming and structure
* **Documentation** (30/30) – README, API docs, examples
* **Platforms** (20/20) – Multi-platform support
* **Analysis** (30/30) – Clean code analysis
* **Dependencies** (15/20) – Up-to-date dependencies

## **Complete Documentation**

### Included Guides

* **[Development Guide](docs/GUIA_DESARROLLO_FLUTTER_DART.md)** – Full Flutter/Dart development walkthrough
* **[Best Practices](docs/MEJORES_PRACTICAS_FLUTTER.md)** – Patterns and conventions
* **[Original Script](scripts/flutter_package_generator.dart)** – Reference generator script

### Covered Topics

* **Architecture** – Clean Architecture, MVVM, BLoC
* **UI/UX** – Material Design, Cupertino, Responsive design
* **State Management** – Provider, Riverpod, BLoC, GetX
* **Testing** – Unit, Widget, Integration, Golden tests
* **Performance** – Optimization, profiling, memory usage
* **Security** – Encryption, authentication, permissions
* **Internationalization** – i18n, l10n, localization
* **Platforms** – Android, iOS, Web, Desktop

## **Advanced Configuration**

### Environment Variables

```bash
export FLUTTER_DEV_AUTHOR="Your Name"
export FLUTTER_DEV_ORG="com.yourorg"
export FLUTTER_DEV_TEMPLATE_DIR="$HOME/flutter_templates"
```

### Configuration File

```yaml
# ~/.flutter_dev_config.yaml
default_author: "Your Name"
default_organization: "com.yourorg"
default_license: "MIT"
templates_dir: "~/flutter_templates"
```

## **Usage Examples**

### Case 1: Fast Startup

```bash
# Create full MVP
fpd-toolkit create app startup_mvp --description "Startup MVP"
cd startup_mvp
fpd-toolkit guide architecture
flutter run
```

### Case 2: Enterprise Library

```bash
# Create corporate package
fpd-toolkit create package company_utils --description "Corporate utilities"
fpd-toolkit validate company_utils
dart pub publish --dry-run
```

### Case 3: Cross-Platform Plugin

```bash
# Plugin for all platforms
fpd-toolkit create plugin super_plugin \
  --platforms android,ios,web,windows,macos,linux \
  --description "Incredible universal plugin"
```

## **Use Cases**

### Developers

* Generate packages with professional structure
* Validate before publishing to pub.dev
* Learn best practices interactively

### Companies

* Standardize project structure
* Accelerate MVP development
* Maintain consistent code quality

### Education

* Teach Flutter/Dart best practices
* Ready-to-use practical examples
* Step-by-step interactive guides

## **Recommended Workflow**

1. **Planning**

   ```bash
   fpd-toolkit guide architecture
   ```

2. **Generation**

   ```bash
   fpd-toolkit create package my_lib --description "My library"
   ```

3. **Validation**

   ```bash
   fpd-toolkit validate my_lib
   ```

4. **Development**

   ```bash
   cd my_lib
   fpd-toolkit guide testing
   fpd-toolkit example widget
   ```

5. **Publishing**

   ```bash
   dart pub publish --dry-run
   dart pub publish
   ```

## **Local Development**

### Clone and Run

```bash
git clone https://github.com/flutterpilot/fpd_toolkit.git
cd fpd_toolkit
dart pub get
dart run bin/fpd_toolkit.dart --help
```

### Run Commands

```bash
dart run bin/fpd_toolkit.dart create package test_pkg --description "Test package"
dart run bin/fpd_toolkit.dart validate test_pkg
dart run bin/fpd_toolkit.dart guide --help
```

### Verbose Mode

```bash
dart run bin/fpd_toolkit.dart --verbose create package debug_pkg
```

## **Testing**

### Run Tests

```bash
dart test
```

### Testing with Coverage

```bash
dart test --coverage=coverage
genhtml coverage/lcov.info -o coverage/html
```

### Command Testing

```bash
dart run bin/fpd_toolkit.dart --verbose [command]
```

## **Metrics and Performance**

### Benchmarks

```bash
# Measure generation time
time dart run bin/fpd_toolkit.dart create package perf_test
```

### Memory Profiling

```bash
dart run --observe bin/fpd_toolkit.dart create package perf_test
```

### Validation Scoring

```bash
dart run bin/fpd_toolkit.dart validate generated_package
```

## **CI/CD Integration**

### GitHub Actions

```yaml
name: Validate Package
on: [push, pull_request]
jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: dart-lang/setup-dart@v1
      - run: dart pub global activate fpd_toolkit
      - run: fpd-toolkit validate .
```

### Cross-Platform Testing

```bash
dart run bin/fpd_toolkit.dart create package cross_platform_test
cd cross_platform_test
flutter test
dart test
```

## **Contributing**

### Development Setup

```bash
git clone https://github.com/flutterpilot/fpd_toolkit.git
cd fpd_toolkit
dart pub get
```

### Run Integration Tests

```bash
dart run "$OLDPWD/bin/fpd_toolkit.dart" create package integration_package
dart run "$OLDPWD/bin/fpd_toolkit.dart" create app integration_app
dart run "$OLDPWD/bin/fpd_toolkit.dart" create plugin integration_plugin --platforms android,ios
dart run "$OLDPWD/bin/fpd_toolkit.dart" validate integration_package
```

### Verify Generation

```bash
# Create test package
dart run bin/fpd_toolkit.dart create package test_package --description "Test package"

# Validate structure
dart run bin/fpd_toolkit.dart validate test_package

# Inspect generated files
ls -la test_package/
cat test_package/pubspec.yaml
cat test_package/README.md
```

### Template Testing

```bash
# Test different types
dart run bin/fpd_toolkit.dart create app test_app --description "Test app"
dart run bin/fpd_toolkit.dart create plugin test_plugin --platforms android,ios --description "Test plugin"
dart run bin/fpd_toolkit.dart create package test_package --description "Test package"

# Validate all
dart run bin/fpd_toolkit.dart validate test_app
dart run bin/fpd_toolkit.dart validate test_plugin
dart run bin/fpd_toolkit.dart validate test_package
```

### Performance Testing

```bash
# Measure generation time
time dart run bin/fpd_toolkit.dart create package perf_test
time dart run bin/fpd_toolkit.dart create app perf_app
time dart run bin/fpd_toolkit.dart create plugin perf_plugin --platforms android,ios

# Memory profiling
dart run --observe bin/fpd_toolkit.dart create package memory_test
```

### Cross-Platform Validation

```bash
# Create cross-platform plugin
dart run bin/fpd_toolkit.dart create plugin cross_platform_plugin \
  --platforms android,ios,web,windows,linux,macos \
  --description "Cross-platform plugin"

# Validate structure
dart run bin/fpd_toolkit.dart validate cross_platform_plugin

# Inspect platform-specific folders
ls -la cross_platform_plugin/android/
ls -la cross_platform_plugin/ios/
ls -la cross_platform_plugin/lib/src/
```

### Documentation Testing

```bash
# Verify README generation
dart run bin/fpd_toolkit.dart create package doc_test --description "Documentation test"
cat doc_test/README.md

# Verify CHANGELOG generation
cat doc_test/CHANGELOG.md

# Verify LICENSE generation
cat doc_test/LICENSE
```

### Error Handling Testing

```bash
# Test invalid names
dart run bin/fpd_toolkit.dart create package invalid-name
dart run bin/fpd_toolkit.dart create package 123package
dart run bin/fpd_toolkit.dart create package package@test

# Test existing directories
mkdir existing_dir
dart run bin/fpd_toolkit.dart create package existing_dir
dart run bin/fpd_toolkit.dart create package existing_dir --force
```

### Template Customization Testing

```bash
# Create a custom template
mkdir -p ~/custom_templates/package_template
cp -r test_package/* ~/custom_templates/package_template/

# Use the custom template
dart run bin/fpd_toolkit.dart create package custom_test --template ~/custom_templates/package_template
```

## **Troubleshooting**

### Common Issues

#### Error: "Command not found"

```bash
# Check installation
dart pub global list | grep fpd_toolkit

# Reinstall
dart pub global deactivate fpd_toolkit
dart pub global activate fpd_toolkit
```

#### Error: "Permission denied"

```bash
# Check permissions
ls -la ~/.pub-cache/bin/

# Fix permissions
chmod +x ~/.pub-cache/bin/fpd-toolkit
```

#### Error: "Template not found"

```bash
# Check available templates
fpd-toolkit template list

# Use default template
fpd-toolkit create package my_package --template default
```

#### Error: "Invalid package name"

```bash
# Use snake_case
fpd-toolkit create package my_valid_package

# Avoid special characters:
# Invalid: my-package, my_package@test, 123package
# Valid: my_package, my_valid_package, package_test
```

## **Support**

### Help Resources

* **Documentation**: [docs/](docs/)
* **Issues**: [GitHub Issues](https://github.com/flutterpilot/fpd_toolkit/issues)
* **Discussions**: [GitHub Discussions](https://github.com/flutterpilot/fpd_toolkit/discussions)

## **License**

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

## **Author**

**Sebastián Larrauri** – [dash@flutterpilot.dev](mailto:dash@flutterpilot.dev)


