---
layout: post
title:  "CSS Attribute Selector"
date:   2018-10-30
categories: css selector attrigute
---

`div[title]` - title 속성을 가진 div

`div [title]` - div 하위에 있는 [title] 속성을 가진 요소

`div[title="dna"]` - dna 타이틀을 가진 div

`div[title~="dna"]` - 여러 공백으로 구분된 리스트 중에 dna를 타이틀로 가진 div

`[title$="dna"]` - 타이틀의 뒤에 dna라는 단어를 포함하고 있는 모든 요소

`[title^="dna"]` - 타이틀의 앞에 dna라는 단어를 포함하고 있는 모든 요소

`[title|="gene"]` - "genealogy"는 선택하지 않고 "gene"나 "gene-data"를 선택하고 싶을 때. 하이픈은 포함된다.

`[title*="dna"]` - dna라는 단어를 포함하고 있는 모든 타이틀

`a[title][class$="genes"]` - 클래스 이름이 "genes"로 끝나는 클래스를 가지고 있고, 타이틀 속성을 가지고 있는 a 태그

`[title*="DNA" i]` - 대소문자 상관없이 dna라는 타이틀을 가진 요소. i는 크롬 사파리 파폭 및 모바일 브라우저에서만 인식



#### 링크별로 다른 스타일 지정

```css
a[href^="http"]{
   color: bisque;
}
a:not([href^="http"]) {
  color: darksalmon;
}

a[href^="http://"]:after {
   content: url(unlock-icon.svg);
}
a[href^="https://"]:after {
   content: url(lock-icon.svg);
}
```



#### 첨부파일이나 다운로드 받아야 할 파일의 링크에 적용.

download 속성은 다운로드 받을 수 있게 해줌

```css
a[download]:after {
   content: url(download-arrow.svg);
}
```



#### 파일의 확장자 별로 다른 아이콘 지정

```css
a[href$="pdf"]:after {
   content: url(pdf-icon.svg);
}
a[href$="docx"]:after {
   content: url(docx-icon.svg);
}
a[href$="odf"]:after {
   content: url(open-office-icon.svg);
}
```



#### 다운로드 받을 수 있는 pdf 파일에 지정된 아이콘

```css
a[download][href$="pdf"]:after {
   content: url(pdf-icon.svg);
}
```



