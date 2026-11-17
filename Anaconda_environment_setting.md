# Anaconda 분석 환경 구축

Google Colab으로 실습할 경우 아래 설치 과정은 필요하지 않습니다. 이 문서는 개인 컴퓨터에서 Jupyter Notebook을 실행하려는 경우를 위한 안내입니다.

## Anaconda 설치 및 실행
1. [여기](https://www.anaconda.com/download/success)에서 Anaconda Distribution을 다운 받습니다. (OS와 CPU에 맞는 설치파일을 다운 받되 Windows나 Mac의 경우 Graphical Installer를 추천합니다. Mac은 Apple Silicon과 Intel을 구분하여 선택하세요.)
2. 다운받은 설치파일을 실행시켜 Anaconda를 설치합니다. (동의를 한번하고 Next 버튼을 몇번 누르고 Install 버튼을 누르면 됩니다.)
3. 설치가 완료되면 Windows의 경우 시작 메뉴 -> 'Anaconda (anaconda3)'에, Mac의 경우 응용 프로그램(Applications)에 "Anaconda Navigator" 가 생깁니다.
4. "Anaconda Navigator"를 실행하면 창이 하나 뜨고 "JupyterLab"과 "Jupyter Notebook" 패널이 보입니다. (아래 그림)
5. "JupyterLab"과 "Jupyter Notebook" 중 하나의 Launch 버튼을 클릭하면 브라우저에서 주피터 창이 열리는데 그러면 사용 준비가 된 것입니다. 가지고 있는 주피터 노트북 파일이 있는 경로로 들어가 해당 주피터 노트북을 열거나 새로 주피터 노트북을 만들어 사용하면 됩니다.

![image](https://github.com/user-attachments/assets/0f4d9cfb-14cf-4711-84d5-f2b442ee3582)

- Anaconda Navigator 창 상단 중앙에 보면 "base (root)"라는 Drop down 메뉴가 보이는데 현재 "base" conda 환경에서 실행 중이라는 의미입니다.
- "base" conda 환경에도 기본적인 Python 패키지가 설치되어 있지만, 실습용 패키지는 별도 conda 환경을 만들어 설치하는 것을 권장합니다.

## Conda 환경 만들기
- "base" 환경에는 배포판에 포함된 Python과 여러 기본 패키지가 설치되어 있는데 (호환성 문제 등으로) 특정 python 버전을 사용하고 싶은 경우 새로 conda 환경을 만들어야 하고 R을 사용하고자 한다고 해도 새로 conda 환경을 만들어 사용하는 것이 좋습니다.
- Conda 환경의 생성은 Anaconda Navigator에서도 좌측 메뉴에서 Environment를 선택하여 할 수 있지만 이보다는 터미널에서 conda command를 이용하는 것이 보다 편리합니다.
- [여기](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)를 참고하여 conda 환경을 생성하고 필요한 패키지를 설치하여 사용하면 되는데 터미널 열기는 Windows의 경우 시작 -> Anaconda (anaconda3) -> Anaconda Prompt 를 실행하여 터미널을 열면 되고 Mac OS의 경우 응용 프로그램에서 Terminal (터미널)을 실행시키면 됩니다.

Python 실습용 환경은 아래와 같이 만들 수 있습니다. `python=3.12`는 버전 지정 예시이며, 실습 노트북에서 요구하는 버전이 있으면 그에 맞추세요. 추가 패키지는 각 노트북의 설치 안내를 따릅니다.

```bash
conda create -n mlbi_env --override-channels -c conda-forge python=3.12 notebook jupyterlab
conda activate mlbi_env
jupyter lab
```

아래 R 환경도 포함하여 설치 채널은 `conda-forge`로 통일합니다. `--override-channels`는 해당 설치 명령에서 다른 채널을 사용하지 않도록 합니다.

## R을 사용하기 위한 Conda 환경 만들기 및 주피터에서 R 사용하기
Anaconda Navigator에서도 좌측 메뉴에서 Environment를 선택하여 R을 사용하기 위한 conda 환경을 생성할 수 있지만 R 버전이 맞지않을 수 있어 터미널에서 conda command를 이용하는 것이 좋습니다. 다음과 같이 진행하면 됩니다.

1. 위의 설명을 참고하여 터미널을 엽니다. `conda --version`으로 conda 명령이 실행되는지 확인합니다.
2. 터미널에서 다음의 명령으로 conda 환경을 새로 하나 만듭니다. `conda create -n r_env --override-channels -c conda-forge notebook jupyterlab r-essentials`. (여기서 `r_env`는 새로 만들어지는 환경의 이름입니다. 다른 이름을 사용해도 좋습니다. Jupyter와 R 패키지를 함께 설치하며, 운영체제와 패키지 의존성을 만족하는 버전이 선택됩니다.)
3. (선택 사항) 특정 Python 또는 R 버전이 필요하면 **2번 명령을 실행할 때** 끝에 `python=버전` 또는 `r-base=버전`을 추가합니다. 같은 이름의 환경을 다시 생성하는 단계가 아닙니다. 지정한 버전은 운영체제와 다른 패키지에 따라 설치가 불가능할 수 있습니다.
4. 다음의 명령으로 새로 만든 conda 환경을 활성화합니다. `conda activate r_env`. (그러면 Command prompt 앞에 `(r_env)`가 표시됩니다.)
5. 이제 Command prompt에서 `jupyter notebook` 혹은 `jupyter lab` 명령을 실행하면 브라우저에서 주피터가 열리고, 노트북을 열 때 R 커널을 선택하여 R 명령을 사용할 수 있습니다.

- R 커널이 보이지 않으면 `r_env`가 활성화된 터미널에서 `jupyter kernelspec list`로 확인합니다. R 커널이 목록에 없다면 같은 터미널에서 `R`을 실행한 뒤 `IRkernel::installspec()`으로 등록하고 Jupyter를 다시 실행합니다.
