## java-lotto-precourse

### 기능 요구 사항

**간단한 로또 발매기를 구현한다.**

* 로또 번호의 숫자 범위는 1~45까지이다.

* 1개의 로또를 발행할 때 중복되지 않는 6개의 숫자를 뽑는다.

* 당첨 번호 추첨 시 중복되지 않는 숫자 6개와 보너스 번호 1개를 뽑는다.

* 당첨은 1등부터 5등까지 있다. 당첨 기준과 금액은 아래와 같다.

    * 1등: 6개 번호 일치 / 2,000,000,000원

    * 2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원

    * 3등: 5개 번호 일치 / 1,500,000원

    * 4등: 4개 번호 일치 / 50,000원

    * 5등: 3개 번호 일치 / 5,000원

* 로또 구입 금액을 입력하면 구입 금액에 해당하는 만큼 로또를 발행해야 한다.

* 로또 1장의 가격은 1,000원이다.

* 당첨 번호와 보너스 번호를 입력받는다.

* 사용자가 구매한 로또 번호와 당첨 번호를 비교하여 당첨 내역 및 수익률을 출력하고 로또 게임을 종료한다.

* 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시키고, "[ERROR]"로 시작하는 에러 메시지를 출력 후 그 부분부터 입력을 다시 받는다. Exception이 아닌 IllegalArgumentException, IllegalStateException 등과 같은 명확한 유형을 처리한다.

### 구현 기능 - 서비스 객체
- [x] 수익률을 계산한다. (ProfitCalculator)
- [x] 랜덤한 숫자를 6개 생성한다. (MakingRandomNumbers)
- [x] 결과를 출력 한다. (LottoResultPrinter)
- [x] 입력을 받는다. (ConsoleReader)

### 구현 기능 - 도메인 객체
- [x] 등수 별 로또를 관리한다. (추상클래스 PrizeLotto)
    - [x] 1등 로또의 정보를 관리한다. (FirstPrizeLotto)
    - [x] 2등 로또의 정보를 관리한다. (SecondPrizeLotto)
    - [x] 3등 로또의 정보를 관리한다. (ThirdPrizeLotto)
    - [x] 4등 로또의 정보를 관리한다. (FourthPrizeLotto)
    - [x] 5등 로또의 정보를 관리한다. (FifthPrizeLotto)
- [x] 한 장의 로또 정보를 관리한다. (Lotto)
- [x] 로또의 수량 정보를 관리한다. (LottoQuantity)
- [x] 구매한 수량만큼의 로또를 모아서 관리한다. (Lottos)
- [x] 당첨 정보를 관리한다. (PrizeNumber)
- [x] 구매 금액 정보를 관리한다. (PurchasePrice)
- [x] 당첨 번호를 관리한다. (WinNumbers)

### 예외 사항
- [x] 가격이 1000으로 나뉘어 떨어지지 않는 경우 (PRICE_DIVIDE_EXCEPTION)
- [x] 가격이 숫자가 입력 되지 않은 경우 (PRICE_NUMBER_EXCEPTION)
- [x] 로또 번호 및 당첨 번호가 6개가 아닌 경우 (LOTTO_NUMBER_COUNT_EXCEPTION)
- [x] 로또 번호 및 당첨 번호가 숫자가 아닌 경우 (LOTTO_NUMBER_EXCEPTION)
- [x] 이미 존재하는 로또 번호 및 당첨 번호 인 경우 (LOTTO_NUMBER_EXIST_EXCEPTION)
- [x] 로또 번호 및 당첨 번호가 범위를 벗어나는 경우 (LOTTO_NUMBER_RANGE_EXCEPTION)
