# Confirmed Case Counter
신종 코로나 바이러스의 확진자 정보 업데이트가 질본(KCDC)의 언론 공개로 공유되고 있어, WHO나 일부 사이트만을 이용하여 국내 확진자의 수를 정확히 파악하는 것이 어려움.

[코로나맵](http://livecorona.co.kr/) 사이트에 빠르게 확진자 수를 반영하기 위해, KCDC와 여러 사이트에서 확진자 수를 크롤링하여 정확한 확진자 수를 반영.

KCDC에서의 크롤링이 실패해도, worldmeter와 나무위키의 확진자 데이터를 가져와 반영 가능함.

## 함수 설명
### doTry()
크롤링 시도, 실패시 3회 재시도
### main()
전체 사이트 크롤링 시도, doTry로 각 사이트에 크롤링을 시도함.

KCDC, 나무위키, worldMeter 순으로 정보를 업데이트 하여 딕셔너리에 저장.

## Update note
- 2020.02.08
    - 이제 크롤러가 KCDC, 나무위키, worldMeter 순으로 정보를 강화합니다.
    - 이제 확진자 뿐만 아니라 완치자와 사망자도 크롤링합니다.