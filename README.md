# DevLadies Blog

### gitlblog 설치 간단 요약
1.  git repository를 생성
    - repository의 이름은 사용할 블로그 주소(사용자명.github.io)
2.  원하는 jekyll 테마를 clone  
** 로컬주소에서 변경사항을 확인하기 위해서 ruby 및 jekyll 설치 **  
** ruby cmd에서 jekyll install **  
** jekyll build 후 jekyll serve --watch ** 

### 현재 디렉토리 구조
_includes :   각 페이지에 삽입할 수 있는 html  
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

### 로컬의 변경사항을 git에 등록
 git add .  
git commit -m "커밋메세지"  
git push origin master  
  (추후에 branch에서 branch에 올리고 master merge 하는 식으로 합시다)   

