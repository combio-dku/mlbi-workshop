## 바이오인포매틱스 실습 워크숍
# Bioinformatics Workshop
- __교육 대상:__ &nbsp;&nbsp; NGS 데이터를 이용한 바이오인포매틱스 분석 흐름을 실습하려는 학부생, 대학원생, 연구원
- __교육 목표:__ &nbsp;&nbsp; WES 변이 분석, short-read bulk RNA-seq 분석, PacBio long-read RNA-seq 분석의 기본 파이프라인을 Colab 환경에서 실습하고 주요 파일 형식과 분석 결과를 해석할 수 있도록 한다

> **노트북 실행 안내:** 아래 노트북 링크를 클릭하면 이 저장소의 실습 파일이 Google Colab에서 바로 열립니다. Google 계정으로 로그인한 뒤 **연결** 버튼을 눌러 실습을 시작하세요. 수정 내용을 보관하려면 **파일 → 드라이브에 사본 저장**을 이용하세요. 로컬 실행은 저장소의 `Notebooks/` 파일을 JupyterLab 또는 Jupyter Notebook으로 열면 됩니다.

## 사전 준비
- __개인 준비:__ &nbsp;&nbsp; 무선랜과 웹브라우저가 설치된 Laptop (Tablet도 가능은 한데 추천하지는 않습니다), __Google 계정__
- __사용 언어:__ &nbsp;&nbsp; python3, linux shell command &nbsp; (Google Colab을 사용할 예정이라 뭔가 따로 설치할 필요는 없습니다.)
- __발표 자료:__ &nbsp;&nbsp; 따로 이메일로 송부 드립니다.
- __사전 지식:__
  - __필수:__ 생명과학/생화학/유전체학(Central dogma 포함)에 대한 기본 지식(관련/유사 학과 전공자)
  - __필수:__ Python coding 문법, 함수정의 및 다양한 자료 구조에 대한 기초 지식
  - __권장:__ Linux shell command와 파일/디렉토리 구조에 대한 기초 지식

## 실습 자료
1. &nbsp;&nbsp; [실습 A 주피터 노트북](https://colab.research.google.com/github/combio-dku/mlbi-workshop/blob/main/Notebooks/Bi_practice_A_WES_v07_251215.ipynb): 여러가지 파일 형식들, Whole Genome/Exome Seq., read alignment, variant calling, copy number variation analysis
2. &nbsp;&nbsp; [실습 B 주피터 노트북](https://colab.research.google.com/github/combio-dku/mlbi-workshop/blob/main/Notebooks/Bi_practice_B_RNA-seq_v08_251215.ipynb): Short-read bulk RNA-seq, STAR alignment, gene expression quantification, DEG/DEIso analysis
3. &nbsp;&nbsp; [실습 C 주피터 노트북](https://colab.research.google.com/github/combio-dku/mlbi-workshop/blob/main/Notebooks/Bi_practice_C_RNA-seq-PB_v08_251216.ipynb): PacBio long-read RNA-seq, minimap2 alignment, transcript assembly, isoform-level interpretation

