# jwp-subway-path

## 요구사항
### 역 등록 API
#### 비즈니스 요구사항
- [ ] 역이 등록될 때 양의 정수인 거리 정보가 포함되어야 한다.
- [ ] 노선에 역이 하나도 없을 때 두 역을 동시에 등록해야 한다.
- [ ] 하나의 역은 여러 개의 노선에 등록될 수 있다.
- [ ] 존재하는 역의 다음 역을 추가하면 중간에 역이 등록될 수 있다.
- [ ] 노선 사이에 역이 등록되는 경우 등록된 역을 포함한 전 역, 다음 역의 거리를 업데이트 한다.
- [ ] 노선 사이에 역이 등록되는 경우 새로 추가되는 역과 이전 역의 거리는 기존 역 사이의 거리보다 작아야 한다.
- [ ] 기준이 되는 역이 없으면 등록할 수 없다.

### 역 제거 API
- [ ] 역을 제거한 후 노선을 재배치한다.
- [ ] 역을 제거한 후 제거된 역의 전 역, 다음 역의 거리를 업데이트한다.
- [ ] 역을 제거한 후 노선에 역이 하나 남으면 해당 역도 제거한다.  

### 노선 조회 API
- [ ] 노선에 포함된 역을 순서대로 보여주도록 한다.

### 노선 목록 조회 API
- [ ] 노선에 포함된 역을 순서대로 보여주도록 한다.

## 도메인
### 지하철(Subway)
- [ ] 역과 거리 정보를 저장한다.

### 역(Station)
- [ ] 이름, 노선 리스트를 갖는다.

### 거리정보(Edge)
- [ ] 이전 역, 다음 역, 거리, 노선을 갖는다.

### 노선(Line)
- [x] 이름을 갖는다.
