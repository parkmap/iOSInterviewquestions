**UITableView 동작 방식:**

`UITableView`는 데이터를 시각적으로 표시하기 위한 효과적인 방법으로 사용됩니다. 이는 특히 리스트나 그리드 형태의 데이터를 표현하는 데 매우 유용합니다.

1. **Data Source 및 Delegate:**
   - `UITableView`는 데이터를 표시하고 상호작용하는 데에 `UITableViewDataSource`와 `UITableViewDelegate` 프로토콜을 사용합니다.
   - `UITableViewDataSource`는 데이터 소스 역할을 하며, 테이블 뷰에 표시할 데이터 및 셀을 제공합니다.
   - `UITableViewDelegate`는 사용자의 상호작용과 관련된 이벤트를 처리하고, 특정 셀을 선택했을 때의 동작을 정의합니다.

2. **Reusability (셀 재사용):**
   - 효율성을 위해 `UITableView`는 셀을 재사용합니다. 스크롤될 때 화면에서 사라진 셀은 다시 사용되어 새로운 데이터를 표시하게 됩니다.

3. **Section과 Row:**
   - 테이블 뷰는 섹션(section)과 로우(row)로 구성됩니다. 섹션은 섹션 헤더와 푸터를 가질 수 있고, 로우는 실제 데이터를 나타냅니다.

4. **셀의 구성:**
   - 각 셀은 `UITableViewCell` 클래스를 기반으로 합니다. 다양한 스타일과 컴포넌트(텍스트, 이미지, 액세서리 뷰 등)를 가질 수 있습니다.

**UITableViewDataSource 프로토콜의 주요 메서드:**

`UITableViewDataSource` 프로토콜은 테이블 뷰에 데이터를 제공하는 데 필요한 메서드를 정의합니다. 가장 기본적인 메서드들은 다음과 같습니다:

1. **`numberOfSections(in:) -> Int`:**
   - 테이블 뷰의 섹션 개수를 반환합니다.

2. **`tableView(_:numberOfRowsInSection:) -> Int`:**
   - 주어진 섹션에 속한 로우의 개수를 반환합니다.

3. **`tableView(_:cellForRowAt:) -> UITableViewCell`:**
   - 특정 indexPath에 해당하는 셀을 반환합니다. 이 메서드에서는 재사용 큐에서 셀을 가져오고, 데이터를 해당 셀에 설정합니다.

```swift
func numberOfSections(in tableView: UITableView) -> Int {
    return 1 // 예시: 섹션은 1개
}

func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
    return data.count // 예시: 데이터 배열의 개수에 따라 로우 수 결정
}

func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
    let cell = tableView.dequeueReusableCell(withIdentifier: "CellIdentifier", for: indexPath)
    
    // 셀에 데이터 설정
    cell.textLabel?.text = data[indexPath.row]
    
    return cell
}
```

위의 코드에서 `"CellIdentifier"`는 셀의 재사용을 위한 식별자로, Interface Builder에서 설정하거나 코드에서 직접 할당할 수 있습니다.

이렇게 구현된 `UITableViewDataSource`를 통해 테이블 뷰는 데이터를 효과적으로 표시하고 관리할 수 있습니다.

 [목록](../README_link.md#ios)
