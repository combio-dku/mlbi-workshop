# VS Code 설치 및 Codex / Claude Code 계정 연결

이 문서는 개인 컴퓨터에 Visual Studio Code(VS Code)를 설치하고, **Codex 또는 Claude Code 중 하나를 유료 구독 계정으로 연결**하여 워크샵 실습에 사용하는 방법을 안내합니다. 두 서비스를 모두 구독할 필요는 없습니다.

> 공식 문서 확인일: 2026-11-17. 화면 이름과 구독별 제공 기능·사용량은 변경될 수 있습니다. 이 안내는 VS Code 데스크톱 앱의 공식 확장을 기준으로 합니다.

## 1. 준비 사항

- 인터넷 연결이 가능한 Windows, macOS 또는 Linux 컴퓨터
- 아래 중 사용할 서비스의 계정

| 사용할 도구 | 개인 유료 계정 예시 | 설치할 공식 확장 |
| --- | --- | --- |
| OpenAI Codex | ChatGPT Plus 또는 Pro | Codex — OpenAI (`openai.chatgpt`) |
| Anthropic Claude Code | Claude Pro 또는 Max | Claude Code — Anthropic (`anthropic.claude-code`) |

이미 해당 구독을 사용하고 있다면 그 계정으로 로그인합니다. 새로 구독하려는 경우 [ChatGPT](https://chatgpt.com/) 또는 [Claude](https://claude.ai/)의 계정 설정에서 요금제와 제공 기능을 확인한 뒤 선택하세요. 조직 계정은 관리자에게 사용 권한을 확인합니다. 지원 계정은 [Codex 공식 확장 안내](https://marketplace.visualstudio.com/items?itemName=openai.chatgpt)와 [Claude Code 계정 안내](https://code.claude.com/docs/en/authentication)를 참고하세요.

**구독 로그인과 API 사용은 결제 방식이 다릅니다.** 아래 절차에서는 ChatGPT/Claude 구독으로 로그인하므로 API 키를 발급받을 필요가 없습니다. Codex의 API 키 로그인은 OpenAI Platform의 사용량 기반 과금이며, Claude Console도 Claude 구독 로그인과 별도입니다. 유료 구독에도 사용량 제한이 있으므로 무제한 사용을 전제로 하지 마세요. [Codex 인증 안내](https://developers.openai.com/codex/auth/), [Claude Code 인증 안내](https://code.claude.com/docs/en/authentication)

## 2. VS Code 설치 및 실습 폴더 열기

1. [VS Code 다운로드 페이지](https://code.visualstudio.com/download)에서 운영체제와 CPU에 맞는 설치파일을 받습니다. macOS에서는 Apple Silicon과 Intel을 구분합니다.
2. Windows에서는 설치파일을 실행하여 안내에 따라 설치합니다. macOS에서는 내려받은 앱을 응용 프로그램(Applications) 폴더로 옮깁니다. Linux에서는 배포판에 맞는 패키지를 설치합니다.
3. VS Code를 실행합니다.
4. **File → Open Folder…(파일 → 폴더 열기)**에서 `mlbi-workshop` 폴더를 선택합니다. 저장소가 없다면 [GitHub 저장소](https://github.com/combio-dku/mlbi-workshop)에서 **Code → Download ZIP**으로 내려받아 압축을 먼저 풉니다.
5. 왼쪽 탐색기에 `README.md`, `Workshop`, `Notebooks`가 보이는지 확인합니다. Workspace Trust 확인창이 나타나면 직접 준비하고 내용을 신뢰하는 실습 폴더인지 확인하여 진행합니다.

VS Code 설치 자체와 AI 서비스 구독은 별개입니다. 상세한 OS별 절차는 [VS Code 공식 설치 안내](https://code.visualstudio.com/docs/setup/setup-overview)를 참고하세요.

## 3A. Codex 연결 — ChatGPT 계정 사용

1. 왼쪽 **Extensions(확장)** 아이콘을 클릭합니다. 단축키는 Windows/Linux에서 `Ctrl+Shift+X`, macOS에서 `Cmd+Shift+X`입니다.
2. `Codex`를 검색하여 게시자가 **OpenAI**인 공식 확장을 설치합니다. [공식 설치 페이지](https://marketplace.visualstudio.com/items?itemName=openai.chatgpt)에서도 설치할 수 있습니다.
3. **Codex** 아이콘을 눌러 패널을 엽니다. 아이콘이 보이지 않으면 명령 팔레트(`Ctrl+Shift+P` / `Cmd+Shift+P`)에서 `Codex: Open Codex Sidebar`를 실행합니다.
4. **Sign in with ChatGPT**를 선택합니다.
5. 브라우저에서 **구독 중인 ChatGPT 계정**으로 로그인하고 연결을 완료합니다. VS Code로 돌아온 뒤 계정과 작업할 워크스페이스를 확인합니다.
6. 아래 “연결 확인”의 예시 질문을 입력합니다.

이 방식에서는 **Use API Key**를 선택하지 않습니다. 설치·실행은 [Codex IDE 안내](https://developers.openai.com/codex/ide/), 로그인은 [Codex 인증 안내](https://developers.openai.com/codex/auth/)를 참고하세요.

## 3B. Claude Code 연결 — Claude 계정 사용

1. VS Code의 **Extensions(확장)**에서 `Claude Code`를 검색합니다.
2. 게시자가 **Anthropic**인 공식 확장을 설치합니다. [공식 설치 페이지](https://marketplace.visualstudio.com/items?itemName=anthropic.claude-code)에서도 설치할 수 있습니다.
3. 명령 팔레트(`Ctrl+Shift+P` / `Cmd+Shift+P`)에서 `Claude Code`를 검색하고 **Open in New Tab**을 선택합니다.
4. 처음 나타나는 화면에서 **Sign in**을 누릅니다.
5. 브라우저에서 **유료 구독 중인 Claude 계정**으로 로그인하고 연결을 완료합니다. 계정 유형을 선택하는 화면에서는 Claude 구독 계정을 선택합니다.
6. VS Code로 돌아와 아래 “연결 확인”의 예시 질문을 입력합니다.

확장 패널 사용에 필요한 CLI는 확장에 포함되어 있습니다. 터미널에서 직접 `claude` 명령을 사용하려는 경우에만 별도의 CLI 설치가 필요합니다. [Claude Code의 VS Code 공식 안내](https://code.claude.com/docs/en/vs-code)

Windows에서 Bash 명령도 사용하려면 [Git for Windows](https://git-scm.com/downloads/win)를 설치할 수 있습니다. 현재 공식 안내에서는 이를 선택 사항으로 설명합니다. [Windows 설정 안내](https://code.claude.com/docs/en/setup#set-up-on-windows)

## 4. 연결 확인 및 첫 사용

`README.md`를 열고 Codex 또는 Claude Code 패널에 다음과 같이 입력합니다.

> 이 저장소의 README.md를 읽고 어떤 워크샵이 있는지 한국어로 설명해 줘. 파일은 수정하지 마.

실제 파일 내용에 맞는 답변이 오면 기본 연결이 된 것입니다. 이후에는 노트북이나 코드 파일을 열고 원하는 작업을 구체적으로 요청합니다.

- 설명 요청: “이 노트북에서 train/test split을 하는 이유를 설명해 줘.”
- 오류 확인: “아래 오류 메시지의 원인을 설명하고 수정할 부분을 알려 줘.”
- 수정 요청: “이 함수에 입력값 확인을 추가하고, 무엇을 바꿨는지 설명해 줘.”

AI가 제안한 수정은 변경 내용을 확인하고, 코드 실행 결과도 직접 확인합니다. 처음에는 설명 요청부터 시작하면 도구의 동작을 익히기 쉽습니다.

## 5. VS Code에서 Python / Jupyter 실습하기

AI 계정 연결과 Python 실행 환경 준비는 별도입니다. 노트북을 직접 실행하려면 다음 설정도 진행합니다.

1. [Anaconda 환경 설정 안내](Anaconda_environment_setting.md)에 따라 실습 환경을 준비합니다.
2. VS Code의 확장에서 Microsoft의 **Python**(`ms-python.python`)과 **Jupyter**(`ms-toolsai.jupyter`)를 설치합니다.
3. `Notebooks/`의 `.ipynb` 파일을 엽니다.
4. 노트북 우측 상단의 **Select Kernel(커널 선택)**에서 준비한 Python 환경(예: `mlbi_env`)을 선택합니다.
5. 패키지 설치나 커널 설정 안내가 나타나면 **선택한 실습 환경**에 필요한 항목을 설치하고, 노트북의 셀을 순서대로 실행합니다.

간단한 셀에서 아래 코드를 실행하면 실제로 사용 중인 Python 경로를 확인할 수 있습니다.

```python
import sys
print(sys.executable)
```

AI가 코드를 설명할 수 있어도 커널과 패키지가 준비되지 않으면 노트북은 실행되지 않습니다. R 노트북은 별도의 R 환경과 커널이 필요합니다. [VS Code의 Jupyter 공식 안내](https://code.visualstudio.com/docs/datascience/jupyter-notebooks)

## 6. 잘 연결되지 않을 때

| 증상 | 먼저 확인할 내용 |
| --- | --- |
| 구독했는데 이용할 수 없음 | 브라우저와 확장에서 같은 계정으로 로그인했는지, 조직 계정이면 사용 권한이 있는지 확인합니다. |
| API 키 또는 Console 결제를 요구함 | 구독 계정 로그인 경로를 선택했는지 확인합니다. Codex는 **Sign in with ChatGPT**, Claude Code는 **Claude 구독 계정**으로 로그인합니다. |
| 설치 후 AI 패널이 보이지 않음 | 확장이 활성화되어 있는지 확인하고, 명령 팔레트에서 확장 이름을 검색합니다. 필요하면 **Developer: Reload Window**로 창을 다시 불러옵니다. |
| 사용량 제한 안내가 표시됨 | 계정의 사용량과 초기화 시점을 확인합니다. 확장 재설치로 구독 사용량이 초기화되지는 않습니다. |
| 노트북에서 패키지를 찾지 못함 | **Select Kernel**에서 선택한 환경과 패키지를 설치한 환경이 같은지 확인합니다. |

로그인이나 확장 실행 오류가 계속되면 해당 오류 메시지와 함께 [Codex 공식 안내](https://developers.openai.com/codex/ide/) 또는 [Claude Code 문제 해결 안내](https://code.claude.com/docs/en/troubleshooting)를 확인하세요.
