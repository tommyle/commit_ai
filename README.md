# Commit AI

A command-line application built with Dart that generates git commit messages using OpenAI's ChatGPT. This app runs `git diff` in the current working directory, sends the output to ChatGPT, and presents multiple commit message suggestions. The user can then choose a message, and the app will commit the changes using the selected message.

## Prerequisites

- Dart SDK (latest version): https://dart.dev/get-dart
- A valid OpenAI API key: https://beta.openai.com/signup/

## Installation

1. Clone the repository:

```bash
git clone https://github.com/tommyle/commit_ai.git
```

2. Compile the app to a native executable:

```bash
dart compile exe lib/commit_ai.dart -o build/_commit_ai
```

## Usage

1. Set your OpenAI API key:

```bash
./commit_ai --set_api_key
```

   You'll be prompted to enter your API key, which will be saved to a local file for future use.

2. Run the app to generate a commit message and commit the changes:

```bash
./commit_ai
```

   The app will display multiple commit message suggestions based on the `git diff` output. Choose a message and the app will commit the changes using the selected message.

### Optional arguments

- `--help` or `-h`: Display help information.

```bash
./commit_ai --help
```

- `--show_diff` or `-d`: Show the git diff output.

```bash
./commit_ai --show_diff
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
