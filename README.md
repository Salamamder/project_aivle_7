<div style="text-align: center;">
  <h1>🚀 청중의 집중도 분석 및 피드백 웹 서비스 🚀</h1>
</div>


1. 청중의 집중도를 실시간으로 발표자에게 알려준다.
2. 발표가 마무리된 후 발표자에게 청중의 집중도가 시간대별로 어떻게 변화하는지 알려준다.
3. 강의 내용과 청중의 집중도를 기반으로 발표자에게 어떠한 부분이 부족했는지 혹은 좋았는지 피드백을 준다.



### 개요
---
+ 프로젝트 이름: 청중의 소리를 부탁해
+ 프로젝트 지속기간:
+ 개발 언어 및 프레임워크: Python, Django, HTML, CSS, JS, Bootstrap5, MySQL
+ 멤버: 권승회, 장은성, 조수인, 이혜원, 한수민, 박지수

### 서비스 설명
---
| 로그인화면 | 강의설정 |
|--------|--------|
| ![발표자료_13](https://github.com/user-attachments/assets/71c52b3c-feb0-4e50-8d2e-6a328518fc77) | ![발표자료_15](https://github.com/user-attachments/assets/11998a92-6392-4af3-93df-62550c2ef954) |
| 실시간집중도분석 | 강의분석  |
|  |  |
| ![발표자료_16](https://github.com/user-attachments/assets/6765918b-092c-49a3-b48e-fe5f4e058326)  | ![발표자료_18](https://github.com/user-attachments/assets/007c318e-146e-422f-9e5f-307efec0eca9)  |


카메라와 연동하여 청중들의 표정을 실시간으로 분석하여 집중도를 분석한다. 

분석된 집중도는 이모지를 활용하여 발표자에게 직관적으로 표시되도록 한다.

추후 끝난 강의는 발표자가 보관이 가능하며 STT를 통해 변환된 강의내용과 시간별 집중도 데이터를 통해 발표자의 강의에 대한 내용을 피드백해준다. 해당 분석에는 프롬프트 엔지니어링이 된 ChatGPT API가 사용되었다.

---
### 집중도분석 AI 설명

| 학습데이터 | 모델 |
|--------|--------|
| ![발표자료_19](https://github.com/user-attachments/assets/5b46bda4-16f7-4cab-84c5-87abcde3795d) | ![발표자료_32](https://github.com/user-attachments/assets/a3baf5a1-a459-457c-9510-1588797ee30f) |

데이터: DAISEE

모델: Self-CNN 2 (CNN모델 자체 변형해서 사용)

ResNet50, InceptionV3 보다 약 8% 더 향상된 성능을 보여주는 Self-CNN 2

해당 Self-CNN2 모델을 파이프라인에 연결하여 실시간으로 전송받는 데이터를 분석한다. 

청중들의 집중도를 총 3가지 클래스인 좋음, 보통, 나쁨으로 구분하며 하나의 카메라로 여러사람의 집중도를 분석할 수 있다.


