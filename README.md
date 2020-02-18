My Portfolio
=========================

Powered by Jekyll

# 지킬로 돌아가는 사이트
# 기본 사용 방법

## Homepage layout
1. `moi-sungah.github.io/_layouts/default.html` 수정
2. `<body id="page-top" class="index">` 밑에 있는 항목 순서수정/추가/삭제

## Subpage layout
1. `moi-sungah.github.io/_includes/`하위 html파일들을 수정

## 포트폴리오 업데이트 방법
1. `moi-sungah.github.io/img/portfolio/`에 사진 업로드
2. `moi-sungah.github.io/_posts/` 하위에 `<날짜>-<제목>.md`파일생성
3. 생성된 파일에 하단항목 입력 후 commit

'''
---
layout: default
modal-id: 6 # 적합한 modal번호 입력. 중복되면 안됨
date: 2020-02-18 # 작성한 날짜 입력
img: IMG_0114.jpg #
project-date: Februrary 2020 
category: Pokemon #Landing페이지에서 보일 이름
description: This is first upload # 클릭후 보이는 설명
---
'''

4. `moi-sungah.github.io/_includes/portfolio_grid.html`수정
5. 파일에 하단항목을 적절한 위치에 입력후 commit
'''
<div class="col-md-4 col-sm-6 portfolio-item">
    <a href="#portfolioModal6" class="portfolio-link" data-toggle="modal">
        <div class="portfolio-hover">
            <div class="portfolio-hover-content">
                <i class="fa fa-plus fa-3x"></i>
            </div>
        </div>
        <img src="img/portfolio/IMG_0114.jpg" class="img-responsive" alt="">
    </a>
    <div class="portfolio-caption">
        <h4>Pokemon</h4>
        <p class="text-muted">Pokemon / by iPad</p>
    </div>
</div>
'''
- `<a href=`에 modal번호 수정
- `"img/portfolio/IMG_0114.jpg`에 img이름 수정
- `<h4>Pokemon</h4>`에 Landing page에서 보여질 제목 수정
- `<p class="text-muted">Pokemon / by iPad</p>`에 클릭 후 보여질 정보 수정

