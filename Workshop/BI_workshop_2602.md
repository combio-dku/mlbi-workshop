## 바이오인포매틱스 실습 워크숍
# Bioinformatics Workshop
- __교육 대상:__ &nbsp;&nbsp; NGS 데이터를 이용한 바이오인포매틱스 분석 흐름을 실습하려는 학부생, 대학원생, 연구원
- __교육 목표:__ &nbsp;&nbsp; WES 변이 분석, short-read bulk RNA-seq 분석, PacBio long-read RNA-seq 분석의 기본 파이프라인을 Colab 환경에서 실습하고 주요 파일 형식과 분석 결과를 해석할 수 있도록 한다

> **노트북 실행 안내:** 아래 노트북 링크는 이 저장소의 `Notebooks/` 파일을 엽니다. Google Colab에서 실행하려면 노트북을 다운로드한 후 Colab의 **파일 → 노트북 열기 → 업로드**에서 선택하세요. 로컬에서는 JupyterLab 또는 Jupyter Notebook으로 열 수 있습니다.

## 사전 준비
- __개인 준비:__ &nbsp;&nbsp; 무선랜과 웹브라우저가 설치된 Laptop (Tablet도 가능은 한데 추천하지는 않습니다), __Google 계정__
- __사용 언어:__ &nbsp;&nbsp; python3, linux shell command &nbsp; (Google Colab을 사용할 예정이라 뭔가 따로 설치할 필요는 없습니다.)
- __발표 자료:__ &nbsp;&nbsp; 따로 이메일로 송부 드립니다.
- __사전 지식:__
  - __필수:__ 생명과학/생화학/유전체학(Central dogma 포함)에 대한 기본 지식(관련/유사 학과 전공자)
  - __필수:__ Python coding 문법, 함수정의 및 다양한 자료 구조에 대한 기초 지식
  - __권장:__ Linux shell command와 파일/디렉토리 구조에 대한 기초 지식

## 실습 자료
1. &nbsp;&nbsp; [실습 A 주피터 노트북](../Notebooks/Bi_practice_A_WES_v07_251215.ipynb): 여러가지 파일 형식들, Whole Genome/Exome Seq., read alignment, variant calling, copy number variation analysis
2. &nbsp;&nbsp; [실습 B 주피터 노트북](../Notebooks/Bi_practice_B_RNA-seq_v08_251215.ipynb): Short-read bulk RNA-seq, STAR alignment, gene expression quantification, DEG/DEIso analysis
3. &nbsp;&nbsp; [실습 C 주피터 노트북](../Notebooks/Bi_practice_C_RNA-seq-PB_v08_251216.ipynb): PacBio long-read RNA-seq, minimap2 alignment, transcript assembly, isoform-level interpretation

