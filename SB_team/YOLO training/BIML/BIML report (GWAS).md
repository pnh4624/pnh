BIML(GWAS)
================

- <a href="#gwas란-무엇인가" id="toc-gwas란-무엇인가">GWAS란 무엇인가?</a>
  - <a href="#gwasgenome-wide-association-study전장-유전체-연관-분석"
    id="toc-gwasgenome-wide-association-study전장-유전체-연관-분석">GWAS(Genome
    Wide Association Study,전장 유전체 연관 분석)</a>
  - <a href="#gwas-방법론" id="toc-gwas-방법론">GWAS 방법론</a>
  - <a href="#유전체-분석을-위한-개념"
    id="toc-유전체-분석을-위한-개념">유전체 분석을 위한 개념</a>
  - <a href="#post-gwas-분석의-이론과-방법론"
    id="toc-post-gwas-분석의-이론과-방법론">Post-GWAS 분석의 이론과
    방법론</a>
  - <a href="#대표적인-연구-결과의-소개"
    id="toc-대표적인-연구-결과의-소개">대표적인 연구 결과의 소개</a>

## GWAS란 무엇인가?

### GWAS(Genome Wide Association Study,전장 유전체 연관 분석)

#### GWAS의 의미와 목표

    모든 유전체 위치에 대해서, 관심을 가진 형질(Target phenotype)과 연관성을 갖는 유전자의 위치(causal locus)를 찾는다.

#### 도입 개념

- LD(Linkeage Desequilibrium, 연관 비평형) & LD block 연관괴어있는
  유전자들은 연관 비평형을 나타낸다. 연관은 block의 형태로 여러 bp,
  유전자들이 한 블럭에 묶여있다. 그리고 한 블럭 안에서 그 블럭을
  대표하는 SNP를 선출할 수 있다.

- Causal locus, phenotype and typed marker locus

1.  typed marker locus(우리가 알고있는 locus)와 causal
    locus(unobserved)는 직접적인 관계가 있다.  
2.  typed marker locus는 phenotype에 간접적인 영향을 준다.  
3.  phenotype에과 관계있는 typed marker locus을 찾으면, causal locus의
    후보군을 선출할 수 있다.

### GWAS 방법론

work flow

1.  data QC
2.  imputation
3.  Association analysis
4.  Logistic/linear regression (unrelated): PLINK – Mixed effects
    regression (including related): SAIGE, BOLT-LMM, REGENIE •
    Visualization – QQ plot: CM-PLOT – Manhattan plot: CM-PLOT error &
    quality control

- Sample QC

- Variant QC

- Population structure & sub population  
  무작위가 아닌 연관된 데이터끼리 결과가 나옴

- Hardy-Weinberg equilibrium (HWE) test  
  genotyping error 측정

- PLINK: QC software

#### Impuutation

관찰되지 않은 genotype을 통계적 기법을 통해 추정하는 것 나와 비슷한 ref
genome으로 나의 빈 SNP 추론(LD)

HRC TOPMed imputation server

- QQ plot 예상 vs 실제 비교 population이 데이터를 왜곡한다.

  #### Association Analysis

GWAS case와 control 사이에서 유의한 빈도의 차이를 보이는 SNP는 이 둘의
차이를 설명하는데에 연관되어있다. Basic association test: pearson’s
chi-square test

Regression anlaysis

Mixed effects model

Genome-wide significance level

Genome-wide significance level • Multiple-testing (comparisons) problem
– the problem that arises when many null hypotheses are tested; some
significant results are likely even if all the hypotheses are false •
Bonferroni’s correction (more stringent method) – 0.05 / \# of tested
variants (usually assuming 1M) – 0.05 / 1,000,000 = 5E-08 • False
discovery rate (less stringent method)

#### Visualization

Manhattan plot Regional plot of association Phenome-wide analysis
(PheWAS)

### 유전체 분석을 위한 개념

#### SNV(Single Nucleotide Variant)

- MAF (Minor Allele Fequency)  
  일반 인구에서 minor allele의 관측 빈도

- MAF와 effect size에 따른 variants의 분류  
  ![](images/paste-C6877D02.png)

cf) frequency의 분류

high (\<05%), intermediate, (0.5\~1%), common (1\~5%)

#### 유전체 분석을 위한 프로젝트

- HAPMAP Project: Tag SNPs에 집중하여 casual variant를 간접적으로 조사

- 1000 Genome Project(1KG): 다양한 SNP Data의 확보

- Biobank: 각 집단의 특성을 반영하여 디테일한 유전 데이터 조사

### Post-GWAS 분석의 이론과 방법론

### 대표적인 연구 결과의 소개
