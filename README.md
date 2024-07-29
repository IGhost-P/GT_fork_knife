# Fork and Knife Classifier with TTS

이 프로젝트는 Google Teachable Machine을 사용하여 포크와 나이프 이미지를 학습시킨 후, 웹캠을 통해 실시간으로 이미지를 분석하고 텍스트 음성 변환(TTS) 기능을 추가한 웹 애플리케이션입니다. 이 프로젝트는 Netlify를 통해 배포되었습니다.

## 프로젝트 구조

```
📦google-teachable-machine
 ┣ 📂fork_knife_GT_model
 ┃ ┣ 📜metadata.json
 ┃ ┣ 📜model.json
 ┃ ┗ 📜weights.bin
 ┗ 📂src
 ┃ ┗ 📂assets
 ┃ ┃ ┗ 📂images
 ┃ ┃ ┃ ┣ 📂fork
 ┃ ┃ ┃ ┃ ┣ 📜fork_1.png
 ┃ ┃ ┃ ┃ ┣ 📜fork_2.png
 ┃ ┃ ┃ ┃ ┣ 📜fork_3.png
 ┃ ┃ ┃ ┃ ┣ 📜fork_4.png
 ┃ ┃ ┃ ┃ ┗ 📜fork_5.png
 ┃ ┃ ┃ ┣ 📂knife
 ┃ ┃ ┃ ┃ ┣ 📜knife_1.png
 ┃ ┃ ┃ ┃ ┣ 📜knife_2.png
 ┃ ┃ ┃ ┃ ┣ 📜knife_3.png
 ┃ ┃ ┃ ┃ ┣ 📜knife_4.png
 ┃ ┃ ┃ ┃ ┗ 📜knife_5.png
 ┃ ┃ ┃ ┗ 📜index.html
 ┃ ┃ ┗ 📜README.md
```

## 사용된 기술

- HTML
- CSS
- JavaScript
- TensorFlow.js
- Teachable Machine
- Netlify

## 설정 및 실행

### 1. 추가 학습

추가 학습을 위해 새로운 이미지를 Teachable Machine에 업로드하고 모델을 다시 학습시킬 수 있습니다. 학습된 모델 파일을 업데이트하려면 다음 단계를 따르십시오:

1. [Google Teachable Machine](https://teachablemachine.withgoogle.com/)에 접속하여 새로운 프로젝트를 생성하거나 기존 프로젝트를 엽니다.
2. 새로운 포크와 나이프 이미지를 업로드하고 모델을 다시 학습시킵니다.
3. 모델 학습이 완료되면, "Export Model"을 클릭하여 모델 파일을 다운로드합니다.
4. 다운로드한 파일(예: `model.json`, `metadata.json`, `weights.bin`)을 `fork_knife_GT_model` 폴더에 덮어씁니다.
5. 새로운 모델이 적용된 웹 애플리케이션을 실행합니다.

### 2. Netlify 배포

Netlify를 통해 웹 애플리케이션을 배포하려면 다음 단계를 따르십시오:

1. [Netlify](https://www.netlify.com/)에 접속하여 계정을 생성하거나 로그인합니다.
2. "New site from Git"을 클릭하여 GitHub, GitLab 또는 Bitbucket 리포지토리와 연결합니다.
3. 리포지토리를 선택하고 배포 설정을 완료합니다.
4. 배포가 완료되면 Netlify가 제공하는 URL을 통해 웹 애플리케이션에 접근할 수 있습니다.

## 프로젝트 실행

1. 로컬에서 프로젝트를 실행하려면 로컬 서버를 설정해야 합니다. `http-server`와 같은 도구를 사용할 수 있습니다:

   ```sh
   npm install -g http-server
   http-server ./google-teachable-machine/src
   ```

2. 브라우저에서 `http://localhost:8080`을 열어 웹 애플리케이션에 접근합니다.

---
