# 구현 기능 목록

* getMoneyInput
* validateMoneyInput
* purchasePossibleLottos
* createNewLotto
* printCreatedLottos
* getWinningLottoInput
* validateWinningLottoInput
* getBonusLottoInput
* vaildateBonusLottoInput
* getStatistics
* getFifthPrize
* getFourthPrize
* getThirdPrize
* getSecondPrize
* getFirstPrize
* getProfitRate
* printStatistics
* printFifthPrize
* printFourthPrize
* printThirdPrize
* printSecondPrize
* printFirstPrize
* printProfitRate
* simulateLottoGame

## getMoneyInput

* 사용자의 로또 금액 금액을 입력받는다.
* 입력받은 값을 `return` 한다.

## validateMoneyInput

* 입력 받은 값이 유효한지 확인한다.
* 만약 입력 받은 값이 1000으로 나누어 떨어지지 않는다면, `false`를 리턴한다.
* 만약 입력 받은 값이 1000으로 나누어 떨어진다면, `true`를 리턴한다.

## purchasePossibleLottos

* 사용자의 로또 금액을 1000으로 나눈다.
* 해당 값의 횟수만큼 createNewLotto를 실행한다.

## createNewLotto

* 1 ~ 45까지, 중복이 없도록 총 6개의 숫자를 무작위로 생성한다.
* 생성된 오름차순 수열을 List `Lottos`에 저장한다.

## printCreatedLottos

* 생성된 로또 티켓의 정보를 순서대로 출력한다.
* 출력 내용은 다음과 같다.
    * x개를 구매했습니다.
    * [1, 2, 3, 4, 5, 6]
    * [2, 3, 4, 5, 6, 7]

## getWinningLottoInput

* 당첨 로또 번호를 입력받는다.
* 입력은 단일 String으로 이루어지며, 6개의 숫자는 각각 콤마 (,)로 구분된다.

## validateWinningLottoInput

* 당첨 로또 번호를 검증한다.
* 문자열을 콤마를 기준으로 파싱한다.
* 파싱 후 숫자가 총 6개가 아니라면 `false`를 리턴한다.
* 파싱 후 각 숫자가 1 미만 또는 45 초과인 경우가 존재하면 `false`를 리턴한다.
* 파싱 후 각 숫자 중 중복이 존재하면 `false`를 리턴한다.
* 위의 조건에 걸리지 않는다면 `true`를 리턴한다.

## getBonusLottoInput

* 보너스 번호를 입력받는다.

## validateBonusLottoInput

* 입력받은 보너스 번호를 검증한다.
* 입력받은 번호가 1 미만 45 초과인 경우가 존재하면 `false`를 리턴한다.
* 입력받은 번호가 기존의 당첨 번호 6개와 중복되는 경우가 존재하면 `false`를 리턴한다.
* 위의 조건에 걸리지 않았다면 `true`를 리턴한다.

## getStatistics

* 로또 통계를 구한다.
* `getFirstPrize`를 실행한다.
    * 6개가 모두 일치하는 경우를 확인한다.
* `getSecondPrize`를 실행한다.
    * 위의 경우에 해당하지 않는 로또 티켓에 대해, 번호 5개와 보너스 번호 1개가 일치하는 경우를 확인한다.
* `getThirdPrize`를 실행한다.
    * 위의 경우에 해당하지 않는 로또 티켓에 대해, 번호 5개가 일치하는 경우를 확인한다.
* `getFourthPrize`를 실행한다.
    * 위의 경우에 해당하지 않는 로또 티켓에 대해, 번호 4개가 일치하는 경우를 확인한다.
* `getFifthPrize`를 실행한다.
    * 위의 경우에 해당하지 않는 로또 티켓에 대해, 번호 3개가 일치하는 경우를 확인한다.
* `getProfitRate`를 실행한다.
    * 총 수익률 통계를 구한다.

## printStatistics

* 로또 통계를 출력한다.
* 다음을 호출한다.
    * printFifthPrize
    * printFourthPrize
    * printThirdPrize
    * printSecondPrize
    * printFirstPrize
    * printProfitRate

## printFifthPrize

* 5등 당첨 개수에 대한 정보를 출력한다.
* 출력은 아래와 같다.
    * 3개 일치 (5,000원) - 1개

## printFourthPrize

* 4등 당첨 개수에 대한 정보를 출력한다.
* 출력은 아래와 같다.
    * 4개 일치 (50,000원) - 1개

## printThirdPrize

* 3등 당첨 개수에 대한 정보를 출력한다.
* 출력은 아래와 같다.
    * 5개 일치 (1,500,000원) - 1개

## printSecondPrize

* 2등 당첨 개수에 대한 정보를 출력한다.
* 출력은 아래와 같다.
    * 5개 일치, 보너스 볼 일치 (30,000,000원) - 1개

## printFirstPrize

* 1등 당첨 개수에 대한 정보를 출력한다.
* 출력은 아래와 같다.
    * 6개 일치 (2,000,000,000원) - 1개

## printProfitRate

* 수익률을 출력한다.
* 출력은 아래와 같다.
    * 총 수익률은 62.5%입니다.

## simulateLottoGame

* 로또 게임을 시뮬레이션한다. 순서는 아래와 같다.
    * "구입금액을 입력해 주세요." 를 출력한다.
    * `getMoneyInput`을 실행하여 입력을 받는다.
    * `validateMoneyInput`을 실행하여 해당 숫자를 검증한다.
        * `false`를 받는 경우, 에러 메세지를 출력하고 `IllegalArgumentException`을 발생시킨다.
    * `purchasePossibleLottos`를 실행하여, 가능한 만큼 로또 티켓을 발행한다.
    * `printCreatedLottos`를 실행하여, 생성된 로또 티켓 목록을 출력한다.
    * `getWinningLottoInput`을 통해 당첨 번호를 입력 받는다.
    * `validateWinningLottoInput`을 통해 입력받은 당첨 번호를 검증한다.
        * `false`를 받는 경우, 에러 메세지를 출력하고 `IllegalArgumentException`을 발생시킨다.
    * `getBonusLottoInput`을 통해 보너스 번호를 입력 받는다.
        * `false`를 받는 경우, 에러 메세지를 출력하고 `IllegalArgumentException`을 발생시킨다.
    * `getStatistics`를 통해 당첨 정보 및 수익률 정보를 구한다.
    * `printStatistics`를 통해 당첨 정보 및 수익률 정보를 출력한다.
