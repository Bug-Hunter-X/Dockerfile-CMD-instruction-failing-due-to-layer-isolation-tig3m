# Dockerfile Bug: Layer Isolation Issue in CMD

This repository demonstrates a common error in Dockerfiles related to layer isolation.  The `CMD` instruction tries to access a file created in an earlier `RUN` instruction, but the file is not available in the `CMD` layer. This results in the command failing.

The solution provides the correct approach to ensure the file is accessible within the `CMD` execution environment.

**Bug:** The `Dockerfile_bug.txt` file shows the incorrect usage of `CMD` leading to the error.

**Solution:** The `Dockerfile_solution.txt` file demonstrates the correct way to handle this by copying the file to the final layer or using a multi-stage build.