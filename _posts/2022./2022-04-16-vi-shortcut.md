---
layout: post
title: vi(vim) 명령어 정리
date: 2022/04/16/00:00
categories: Posts
---
  
## 이동

명령어 | 동작
:---: | ---
**h, j, k, l** | 방향키 (커서 이동)
**gg** | 첫째줄로 이동
**G** | 마지막줄로 이동
**숫자G** | 입력한 숫자의 라인으로 이동
**0** or **^** | 현재 라인의 맨 처음 문자로 이동
**$** | 현재 라인의 맨 마지막 문자로 이동
**Ctrl+f** | 다음 페이지로 이동
**Ctrl+b** | 이전 페이지로 이동
**Ctrl+d** | 다음 페이지로 반만큼 이동
**Ctrl+u** | 이전 페이지로 반만큼 이동

## 탐색

명령어 | 동작
:---: | ---
**/문자열** | 오른쪽 아래 방향으로 입력한 문자열 검색
**?문자열** | 왼쪽 위 방향으로 입력한 문자열 검색
**n** | 다음 검색 위치로 이동
**N** | 이전 검색 위치로 이동

## 편집

명령어 | 동작
:---: | ---
**yy** | 현재 라인 복사
**숫자yy** | 입력한 숫자만큼의 라인 복사
**dd** | 현재 라인 잘라내기
**숫자dd** | 입력한 숫자만큼의 라인 잘라내기
**p** | 현재 커서의 바로 아래 라인에 붙여넣기
**x** | 현재 커서의 문자 잘라내기
**숫자x** | 현재 커서 뒤로 입력한 숫자만큼의 문자 잘라내기
**v** | 문자 단위의 블럭 지정 모드 전환  
**V** | 라인 단위의 블럭 지정 모드 전환
(블럭 지정 후) **y** | 지정한 블럭 복사
(블럭 지정 후) **x** | 지정한 블럭 잘라내기
**>** | 들여쓰기
**<** | 내어쓰기
**r[문자]** | 현재 커서 위치의 문자를 입력한 문자로 바꿈
**R** | 현재 커서 위치부터 insert 모드 전환

## 입력 모드 전환

명령어 | 동작
:---: | ---
**a** | 현재 커서 위치의 문자 뒤에서 부터 편집 시작
**i** | 현재 커서 위치의 문자 앞에서 부터 편집 시작
**o** | 현재 라인 다음에 새 라인을 추가하며 편집 시작
**O** | 현재 라인 위에 새 라인을 추가하며 편집 시작

## 기타

명령어 | 동작
:---: | ---
**u** | Undo
**:w** | 파일 저장
**:w 파일명** | 입력한 파일명으로 저장
**[ :q ]** | 파일 저장하지 않고 편집기 종료
**:q!** | 파일 저장하지 않고 편집기 강제 종료
**:wq** | 정상적으로 파일 저장 후 편집기 종료
**:set number** or **:set nu** | 편집기 좌측에 라인 번호 표시
**:set nonumber** or **:set nonu** | 편집기 좌측 라인 번호 숨기기
