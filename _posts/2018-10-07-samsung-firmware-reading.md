---
layout: post
title:  "삼성 갤럭시 펌웨어 버전 확인"
author: SiRyuA
categories: Samsung
tags:
- Android
- Samsung
- Firmware
---

## 펌웨어 버전 확인 방법
1. 설정 > 휴대전화 정보 > 소프트웨어 정보
2. 빌드번호가 펌웨어 명칭


## 펌웨어 버전 읽는 법
~~~~
G955NKSU3CRI3
=> 11111-2-3-44-5-6-7-8
=> G955N-K-S-U3-C-R-I-3 * 참고예시
~~~~
* [1] 모델명
  * 통신사에 따라서 마지막 자리가 S/K/L 로 표기
  * Galaxy S8 이후 3사 통합 모델 정책에 따라 N 으로 표기
* [2] 지역구분
  * K = Korea
* [3] 통신사구분
  * S = SKT / K = KT / L = U+
* [4] 부트로더 버전
  * U1 / U2 / U3 형태로 부트로더 버전 표기
  * U2 -> U3 펌웨어로 업데이트는 가능
  * U3 -> U1 펌웨어로 다운그레이드는 불가능
* [5] 메이저 업데이트 횟수
  * 최초 펌웨어는 A
  * 메이저 업데이트에 따라서 ABCDE 순서대로 변경
  * 테스트 또는 베타 펌웨어는 Z 로 표기
* [6] 빌드한 년도
  * L = 2012 / M = 2013 / N = 2014 / O = 2015
  * P = 2016 / Q = 2017 / R = 2018 / S = 2019
  * T = 2020 / U = 2021 / V = 2022 / W = 2023
  * X = 2024 / Y = 2025 / Z = 2026
* [7] 빌드한 월
  * A = 1월 / B = 2월 / C = 3월 / D = 4월
  * E = 5월 / F = 6월 / G = 7월 / H = 8월
  * I = 9월 / J = 10월 / K = 11월 / L = 12월
* [8] 빌드한 횟수
  * 16진수 체계 이용
  * 1/2/3/4/5/6/7/8/9/A/B/C/D/E/F


## CSC 구분을 통해서 통신사 단말기 확인 방법
1. 설정 > 휴대전화 정보 > 소프트웨어 정보
2. 서비스 공급자 SW 버전을 통해서 확인가능
~~~~
SAOMC_SM-955N_OKR_SKC_OO_0018
~~~~
* 요기서 SKC 있는 영역의 문자에 따라 구별
  * SKC = SKT
  * KTC = KT
  * LUC = U+
  * KOO = 자급제
