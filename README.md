# core-config-bundle
Base Core configuration bundle for workshop

1. Fork this repository.
2. Create a GitHub PAT
3. In your CloudBees Core Jenkins Master, encrypt your GitHub PAT
4. Replace the two `REPLACE_WITH_JENKINS_ENCODED_PAT` placeholders with your Jenkins encrypted GitHub PAT in the `jenkins.yaml` file
5. Replace the  `REPLACE_WITH_YOUR_GITHUB_USERNAME` placeholder with your GitHub username in the `jenkins.yaml` file
6. Create a Multibranch Pipeline project in your CloudBees Core Jenkins Master using this repo as the GitHub source
