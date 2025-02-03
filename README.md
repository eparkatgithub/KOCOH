# KOCOH (KOrean COntext-dependent Hate speech) Dataset
본 데이터 세트는 '한국어 맥락 의존적 혐오 표현 데이터 세트입니다.

* 혐오 표현
  * 소수자(실질적인 정치‧사회적 권력이 열세이면서 공통의 정체성을 가진 집단)에 대한 편견 또는 차별을 확산시키거나 조장하는 행위 또는 어떤 개인, 집단에 대해 그들이 소수자로서의 속성을 가졌다는 이유로 멸시‧모욕‧위협하거나 그들에 대한 차별, 적의, 폭력을 선동하는 표현(홍성수, 2018)
* 맥락 의존적 혐오 표현
  * 맥락에 기대어 혐오적으로 해석되는 혐오 표현
  * 즉, 맥락 없이 해당 문장만으로는 무표적이거나 심지어 긍정적으로 해석하는 것도 가능
  * 예시
    |Context|Comment|Hate speech|
    |:---|:---|:---:|
    |여성 고용이 미흡해 정부가 불이익을 준 기업의 이름이 공개되었다.|믿을 만한 그룹이라는 얘기네|1|
    |직원에게 높은 수준의 복지를 제공한 기업의 이름이 공개되었다.|믿을 만한 그룹이라는 얘기네|0|

# 데이터 설명(Data Description)
* 수집 플랫폼: [디시인사이드 실시간 베스트 갤러리](https://gall.dcinside.com/board/lists/?id=dcbest)
* 수집 기간: 2024년 6월 2일~23일
* 데이터 세트 규모
  |Total|Type 1|Type 2|Type 3|
  |:---:|:---:|:---:|:---:|
  |2,005|539|539|927|
* 데이터 유형 설명 및 예시
  <table>
    <thead>
      <tr>
        <th></th>
        <th>Context</th>
        <th>Comment</th>
        <th>Hate speech</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th rowspan="2">type 1</th>
        <td>Actually written context A</td>
        <td>Actually written comment C</td>
        <td rowspan="2">Yes</td>
      </tr>
      <tr>
        <td>광주광역시의 맛있는 음식 다섯 가지를 소개했다.</td>
        <td>먹고 싶은데 여권 들고 가기 귀찮아::</td>
      </tr>
      <tr>
        <th rowspan="2">Type 2</th>
        <td>Created context B</td>
        <td>Comment D(same as comment C)</td>
        <td rowspan="2">No</td>
      </tr>
      <tr>
        <td>일본 오사카의 맛있는 음식 다섯 가지를 소개했다.</td>
        <td>먹고 싶은데 여권 들고 가기 귀찮아::</td>
      </tr>
      <tr>
        <th rowspan="2">Type 3</th>
        <td>Actually written context A</td>
        <td>Actually written comment E</td>
        <td rowspan="2">No</td>
      </tr>
      <tr>
        <td>광주광역시의 맛있는 음식 다섯 가지를 소개했다.</td>
        <td>역시 광주다</td>
      </tr>
    </tbody>
  </table>
* 데이터 세트 열 구성
  <table>
    <thead>
      <tr>
        <th>Column</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>index</th>
        <td>Data index</td>
      </tr>
      <tr>
        <th>set</th>
        <td>Post index</td>
      </tr>
      <tr>
        <th>type</th>
        <td>Type number (1~3 labeling)</td>
      </tr>
      <tr>
        <th>date</th>
        <td>The date the DC Inside post was written</td>
      </tr>
      <tr>
        <th>link</th>
        <td>The link to the DC Inside post</td>
      </tr>
      <tr>
        <th>title</th>
        <td>The title of the DC Inside post</td>
      </tr>
      <tr>
        <th>context</th>
        <td>Summary of the DC Inside post content / Created context</td>
      </tr>
      <tr>
        <th>comment</th>
        <td>Comments collected from DC Inside</td>
      </tr>
      <tr>
        <th>hate speech</th>
        <td>Whether it is hate speech (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>gender</th>
        <td>Target: gender (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>disability</th>
        <td>Target: disability (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>race/nation</th>
        <td>Target: race/nation (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>region</th>
        <td>Target: region (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>age</th>
        <td>Target: age (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>note</th>
        <td>Ikiyano style (-no)</td>
      </tr>
    </tbody>
  </table>

# 인용(Citation)
```

```

# 참고 문헌(Reference)
홍성수. (2018). _말이 칼이 될 때: 혐오표현은 무엇이고 왜 문제인가?._ 어크로스.