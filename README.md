<p align="center">
<img src="./assets/leetcomp_banner.png">
<sub>https://kuutsav.github.io/leetcode-compensation</sub>
</p>

<p align="center">
<a href="https://github.com/kuutsav/leetcode-compensation/actions/workflows/data-refresh.yaml"><img src="https://github.com/kuutsav/leetcode-compensation/actions/workflows/data-refresh.yaml/badge.svg" alt="automatic-data-update"/ ></a>
<a href="https://github.com/kuutsav/leetcode-compensation/actions/workflows/pages/pages-build-deployment"><img src="https://github.com/kuutsav/leetcode-compensation/actions/workflows/pages/pages-build-deployment/badge.svg" alt="pages-build-deployment" /></a>
<a href="http://mypy-lang.org/"><img src="http://www.mypy-lang.org/static/mypy_badge.svg" alt="Checked with mypy" /></a>
</p>

**[LeetCode Compensation](https://kuutsav.github.io/leetcode-compensation)** is a tool that helps you find **Software Engineer Salary in India** by:
- Fetching compensation data from Leetcode forums.
- Updating Bi-weekly through GitHub action PRs.
- Using LLMs for parsing and sanitizing structured data from posts, followed by aggregation.

> [!WARNING]
> We filter out posts with negative votes. To that end, we have added a 2-day data refresh delay to allow the votes to accumulate.

## Getting Started

Install uv from [Standalone Installers](https://github.com/astral-sh/uv) or from [PyPI](https://pypi.org/project/uv/):

To create a virtual environment:

```shell
uv venv  # Create a virtual environment at .venv.
```

To activate the virtual environment:

```shell
# On macOS and Linux.
source .venv/bin/activate

# On Windows.
.venv\Scripts\activate
```

To install a package into the virtual environment:

```shell
uv pip install -r requirements.txt  # Install from a requirements.txt file.
```

## Updating data

> [!NOTE]
> Make sure you are in a venv with all the packages installed and have llm inference setup (look at the llms section of config.toml) using any of the supported options like ollama(local), vllm(local), openrouter(api)

```bash
$ export PYTHONPATH=.
$ python leetcomp/refresh.py
$ python leetcomp/parse.py
```

## Roadmap

- [x] Sort by Compensation and Yoe
- [x] Add pagination
- [x] Filters for Yoe, Compensation
- [x] Search for Companies and Locations

## Contributions

PRs are welcome but please go through [CONTRIBUTING.md](CONTRIBUTING.md) before raising a PR.
