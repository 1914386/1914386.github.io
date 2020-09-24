---
layout: post
title: 블로그 개설 과정
comments: true
categories: [Dev, ㄴgithub]
tags:
- GitHub
- Jekyll
---
<p class="message">
블로그를 잘 활용하기 위해 테마와 커스터마이징 방법을 탐색했습니다.  많은 시행착오 끝에 <strong>Lanyon</strong> 테마를 선택하였으며, 다음의 사이트들을 참고하여 커스터마이징을 할 예정입니다.
</p>
---

### 지킬 설치 및 테마 적용
+ [Lanyon 테마 GitHub](https://github.com/poole/lanyon)
+ [jekyll을 활용하여 git blog 만들어보기](https://hwiyong.tistory.com/275)
+ [Lanyon for Github Pages - Gemfile 생성법](https://www.akashhajari.com/blogs/Lanyon-for-Github-Pages)
+ ['bundle exec jekyll serve' 빌드 진행 중 에러가 발생한 경우](https://swifteyes.blogspot.com/2016/12/jekyll-github.html)

### 커스터마이징 - 태그, 카테고리 적용 완료
+ [devYurim 님의 블로그 - 커스터마이징 전반](https://devyurim.github.io/DE/Github%20Blog)
+ [변경민의 LOWIL - 커스터마이징 전반](https://changemin.github.io/posts/)
+ [hoisharka's blog - 지킬에 카테고리와 태그 적용하기(1)](https://hoisharka.github.io/jekyll/2017/12/03/jekyll-category-001/) - 적용완료!
+ [hoisharka's blog - 지킬에 카테고리와 태그 적용하기(2)](https://hoisharka.github.io/jekyll/2017/12/03/jekyll-category-002/)   
+ [Jekyll 블로그 태그 기능 붙이기](https://hyesun03.github.io/2016/12/05/jekyllTag) - 적용완료!  
+ [coilly blog - 전체 화면에서 사이드바 고정](https://coilly.github.io/)  
+ [coilly님 블로그 GitHub](https://coilly.github.io/)

### 마크다운 문법
+ [마크다운 총정리 All in One](https://steemit.com/kr/@nand/markdown)
+ [TheoryDB - 마크다운(Markdown) 사용법 및 예제](https://theorydb.github.io/envops/2019/05/22/envops-blog-how-to-use-md/) 

### 변경사항 commit 후 push하기
1. $ git add .
2. $ git commit -m "commit message"
3. $ git push origin master

### commit message 수정하기
+ [Git 과거의 특정 커밋 수정하기](https://homoefficio.github.io/2017/04/16/Git-%EA%B3%BC%EA%B1%B0%EC%9D%98-%ED%8A%B9%EC%A0%95-%EC%BB%A4%EB%B0%8B-%EC%88%98%EC%A0%95%ED%95%98%EA%B8%B0/)
+ [GitHub Commit 수정하기](https://coding-groot.tistory.com/30)
+ [Vi 에디터를 이용한 커밋 메시지 작성 방법](https://cau-dosc.github.io/how-to-write-commit-messages-using-vi.html)  
1. `git log`을 입력하여 수정할 커밋을 확인한다.
2. `git rebase --interactive 이전 커밋`을 입력하여 바꾸려는 커밋의 이전 커밋을 target으로 지정한다.
3. `i`를 눌러 작성 모드로 변경한다.
4. `pick` → `edit`으로 수정한다.
5. `Esc`를 누른 후 `:wq!`을 입력하여 저장하고 편집기를 종료한다.
6. `git commit --amend`을 입력하면 편집기가 생성된다. 아까처럼 3번 절차를 실행하여 커밋 메시지를 바꾼다. 5번 절차를 실행하여 저장하고 편집을 종료한다.
7. `git rebase --continue`를 입력하고 'Successfully rebased and updated ...'이 뜬다면 성공
8. `git log`을 다시 입력하여 정상적으로 수정되었는지 확인  

### DISQUS에 가입하여 댓글 기능 추가하기 - 완료
+ [_includes\disqus.html 생성 + 기타 파일 수정](https://skyksit.tistory.com/entry/%EB%94%94%EC%8A%A4%EC%BB%A4%EC%8A%A4-disqus-%EB%A1%9C-%EA%B9%83%ED%97%88%EB%B8%8C%EC%97%90-%EB%8C%93%EA%B8%80-%EA%B8%B0%EB%8A%A5-%EB%8B%AC%EA%B8%B0-jekyll-github-pages)
+ [고급 설정 - 댓글창 꾸미기](https://jamesu.dev/posts/2020/01/03/adding-disqus-comment-service-to-jekyll/)
+ [lanyon 테마에서의 댓글 적용법 (실제로 참고는 하지 않음)](http://anandmanisankar.com/posts/set-up-blog-jekyll-github-pages-2/)  

### 고급 설정
`codinfox-lanyon` 테마에서 최대한 참고하여 태그, 검색기능 등 고급 기능 추가하기  
+ [원작자 GitHub](https://github.com/codinfox/codinfox-lanyon)
+ [원작자 블로그](http://codinfox.github.io/blog/categories/)
+ [Jaden Develop Log](https://callmejaden.github.io/)
+ [Log for everything - Day 1176](https://minyoungjung.github.io/blog/categories/#%EB%B8%94%EB%A1%9C%EA%B7%B8)
+ [ANAND MANI SANKAR](http://anandmanisankar.com/)  