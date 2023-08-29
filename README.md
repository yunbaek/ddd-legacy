# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항
### 포스 시스템 구현
#### 메뉴 그룹
- [ ] 메뉴 그룹을 등록한다.
  - [ ] 메뉴 그룹의 이름은 비어있거나 255자를 초과할 수 없다.
- [ ] 메뉴 그룹의 목록을 조회한다.

#### 메뉴
- [ ] 메뉴를 등록한다.
  - [ ] 메뉴의 가격은 0원 이상이어야 한다.
  - [ ] 메뉴의 가격은 메뉴 상품들 가격의 총 합보다 클 수 없다.
  - [ ] 메뉴의 메뉴 그룹은 이미 저장되어 있어야 한다.
  - [ ] 등록하려는 메뉴의 상품들은 이미 저장되어 있어야 한다.
  - [ ] 메뉴의 이름은 비어있거나 255자를 초과할 수 없다.
  - [ ] 메뉴의 이름에는 비속어가 포함 될 수 없다.
- [ ] 메뉴의 가격을 수정한다.
  - [ ] 메뉴의 가격은 0원 이상이어야 한다.
  - [ ] 메뉴의 가격은 메뉴 상품들 가격의 총 합보다 클 수 없다.
- [ ] 등록한 메뉴의 상품을 노출한다.
    - [ ] 메뉴의 가격은 메뉴 상품들 가격의 총 합보다 클 수 없다.
- [ ] 노출한 메뉴를 숨긴다.
- [ ] 메뉴의 목록을 조회한다.

#### 상품
- [ ] 새로운 상품을 등록한다.
  - [ ] 상품의 가격은 0원 이상이어야 한다.
  - [ ] 상품의 이름은 비어있을 수 없고, 255자를 초과할 수 없다.
  - [ ] 상품의 이름에는 비속어가 포함 될 수 없다.
- [ ] 상품의 가격을 변경한다.
    - [ ] 상품의 가격은 0원 이상이어야 한다.
    - [ ] 변경하려는 상품의 가격은 메뉴 상품들 가격의 총 합보다 클 수 없다. 큰 경우 해당 메뉴를 숨긴다.
- [ ] 상품의 목록을 조회한다.
 
#### 주문
- [ ] 주문을 등록한다.
  - [ ] 주문은 유형을 가진다. (배달, 포장, 매장)
  - [ ] 주문은 상태를 가진다. (대기, 승낙, 서빙, 배달중, 배달완료, 완료)
  - [ ] 주문을 하면 초기 주문 상태는 `조리중` 상태이다.
  - [ ] 주문 항목 정보가 올바르지 않으면 주문을 할 수 없다.
    - [ ] 주문 유형은 비어있을 수 없다.
      - [ ] 주문 유형이 배달이면 배달 주소가 있어야 한다.
      - [ ] 주문 유형이 매장 식사이면 사용 가능한 주문 테이블이 있어야 한다.
    - [ ] 주문할 메뉴는 1개 이상 있어야 한다.
    - [ ] 주문 항목이 1개 이상 있어야 한다.
    - [ ] 주문 항목들의 메뉴들은 모두 노출된 상태여야 한다.
    - [ ] 주문을 받은 테이블은 등록된 테이블이어야 한다.
    - [ ] 주문을 받은 테이블은 비어있지 않아야 한다.
- [ ] 주문을 수락한다.
  - [ ] 주문이 대기 상태여야 한다.
  - [ ] 주문 유형이 배달이면, 배달 업체에 배달 요청을 한다.
    - [ ] 배달에 필요한 주문 정보를 배달 업체에 전달한다.
- [ ] 주문을 제공한다.
  - [ ] 주문이 승낙 상태여야 한다.
- [ ] 배달 주문을 배달한다.
  - [ ] 주문의 유형이 배달이어야한다.
  - [ ] 주문의 상태가 서빙 상태여야 한다.
- [ ] 배달 주문의 배달을 완료한다.
  - [ ] 주문의 상태가 배달중 상태여야 한다.
- [ ] 주문을 완료한다.
  - [ ] 배달 주문의 상태가 배달 완료여야 한다.
  - [ ] 포장 또는 매장 주문의 상태가 제공이여야 한다.
  - [ ] 매장 주문의 경우, 주문 테이블을 정리한다.
- [ ] 주문의 목록을 조회한다.

#### 주문 테이블 (Order Table)
- [ ] 테이블을 등록한다.
  - [ ] 테이블의 이름은 비어있을 수 없고, 255자를 초과할 수 없다.
- [ ] 등록된 테이블에 고객을 입장시킨다.
- [ ] 등록된 테이블에 고객을 퇴장시킨다.
  - [ ] 테이블의 주문 상태가 완료여야 한다.
- [ ] 입장된 테이블의 고객 수를 변경한다.
  - [ ] 테이블의 고객 수는 0명 이상이어야 한다.
  - [ ] 테이블에 고객이 입장 상태여야 한다.
- [ ] 테이블의 목록을 조회한다.

## 용어 사전

| 한글명 | 영문명 | 설명 |
| --- | --- | --- |
|  |  |  |

## 모델링
