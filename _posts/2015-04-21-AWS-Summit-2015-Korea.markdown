---
title:  "AWS Summit 2015 Korea"
---
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>GIT</title>
    <link rel="stylesheet" href="/css/reveal.css">
    <link rel="stylesheet" href="/css/theme/simple.css" id="theme">
    <!--<link rel="stylesheet" href="/css/custome/2015-04-10.css">-->
    <!--[i?f lt IE 9]>
    <script src="lib/js/html5shiv.js"></script>
    <![endif]-->
</head>
<body>
<div class="reveal">
    <div class="slides">
        <section>
            <h1>GIT 명령어</h1>
        </section>
        <section>
            <h1>KBJ GIT 기초↓ </h1>
            <h3><a href="https://docs.google.com/presentation/d/1EGRKXnbJEiWz-1-xFPGN6kV-OYP8QVSW5gYwFRCRaTQ/edit?usp=sharing" target="_blank">link</a></h3>
        </section>
        <section>
            <ol>
                <li>bisect</li>
                <li>diff</li>
                <li>grep</li>
                <li>rebase</li>
                <li>stash</li>
                <li>fetch</li>
                <li>tag</li>
            </ol>
        </section>
        <section>
            <section>
                <h1>bisect</h1>
            </section>
            <section>
                <h3>커밋 히스토리를 이진 탐색으로 탐색</h3>

                <div style="text-align: left;">
                    <ul>
                        <li style="list-style-type: none;">1. 탐색 시작하기</li>
                        <li><strong>git bisect start</strong> : 탐색 시작</li>
                        <br/>
                        <li style="list-style-type: none;">2. 탐색 범위 지정하기</li>
                        <li><strong>git bisect good [커밋]</strong> : 문제가 발생하지 않은 커밋 지정</li>
                        <li><strong>git bisect bad [커밋]</strong> : 문제가 발생하는 커밋 지정</li>
                        <li style="list-style-type: none; color: gray;">
                            <small>-> git이 의심되는 커밋을 한개씩 Checkout해서 보여준다</small>
                        </li>
                        <br/>
                        <li style="list-style-type: none;">2. 탐색 검증하기</li>
                        <li><strong>git bisect good</strong> : 현재 git이 가리키는 커밋이 정상</li>
                        <li><strong>git bisect bad</strong> : 현재 git이 가리키는 커밋이 오류</li>
                        <li><strong>git bisect reset</strong> : 탐색을 시작하기 전으로 HEAD를 돌려놓기</li>
                    </ul>
                </div>

            </section>
        </section>

        <section>
            <section>
                <h1>diff</h1>
            </section>
            <section>
                <h3>파일의 변동사항 확인</h3>
                <ul>
                    <li><strong>git diff</strong> : Working directory vs Staging Area</li>
                    <br/>
                    <li><strong>git diff --staged</strong> : Staging Area vs Repository</li>
                </ul>
            </section>
        </section>

        <section>
            <section>
                <h1>grep</h1>
            </section>
            <section>
                <h3><strong>git grep [검색어]</strong></h3>
                <br/>

                <p> 내용에 [검색어]가 있는 파일을 찾아 보여줍니다. </p>
            </section>
            <section>
                <h3><strong>git grep [옵션][검색어][브렌치명]</strong></h3>
                <br/>

                <p>
                <ul>
                    <li> 옵션
                        <ul>
                            <li> -l : list 형태로 출력(이름만)</li>
                            <li> -c : 해당 문서에서 검색어가 사용된 횟수 출력</li>
                            <li> -n : 해당 문서에서 검색어가 위치한 라인 넘버를 출력</li>
                        </ul>
                    </li>
                    <br/>
                    <li><span style="color:blue">검색어</span>뿐만 아니라 <span style="color:blue">정규식</span>도 가능</li>
                    <li>브렌치명을 적어 검색 범위 지정 가능</li>
                </ul>
                </p>
            </section>
            <section>
                <h3><strong>git log --grep [검색어]</strong></h3>

                <p>로그에서 [검색어]가 있는 커밋 조회</p>
                <br/>

                <h3><strong>git log -G[검색어]</strong></h3>

                <p>파일내의 [검색어]가 있는 커밋 조회</p>
            </section>
        </section>

        <section>
            <section>
                <h1>rebase</h1>
            </section>
            <section>
                <h4>커밋 로그를 재구성해 간결하게 바꿔줌.</h4>
                <img src="/images/2015-04-17/rebase-step-1.gif" style="border: none;">
            </section>
            <section data-transition="fade">
                <h4>커밋 로그를 재구성해 간결하게 바꿔줌.</h4>
                <img src="/images/2015-04-17/rebase-step-2.gif" style="border: none;">
            </section>
            <section data-transition="fade">
                <h4>커밋 로그를 재구성해 간결하게 바꿔줌.</h4>
                <img src="/images/2015-04-17/rebase-step-3.gif" style="border: none;">
            </section>
            <section>
                <ol>
                    <li>두 브렌치가 나뉘기 전의 공통 커밋으로 이동</li>
                    <li>그 커밋으로부터 현재 checkout한 커밋까지 따로 저장</li>
                    <li>rebase할 브렌치(현재 checkout한)가 기준 브렌치가 가리키는 커밋을 가리킴</li>
                    <li>이전에 임시로 저장해 놓았던 변경사항을 차례로 적용</li>
                </ol>
            </section>
            <section>
                <h3>merge와의 차이점</h3>
                <ul>
                   <li>rebase : 브렌치의 변경사항을 순서대로 다른 브랜치에 적용하면서 합침</li>
                   <li>merge : 두 브랜치의 최종결과만을 가지고 합침</li>
                </ul>
            </section>
            <section>
                <ol>
                    <li>rebase 할 branch 를 checkout 한다. <br/>
                        --> $ git checkout slave
                    </li>
                    <br/>
                    <li>기준이 되는 branch에 rebase 한다. <br/>
                        --> $ git rebase master
                    </li>
                    <br/>
                    <li>기준 branch 를 fast-forward한다. <br/>
                        --> $ git checkout master <br/>
                        --> $ git merge slave
                    </li>
                </ol>
            </section>
            <section>
                <h4 style="color: red;">주의사항</h4>

                <p>커밋들을 재구성하기 때문에 다수의 작업에서 피해야 한다</p>
                <img src="/images/2015-04-17/1.png" style="border: none;">
            </section>
            <section data-transition="fade">
                <h4 style="color: red;">주의사항</h4>

                <p>커밋들을 재구성하기 때문에 다수의 작업에서 피해야 한다</p>
                <img src="/images/2015-04-17/2.png" style="border: none;">
            </section>
            <section data-transition="fade">
                <h4 style="color: red;">주의사항</h4>

                <p>커밋들을 재구성하기 때문에 다수의 작업에서 피해야 한다</p>
                <img src="/images/2015-04-17/3.png" style="border: none;">
            </section>
            <section data-transition="fade">
                <h4 style="color: red;">주의사항</h4>

                <p>커밋들을 재구성하기 때문에 다수의 작업에서 피해야 한다</p>
                <img src="/images/2015-04-17/4.png" style="border: none;">
            </section>
            <section>
                <ol>
                    <li>rebase를 하려면 push 전에 하자!</li>
                    <li>push를 한 경우라면 rebase는 피하자!</li>
                </ol>
            </section>
            <section>
                <h4>같은 브렌치의 커밋 간결화</h4>
                <p>git reabse -i HEAD~n</p>
            </section>
        </section>

        <section>
            <section>
                <h1>reset</h1>
            </section>
            <section>
                <p>수정하기 이전을 되돌림</p>
                <ul>
                    <li style="list-style-type: none;">1. index 취소</li>
                    <li>git reset -- [파일명] : 해당 파일을 unstaged</li>
                    <li>git reset HEAD [파일명] : 위와 동일</li>
                    <br/>
                    <li style="list-style-type: none;">2. commit 취소</li>
                    <li>git reset HEAD^ : 최종 커밋 취소</li>
                    <li>git reset HEAD~2 : 마지막 2개의 커밋 취소</li>
                    <li>git reset --hard ORIG_HEAD : 머지 커밋 취소</li>
                </ul>
            </section>
        </section>

        <section>
            <section>
                <h1>stash</h1>
            </section>
            <section>
                <h4>워킹 디렉토리에 unstaged 파일들을 백업하고,<br/>워킹 디렉토리를 깨끗한 상태로 만든다.</h4>
                <br/>
                <h5>현재 작업을 하던 도중 다른 작업을 해야할때<br/>지금 작업을 임시로 저장해서 작업한다</h5>
            </section>
            <section>
                <p>git stash [명령어]: 현재 작업을 임시 저장</p>

                <p>[명령어]</p>
                <ul>
                    <li>[list] : 임시저장된 작업들의 리스트 출력</li>
                    <li>[pop] : 임시저장한 작업 적용</li>
                    <li>[apply] : 임시저장한 작업 적용(list에서 삭제x)</li>
                    <li>[drop] : 최근 임시저장된 작업 삭제</li>
                    <li>[clear] : list를 비운기</li>
                </ul>
            </section>

        </section>

        <section>
            <section>
                <h1>fetch</h1>
            </section>
            <section>
                <h3>원격저장소에서 변경사항을 가져옴.</h3>
                <ul>
                    <li>git fetch [저장소이름]</li>
                    <li style="list-style-type: none; color:gray">
                        <small>--> fetch는 로컬 저장소에 미반영</small>
                    </li>
                    <br/>
                    <li>pull : fetch + merge</li>
                </ul>
            </section>
        </section>

        <section>
            <section>
                <h1>tag</h1>
            </section>
            <section>
                <h4>브렌치의 현재 시점에 태그명을 붙힙니다.</h4>
                <ul>
                    <li>git tag : 지정한 태그 목록 보기</li>
                    <li>git tag -a [태그명] -m [메시지]: 태그 지정하기</li>
                    <li>git tag -d [태그명] : 태그 삭제</li>
                    <li>git show [태그명] : 명시한 태그의 내용보기</li>
                    <li>git push origin --tags : 태그랑 함께 Push하기</li>
                </ul>
            </section>
        </section>

        <section style="text-align: left;">
            <h1>THE END</h1>
        </section>

    </div>
</div>
<script src="/js/jquery-1.11.1.min.js"></script>
<script src="/lib/js/head.min.js"></script>
<script src="/js/reveal.js"></script>
<script>
    Reveal.initialize({
        controls: true,
        progress: true,
        slideNumber: true,
        fragments: true,
        top: 0
    });
</script>
</body>

</html>
