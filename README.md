# DevLadies Blog
>git pages 기능을 활용하여 개설한 공동 블로그

동기들과 함께 사용하기 위해 블로그를 개설하였으며 앞으로 공부한 내용과 프로젝트를 올릴 예정입니다.

## gitlblog 개설 방법
1.  git Repository를 생성
    - repository의 이름은 사용할 블로그 주소로 작성(사용자명.github.io)
2.  원하는 jekyll 테마를 clone
3. **로컬주소에서 변경사항을 확인하기 위해서 ruby 및 jekyll 설치**  
**ruby cmd에서 jekyll install**
```ruby
jekyll install #이미 Gemfile.lock이 있을 경우 jekyll update를 통해 필요한 파일을 설치
jekyll build
jekyll serve --watch
```

## 현재 디렉토리 구조
현재 jekyll theme를 clone해오며 생성된 디렉토리에 대한 설명입니다.  
 _includes :   각 페이지에 컴포넌트로서 삽입할 수 있는 html  
  _layout :  각 페이지의 레이아웃 html  
  _posts : 작성한 글(yyyy-mm-dd-postname-number.md 형식 지켜야 글 작성가능)   
  _sass : css 파일  
  _site : 로컬에서 서버를 돌릴 시 생성되는 파일들 (신경 x)    
  assets : css 및 img 파일 / main.scss의 @import type-theme.scss.를 통해 _sass폴더와 연결  
  category : 카테고리  
  _config.yml : 설정 파일  
  404.md : 페이지 없을 시 나타나는 에러페이지  
  about.md: about 페이지  
  .gitignore : git add 시 제외할 파일등록  
  Gemfile/Gemfile.lock : ruby를 사용할 때 쓰는 파일인 것 같음  

## local repository의 작업사항을 원격 repository에 적용
```bash
git clone 원격레포지토리주소 #이미 레포지토리가 있을 경우 처음 한번만 적용

git pull #원격 저장소 내용을 local에 적용 (작업한거 다 날아갈 수 있으니 주의)

git add . 
git commit -m "커밋메세지"  
git push origin master  
#추후에 branch에서 branch에 올리고 master merge 하는 식으로 합시다
```