## 스마트 가계부 작성 및 구매기록 분석 서비스 



### :money_with_wings: 서비스 소개
---
모바일영수증을 읽어 가계부를 작성하고, 구매주기를 분석해 추천하는 웹 서비스입니다. 사용자가 모바일 영수증을 업로드하면, 자동으로 지출 내역을 분류하고 소비 현황과 패턴을 분석해 제공합니다.


_서울과학기술대학교 24-1 디지털응용및전환 팀프로젝트_
![모바일영수증이미지](https://github.com/user-attachments/assets/613616c7-0375-44ed-8320-cce8c668179c)



### :wrench: 개발환경
---
- **프로그래밍 언어**: Python
- **프레임워크**: Flask
- **OCR API**: Clova OCR API



### :pushpin: 주요기능
---
#### 1. 영수증 스캔 및 데이터 추출
사용자는 마트에서 받은 모바일 영수증을 캡처해서 업로드할 수 있습니다. 
Clova OCR API를 이용해 영수증 텍스트를 추출하며, 
영수증의 패턴을 파악해 날짜, 품명, 개수, 단가, 금액으로 나눠서 저장합니다.

#### 2. 지출 내역 자동분류
이마트몰을 크롤링하여 카테고리별 품목 데이터를 엑셀 파일로 저장해두어 일종의 데이터베이스를 만들었습니다.
영수증에서 읽은 품명을 데이터베이스에서 찾아 해당 카테고리에 속하는지 파악하고, 품목별 카테고리 정보 저장합니다.

#### 3. 카테고리별 소비현황 시각화
최근 3개월 간의 소비 내역을 카테고리별로 합산하여 파이차트로 비율을 시각화합니다. 
사용자가 소비 현황을 직관적으로 확인할 수 있습니다.

#### 4. 많이 구매한 상위 품목 분석
최근 3개월 간의 품목별 구매 개수를 합산하여 많이 구매한 상품 리스트를 제공합니다. 
사용자는 불필요한 상품을 반복 구매하는지 확인하고, 필요한 상품을 잊지 않고 다시 구매할 수 있습니다.

#### 5. 엑셀로 가계부 파일 제공
추출된 데이터를 엑셀 파일로 저장합니다. 
사용자는 가계부 보기 버튼을 눌러 파일을 다운로드할 수 있습니다. 
가계부 파일명을 바꾸지 않는 한, 동일한 가계부를 읽으면서 새로운 영수증 정보를 누적해서 저장할 수 있습니다.

#### 6. 구매 주기 분석 및 추천
각 카테고리의 평균 구매 주기를 계산하고, 구매주기가 비슷한 카테고리끼리 그룹화합니다.
그룹별 마지막 구매 일자에 평균 주기를 더해 예상되는 다음 구매 일자를 도출합니다. 
사용자는 필요한 시점에 상품을 구매할 수 있도록 구매일자를 추천받을 수 있습니다.



### :tv: 화면
---
![화면](https://github.com/user-attachments/assets/2bdf5938-2cdb-477e-9271-d5b3daef4424)
