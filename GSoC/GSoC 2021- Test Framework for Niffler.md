# GSoC 2021 Final Report

## Overview

**Project**: A Testing Framework for Niffler DICOM frameworks for Continuous Integration

**Description**: This Project aims to develop unit and integration tests for the Niffler modules and implement automated testing using Continuous Integration. The project will introduce checks to confirm that the commits to the codebase do not break the functionality of Niffler, before each major production release. These tests will significantly reduce the potential for bugs in the codebase, allowing the deployment of newer versions seamlessly.

**Student**: Chinmay Vibhute

**Org**: Department of Biomedical Informatics (BMI), Emory University School of Medicine

**Mentors**:

- Ramon Correa
- Pradeeban Kathiravelu
- Hari Trivedi

## Work Done

- Test Environment Setup and Unit Tests for PNG Extraction Module [#140](https://github.com/Emory-HITI/Niffler/pull/140)
- Code Refactoring and Unit tests for Metadata Extraction Module [#151](https://github.com/Emory-HITI/Niffler/pull/151)
- Unit Tests for Cold Extraction Module [#189](https://github.com/Emory-HITI/Niffler/pull/189)
- Integration Tests for PNG Extraction module and added Test Data for all tests [#191](https://github.com/Emory-HITI/Niffler/pull/191)
- Unit and Integration Tests for Dicom Anonymization Module [#192](https://github.com/Emory-HITI/Niffler/pull/192)
- Implemented Automated Testing using GitHub Actions [#212](https://github.com/Emory-HITI/Niffler/pull/212) & [#214](https://github.com/Emory-HITI/Niffler/pull/214)
- Code Commenting, Test Documentation and bug fixes [#211](https://github.com/Emory-HITI/Niffler/pull/211) and [#217](https://github.com/Emory-HITI/Niffler/pull/217)

All my contributions can be found [here](https://github.com/Emory-HITI/Niffler/pulls?q=type%3Apr+author%3Achinvib66+)

## Highlights and Challenges

The most challenging part of the project was mocking and maintaining module-level state variables which were declared globally. Based on the current code structure of Niffler modules, `pytest-mock` could not mock these state variables and thus I had to set & reset the required states manually for each test suite.

Understanding the codebase, its specific use cases, along with the edge cases involved, was also another challenge that took me some time to understand and work with.

Another major challenge was figuring out how to implement automated _integration_ tests for modules that ran processes involving timestamp-based execution. At the moment the project has to rely on manual testing and verification for `Cold Extraction` and `Meta Extraction`.

## Conclusion

I’ve had a wonderful time during these 2-3 months and have learned plenty of things. Special thanks to my mentor, _Ramon Correa_ for his constant support throughout GSoC '21.
