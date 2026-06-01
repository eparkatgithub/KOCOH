# KOCOH (KOrean COntext-dependent Hate speech) Dataset
* Paper: [KOCOH: Korean Context-Dependent Hate Speech Dataset](https://doi.org/10.63317/5pnu2jn6awun)
* Authors: [Park Eunah](https://github.com/eparkatgithub), [Song Sanghoun](http://corpus.mireene.com/)
* Contact: dmsdk1993@korea.ac.kr
* [Hugging Face](https://huggingface.co/datasets/E-Park/KOCOH)🤗

This is **Ko**rean **co**ntext-dependent **h**ate speech dataset, KOCOH.<br>
[한국어 설명](https://github.com/eparkatgithub/KOCOH/blob/main/README_ko.md)

## Main concept
* Hate speech
  * Verbal or non-verbal expressions that, based on prejudice or discrimination against socially marginalized or vulnerable groups, denigrate, disparage, or insult such groups or individuals belonging to them, or incite discrimination or violence against them.
* Context-dependent hate speech
  * Hate speech interpreted as hateful through contextual factors rather than explicit content alone
  * In other words, without context, the statement itself may appear neutral or even positive in interpretation
  * Examples
    |Context|Comment|Hate|
    |:---|:---|:---:|
    |여성 고용이 미흡해 정부가 불이익을 준 기업의 이름이 공개되었다.<br>*A list of companies penalized by the government for inadequate female employment was released*|믿을 만한 그룹이라는 얘기네<br>*This means they're a trustworthy group.*|1|
    |직원에게 높은 수준의 복지를 제공한 기업의 이름이 공개되었다.<br>*A list of companies that provide high-level welfare benefits to employees was released.*|믿을 만한 그룹이라는 얘기네<br>*This means they're a trustworthy group.*|0|

## Data Description
* Source
  * [Dcinside Real-time Best Gallery](https://gall.dcinside.com/board/lists/?id=dcbest) (2024/06/02-23)
  * [FMkorea Best Board](https://www.fmkorea.com/best)(2025/01/01-21)
* Size
  |Total|Type 1|Type 2|Type 3|
  |:---:|:---:|:---:|:---:|
  |3,000|764|764|1,472|
* Types and examples
  <table>
    <thead>
      <tr>
        <th></th>
        <th>Context</th>
        <th>Comment</th>
        <th>Hate</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th rowspan="2">Type 1</th>
        <td>Actually written context A</td>
        <td>Actually written comment C</td>
        <td rowspan="2">1</td>
      </tr>
      <tr>
        <td>광주광역시의 맛있는 음식 다섯 가지를 소개했다.<br><i>Introduced five delicious foods from Gwangju Metropolitan City.</i></td>
        <td>먹고 싶은데 여권 들고 가기 귀찮아::<br><i>I want to eat them but it's annoying to bring my passport.</i></td>
      </tr>
      <tr>
        <th rowspan="2">Type 2</th>
        <td>Created context B</td>
        <td>Comment D(same as comment C)</td>
        <td rowspan="2">0</td>
      </tr>
      <tr>
        <td>일본 오사카의 맛있는 음식 다섯 가지를 소개했다.<br><i>Introduced five delicious foods from Osaka, Japan.</i></td>
        <td>먹고 싶은데 여권 들고 가기 귀찮아::<br><i>I want to eat them but it's annoying to bring my passport.</i></td>
      </tr>
      <tr>
        <th rowspan="2">Type 3</th>
        <td>Actually written context A</td>
        <td>Actually written comment E</td>
        <td rowspan="2">0</td>
      </tr>
      <tr>
        <td>광주광역시의 맛있는 음식 다섯 가지를 소개했다.<br><i>Introduced five delicious foods from Gwangju Metropolitan City.</i></td>
        <td>역시 광주다<br><i>That's Gwangju for you.</i></td>
      </tr>
    </tbody>
  </table>
* Columns
  <table>
    <thead>
      <tr>
        <th>Column</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>Index</th>
        <td>Data index</td>
      </tr>
      <tr>
        <th>Set</th>
        <td>Post index</td>
      </tr>
      <tr>
        <th>Type</th>
        <td>Type number (1~3 labeling)</td>
      </tr>
      <tr>
        <th>Date</th>
        <td>The date the post was written</td>
      </tr>
      <tr>
        <th>Link</th>
        <td>The link to the post</td>
      </tr>
      <tr>
        <th>Title</th>
        <td>The title of the post</td>
      </tr>
      <tr>
        <th>Context</th>
        <td>Summary of the post content / Created context</td>
      </tr>
      <tr>
        <th>Comment</th>
        <td>Comments collected from the forum</td>
      </tr>
      <tr>
        <th>Hate speech</th>
        <td>Whether it is hate speech (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>Counter speech</th>
        <td>Whether it is counter speech (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>Gender</th>
        <td>Target: gender (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>Disability</th>
        <td>Target: disability (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>Race/Nationality</th>
        <td>Target: race/nationality (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>Region (Korea)</th>
        <td>Target: region (Korea) (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>Age</th>
        <td>Target: age (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>Profanity</th>
        <td>Including profanity (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>Ikiyano-style</th>
        <td>Including *ikiyano* style (-no) (0 or 1 labeling)</td>
      </tr>
    </tbody>
  </table>

## Citation
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

## License
TBD
