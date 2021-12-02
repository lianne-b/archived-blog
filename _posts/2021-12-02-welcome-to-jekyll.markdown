---
layout: post
title: "좌충우돌 블로그 개설기 "
date: 2021-12-02 15:04:21 +0800
categories: jekyll update
---

배경 지식 없이 깃헙 공식 문서 따라서 블로그를 만들어 보려다가 이거.. 내 이해력으론 너무 오래 걸릴 것 같길래

치트키인 한국인 블로거 분의 도움을 받아... 어찌저찌 개설에 성공했다. [참고 블로그](https://zeddios.tistory.com/1222)

근데 말이 치트키지 ㅜㅠ 진짜 너무 아는 게 없어서 이 부분에서 막히고 저 부분에서 막히느라 배포에만 반나절을 쏟았다. 전부 모르는 용어와 개념들이고.. 말 없이 빨간 줄을 토해내는 터미널을 무기력하게 바라볼 뿐.

나는 바보.. 하지만 괜찮다 ...언젠간 극복하겠지^^ㅋ

일단 처음부터 Ruby가 문제였다.

참고로 난 Ruby라는 언어를 이름만 들어봤지 뭐, 지금 자바스크립트도 겨우 겉핥기 식으로 하고 있는데.

제대로 설치하는 것부터가 순탄치 않았다. 공식 문서 등등에서 하라는대로 다 따라하긴 했는데도,

에러가 말그대로 줄줄줄줄 났다; (맘같아선 전부 기록해놓고 싶었는데 너무 많이 떠서 걍 포기)

찾아보니 Ruby의 버전 매니저인 RVM 이라는 걸 받으래서 그거 설치하고..

또 막 터미널이 뭐라뭐라... 어쩌구 하다가 gem이 다운이 안된댄다. gem은 Ruby의 패키지 매니저인데

왜.. 대체 왜를 울부짖다가 이 분의 블로그에 도달했다. 마침 내가 마주친 거랑 동일한 에러여서 완전 럭키.

[Mac에서 Gem::FilePermissionError 에러 발생시 해결 방법](https://jojoldu.tistory.com/288) (넘 멋지신 분 흑흑 저 유튜브도 구독하고 있어요)

알려주신대로 rbenv라는 Ruby 버전 매니저를 설치하고, rbenv을 통해 사용되고 있는 Ruby의 버전을 확인해보니 System Ruby.

요 System Ruby를 사용하고 있어서 권한이 없다고 gem이 설치가 안된다고 에러가 뜬건데,

System Ruby는 또 뭐야.. 싶었다 당연히. 그게 뭡니까..

아무튼 뭔진 몰라도 최신 버전의 Ruby를 다운받고 글로벌 버전 시스템을 최신 버전(현재 기준 3.0.3)으로 바꿔주니 드디어. 에러가 해결이 됐다. 오예..

하지만 이 부분은 나중에 다시 들여다 봐야 한다. 현재로써 어렴풋이 이해한 바로는 System Ruby는 기존 컴퓨터에 내장된 버전이고..? 이보다는 외부적으로 설치된 버전의 Ruby가 권장된다는 점? 구글에 물어봤을 땐 다 System Ruby 쓰지말래.

조만간 이 밑의 링크를 자세히 뜯어보도록.. 오늘은 이미 시간을 너무 많이 잡아먹어서 딴 거 해야되니까!

[https://www.freecodecamp.org/news/do-not-use-mac-system-ruby-do-this-instead/](https://www.freecodecamp.org/news/do-not-use-mac-system-ruby-do-this-instead/)

그렇게 우여곡절 끝에 모든 설치를 마치고 로컬 서버를 받고 jekyll을 성공적으로 띄웠다.

그리고 깃헙에 푸쉬해서 배포 완료! 하핳

정말 별 거 아니였지만 다사다난했던 여정... 왕초보는 이렇게 성장하는 거죠.

내 자신 화이팅!!!

### 다시 들여봐야 하는 부분

- Ruby의 전반적인 개념과 작동원리
- System Ruby의 단점
- Ruby 버전 매니저 종류, 차이점
- 로컬 PATH

### 내일의 목표:

1. 블로그 템플릿 정하기
2. 블로그에 깃에 관련된 내용 정리해서 포스팅 하기
3. 깃 명령어 숙지하기

{% highlight ruby %}
def print_hi(name)
puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]: https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
