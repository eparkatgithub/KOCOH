# KOCOH (KOrean COntext-dependent Hate speech) Dataset
* 논문: [KOCOH: Korean Context-Dependent Hate Speech Dataset](https://doi.org/10.63317/5pnu2jn6awun)
* 저자: [박은아](https://github.com/eparkatgithub), [송상헌](http://corpus.mireene.com/)
* 연락처: dmsdk1993@korea.ac.kr
* [Hugging Face](https://huggingface.co/datasets/E-Park/KOCOH)🤗
 
KOCOH는 '한국어 맥락 의존적 혐오 표현' 데이터 세트입니다.
본 연구에 대한 더욱 자세한 설명은 [학위 논문](http://www.dcollection.net/handler/korea/000000306848)을 참고하시면 좋습니다.

## 업데이트 내역
* 2025/10/24: 버전2 업데이트
* 2025/01/31: 데이터 세트 첫 공개

## 주요 개념
* 혐오 표현
  * 사회적 소수자나 약자에 대한 편견, 차별을 기반으로 해당 집단이나 집단에 속한 개인을 멸시·비하·모욕하거나 그들에 대한 차별, 폭력을 선동하는 언어적 또는 비언어적 표현
* 맥락 의존적 혐오 표현
  * 맥락에 기대어 혐오적으로 해석되는 혐오 표현
  * 즉, 맥락 없이 해당 문장만으로는 무표적이거나 심지어 긍정적으로 해석되는 것도 가능
  * 예시
     |맥락|댓글|혐오 여부|
     |:---|:---|:---:|
     |여성 고용이 미흡해 정부가 불이익을 준 기업의 이름이 공개되었다.|믿을 만한 그룹이라는 얘기네|1|
     |직원에게 높은 수준의 복지를 제공한 기업의 이름이 공개되었다.|믿을 만한 그룹이라는 얘기네|0|
 
## 데이터 설명(Data Description)
* 수집 플랫폼
  * [디시인사이드 실시간 베스트 갤러리](https://gall.dcinside.com/board/lists/?id=dcbest)(2024년 6월 2일~23일)
  * [에펨코리아 포텐터짐 게시판](https://www.fmkorea.com/best)(2025년 1월 1일~21일)
* 데이터 세트 규모
  |전체|유형 1|유형 2|유형 3|
  |:---:|:---:|:---:|:---:|
  |3,000|764|764|1,472|
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
        <th>Index</th>
        <td>데이터 인덱스</td>
      </tr>
      <tr>
        <th>Set</th>
        <td>글 인덱스(세트 인덱스)</td>
      </tr>
      <tr>
        <th>Type</th>
        <td>유형 번호(1~3 주석)</td>
      </tr>
      <tr>
        <th>Date</th>
        <td>글이 작성된 날짜</td>
      </tr>
      <tr>
        <th>Link</th>
        <td>작성된 글의 링크</td>
      </tr>
      <tr>
        <th>Title</th>
        <td>작성된 글의 제목</td>
      </tr>
      <tr>
        <th>Context</th>
        <td>작성된 글 내용의 요약/만들어진 맥락</td>
      </tr>
      <tr>
        <th>Comment</th>
        <td>수집된 댓글</td>
      </tr>
      <tr>
        <th>Hate speech</th>
        <td>혐오 표현 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>Counter speech</th>
        <td>대항 표현 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>Gender</th>
        <td>혐오 대상 성별 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>Disability</th>
        <td>혐오 대상 장애 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>Race/Nationality</th>
        <td>혐오 대상 인종/국가 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>Region (Korea)</th>
        <td>혐오 대상 지역 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>Age</th>
        <td>혐오 대상 연령 여부(0 또는 1 주석)</td>
      </tr>
      <tr>
        <th>Profanity</th>
        <td>비속어 포함 여부</td>
      </tr>
      <tr>
        <th>Ikiyano-style</th>
        <td>이기야노체(일베 말투) 포함 여부</td>
      </tr>
    </tbody>
  </table>

## 인용
 ```
@inproceedings{park-etal-2026-kocoh,
  title = {KOCOH: Korean Context-Dependent Hate Speech Dataset},
  author = {Park, Eunah and Song, Sanghoun},
  booktitle = {Proceedings of the Fifteenth Language Resources and Evaluation Conference (LREC 2026)},
  month = {May},
  year = {2026},
  pages = {4103--4114},
  address = {Palma, Mallorca, Spain},
  publisher = {European Language Resources Association (ELRA)},
  editor = {Piperidis, Stelios and Bel, Núria and van den Heuvel, Henk and Ide, Nancy and Krek, Simon and Toral, Antonio},
  doi = {10.63317/5pnu2jn6awun},
  abstract = {We introduce the KOrean COntext-dependent Hate speech dataset (KOCOH) to evaluate large language models’ ability to detect context-dependent hate speech in Korean. KOCOH consists of 3,000 context-comment pairs collected from Korean online communities (Dcinside, FMkorea) with detailed annotations, including labels for hate speech and hate target groups. We assess the context-dependent hate speech detection capabilities of both humans and 11 state-of-the-art large language models, including GPT-5, Claude Sonnet 4, and Gemini 2.5 Flash. Our results show that humans outperform language models, with GPT-5 achieving the highest performance among the evaluated models. While humans demonstrate balanced recall and specificity, language models generally show significantly higher specificity compared to recall. The performance of both humans and models is affected by factors such as Honam-related vocabulary and sentiment polarity. This study contributes resources to Korean hate speech research and empirically demonstrates the performance gap between humans and language models. Through both quantitative and qualitative analyses, we explore the similarities and differences between humans and language models, offering insights for future developments in language models and AI ethics research. KOCOH is available at https://github.com/eparkatgithub/KOCOH.}
}
 ```

## 라이선스
