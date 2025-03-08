# KOCOH (KOrean COntext-dependent Hate speech) Dataset
* 논문: [KOCOH: 맥락 의존적 혐오 표현 탐지를 위한 데이터 세트](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART003173761)
* 저자: [박은아](https://github.com/eparkatgithub), [송상헌](http://corpus.mireene.com/)
* 연락: dmsdk1993@korea.ac.kr
* [Hugging Face](https://huggingface.co/datasets/E-Park/KOCOH)🤗
 
KOCOH는 '한국어 맥락 의존적 혐오 표현' 데이터 세트입니다.

## 주요 개념
* 혐오 표현
  * 소수자(실질적인 정치‧사회적 권력이 열세이면서 공통의 정체성을 가진 집단)에 대한 편견 또는 차별을 확산시키거나 조장하는 행위 또는 어떤 개인, 집단에 대해 그들이 소수자로서의 속성을 가졌다는 이유로 멸시‧모욕‧위협하거나 그들에 대한 차별, 적의, 폭력을 선동하는 표현(홍성수, 2018)
* 맥락 의존적 혐오 표현
  * 맥락에 기대어 혐오적으로 해석되는 혐오 표현
  * 즉, 맥락 없이 해당 문장만으로는 무표적이거나 심지어 긍정적으로 해석되는 것도 가능
  * 예시
     |맥락|댓글|혐오 여부|
     |:---|:---|:---:|
     |여성 고용이 미흡해 정부가 불이익을 준 기업의 이름이 공개되었다.|믿을 만한 그룹이라는 얘기네|1|
     |직원에게 높은 수준의 복지를 제공한 기업의 이름이 공개되었다.|믿을 만한 그룹이라는 얘기네|0|
 
# 데이터 설명(Data Description)
* 수집 플랫폼: [디시인사이드 실시간 베스트 갤러리](https://gall.dcinside.com/board/lists/?id=dcbest)
* 수집 기간: 2024년 6월 2일~23일
* 데이터 세트 규모
  |전체|유형 1|유형 2|유형 3|
  |:---:|:---:|:---:|:---:|
  |2,005|539|539|927|
* 데이터 유형 설명 및 예시
  <table>
    <thead>
      <tr>
        <th></th>
        <th>맥락</th>
        <th>댓글</th>
        <th>혐오 여부</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th rowspan="2">유형 1</th>
        <td>실제로 쓰인 맥락 A</td>
        <td>실제로 쓰인 댓글 C</td>
        <td rowspan="2">1</td>
      </tr>
      <tr>
        <td>광주광역시의 맛있는 음식 다섯 가지를 소개했다.</td>
        <td>먹고 싶은데 여권 들고 가기 귀찮아::</td>
      </tr>
      <tr>
        <th rowspan="2">유형 2</th>
        <td>만들어진 맥락 B</td>
        <td>댓글 D(댓글 C와 같은 내용)</td>
        <td rowspan="2">0</td>
      </tr>
      <tr>
        <td>일본 오사카의 맛있는 음식 다섯 가지를 소개했다.</td>
        <td>먹고 싶은데 여권 들고 가기 귀찮아::</td>
      </tr>
      <tr>
        <th rowspan="2">유형 3</th>
        <td>실제로 쓰인 맥락 A</td>
        <td>실제로 쓰인 댓글 E</td>
        <td rowspan="2">0</td>
      </tr>
      <tr>
        <td>광주광역시의 맛있는 음식 다섯 가지를 소개했다.</td>
        <td>역시 광주다</td>
      </tr>
    </tbody>
  </table>
* 데이터 열 설명
  <table>
    <thead>
      <tr>
        <th>열 이름</th>
        <th>설명</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>index</th>
        <td>데이터 인덱스</td>
      </tr>
      <tr>
        <th>set</th>
        <td>글 인덱스(세트 인덱스)</td>
      </tr>
      <tr>
        <th>type</th>
        <td>유형 번호(1~3 주석)</td>
      </tr>
      <tr>
        <th>date</th>
        <td>디시인사이드 글이 쓰인 날짜</td>
      </tr>
      <tr>
        <th>link</th>
        <td>디시인사이드 글의 링크</td>
      </tr>
      <tr>
        <th>title</th>
        <td>디시인사이드 글의 제목</td>
      </tr>
      <tr>
        <th>context</th>
        <td>디시인사이드 글 내용의 요약/만들어진 맥락</td>
      </tr>
      <tr>
        <th>comment</th>
        <td>디시인사이드에서 수집된 댓글</td>
      </tr>
      <tr>
        <th>hate speech</th>
        <td>혐오 표현 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>gender</th>
        <td>혐오 대상 성별 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>disability</th>
        <td>혐오 대상 장애 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>race/nation</th>
        <td>혐오 대상 인종/국가 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>region</th>
        <td>혐오 대상 지역 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>age</th>
        <td>혐오 대상 연령 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>note</th>
        <td>이기야노체(일베 말투)</td>
      </tr>
    </tbody>
  </table>
## 참고 문헌
홍성수. (2018). [*말이 칼이 될 때: 혐오표현은 무엇이고 왜 문제인가?*](https://scholarworks.sookmyung.ac.kr/handle/2020.sw.sookmyung/20524). 어크로스.

## 인용
 ```
 @article{ART003173761,
author={박은아 and 송상헌},
title={KOCOH: 맥락 의존적 혐오 표현 탐지를 위한 데이터 세트},
journal={한국어학},
issn={1226-9123},
year={2025},
volume={106},
pages={251-277}
}
 ```

## 라이선스
