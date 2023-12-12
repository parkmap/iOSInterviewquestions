Foundation 프레임워크는 앱 및 프레임워크를 위한 기본 기능을 제공하며, 데이터 저장 및 지속성, 텍스트 처리, 날짜 및 시간 계산, 정렬 및 필터링, 그리고 네트워킹을 포함합니다. Foundation이 정의한 클래스, 프로토콜, 및 데이터 유형은 macOS, iOS, watchOS, 그리고 tvOS SDK에서 전반적으로 사용됩니다.


| 클래스                            | 설명                                                                |
| --------------------------------- | ------------------------------------------------------------------- |
| NSObject                         | 모든 Objective-C 및 Swift 클래스의 기본 클래스                      |
| NSString 및 NSMutableString      | 문자열을 다루기 위한 클래스                                           |
| NSArray, NSMutableArray          | 배열을 다루기 위한 클래스                                              |
| NSDictionary, NSMutableDictionary | 딕셔너리와 키-값 쌍 형태의 데이터를 다루기 위한 클래스               |
| NSData, NSMutableData             | 이진 데이터를 다루기 위한 클래스                                      |
| NSDate, NSDateFormatter           | 날짜와 시간을 다루기 위한 클래스                                     |
| NSFileManager                    | 파일 및 디렉터리 관리를 위한 클래스                                   |
| NSURL, NSURLComponents            | URL을 처리하고 조작하기 위한 클래스                                    |
| NSJSONSerialization               | JSON 데이터를 다루기 위한 클래스                                     |
| NSUserDefaults                   | 앱 설정을 저장하고 검색하기 위한 클래스                               |
| NSNotificationCenter              | 통지를 사용하여 애플리케이션 내에서 이벤트를 전달하는 클래스          |
| NSURLSession                    | 네트워크 통신을 수행하기 위한 클래스                                  |
| NSAttributedString, NSMutableAttributedString | 텍스트에 스타일 및 속성을 적용하는 클래스   |
| NSPredicate                      | 데이터 컬렉션을 필터링하고 정렬하기 위한 클래스                       |
| NSNumber                        | 숫자를 표현하기 위한 클래스                                          |
| NSCharacterSet                 | 문자 세트를 정의하고 조작하기 위한 클래스                             |
| NSError                         | 에러를 표현하기 위한 클래스                                           |
| NSXMLParser                     | XML 문서를 파싱하기 위한 클래스                                       |
| NSCache                         | 캐시를 구현하기 위한 클래스                                           |
| NSOperation, NSOperationQueue   | 비동기 작업을 관리하기 위한 클래스와 큐                              |
| NSRunLoop                       | 이벤트 루프를 관리하기 위한 클래스                                  |
| NSLocale                        | 지역화된 정보를 관리하기 위한 클래스                                |
| NSUUID                          | UUID(Universally Unique Identifier)를 생성하고 다루기 위한 클래스   |
| NSRegularExpression            | 정규 표현식을 사용하여 문자열을 검색하고 조작하기 위한 클래스       |
| NSUserDefaultsController        | 사용자 설정 관리를 위한 컨트롤러 클래스                               |
| NSFileHandle                    | 파일 핸들을 다루기 위한 클래스                                       |
| NSPredicateEditor               | 프레디케이트(조건)를 구성하기 위한 편집기 클래스                      |
| NSKeyedArchiver, NSKeyedUnarchiver | 객체를 아카이브(serialize)하고 언아카이브(deserialize)하기 위한 클래스 |
| NSDecimalNumber                 | 십진수 연산을 위한 클래스                                            |
| NSNotificationCenter           | 애플리케이션 내에서의 이벤트 전달을 위한 클래스                     |
| NSFormatter                     | 데이터 형식을 지정하기 위한 추상 클래스                              |
| NSAffineTransform                | 2D 변환 매트릭스를 나타내기 위한 클래스                               |
| NSArchiver                       | 객체 그래프를 아카이브하기 위한 클래스                                 |
| NSAssertionHandler               | 어서션(assertion) 실패를 처리하는 핸들러 클래스                      |
| NSBundle                         | 번들에 포함된 리소스 및 정보에 접근하기 위한 클래스                  |
| NSCalendar                       | 날짜와 시간을 관리하기 위한 클래스                                   |
| NSCharacterSet                   | 문자 세트를 나타내고 조작하기 위한 클래스                           |
| NSComparisonPredicate            | 비교를 수행하기 위한 프레디케이트 클래스                             |
| NSCondition                      | 여러 스레드 간에 조건을 통한 통신을 지원하기 위한 클래스            |
| NSCoder                         | 객체를 인코딩 및 디코딩하기 위한 추상 클래스                          |
| NSCopying                       | 객체를 복사하기 위한 프로토콜                                         |
| NSCountedSet                    | 객체의 개수를 세는 집합 클래스                                       |
| NSDataDetector                  | 데이터 유형을 감지하는 클래스                                         |
| NSDateComponents                | 날짜 및 시간 구성 요소를 나타내기 위한 클래스                       |
| NSDecimal                       | 고정 소수점 수를 나타내기 위한 구조체                               |
| NSExpression                    | 수식을 나타내고 계산하기 위한 클래스                                 |
| NSFormatter                     | 데이터 형식을 지정하기 위한 추상 클래스                              |
| NSHashTable                     | 해시 테이블을 나타내기 위한 클래스                                   |
| NSIndexPath                    | 트리 구조에서 특정 위치를 나타내기 위한 클래스                      |
| NSIndexSet                      | 정수 집합을 나타내기 위한 클래스                                     |
| NSInvocation                    | 메소드 호출을 나타내기 위한 클래스                                   |
| NSItemProvider                  | 데이터를 다른 애플리케이션에 전달하기 위한 클래스                   |
| NSLinguisticTagger              | 언어 및 문법 태깅을 수행하기 위한 클래스                             |
| NSMapTable                      | 키-값 쌍을 저장하는 테이블을 나타내기 위한 클래스                   |
| NSMeasurement                   | 물리적 측정 값을 나타내기 위한 클래스                               |
| NSMetadata                      | 메타데이터 쿼리 및 검색을 수행하기 위한 클래스                      |
| NSMethodSignature               | 메소드 시그니처를 나타내기 위한 클래스                               |
| NSNotificationCenter           | 애플리케이션 내에서의 이벤트 전달을 위한 클래스                     |
| NSNotificationQueue             | 특정 큐에 이벤트를 지연시켜 전달하기 위한 클래스                    |
| NSNull                          | 널(Null) 객체를 나타내기 위한 클래스                                |
| NSOperationQueue                | 비동기 작업을 수행하기 위한 큐 클래스                               |
| NSOrderedSet                    | 순서가 있는 집합을 나타내기 위한 클래스                             |
| NSOrthography                   | 언어 및 철자법 정보를 나타내기 위한 클래스                           |
| NSPointerArray                  | 포인터 배열을 나타내기 위한 클래스                                   |
| NSPointerFunctions              | 포인터 키 및 값에 대한 동작을 정의하기 위한 클래스                 |
| NSPredicateEditorRowTemplate    | 프레디케이트 에디터에서 사용되는 템플릿 클래스                       |
| NSProgress                      | 작업의 진행 상태를 나타내기 위한 클래스                             |
| NSPropertyListSerialization     | 프로퍼티 리스트(serialized property list)를 다루기 위한 클래스     |
| NSProxy                         | 다른 객체를 대리하여 동작하는 추상 클래스                           |
| NSRegularExpressionOptions      | 정규 표현식 옵션을 나타내는 열거형                                   |
| NSRunLoopMode                   | 런 루프 모드를 나타내는 문자열 상수                                  |
| NSScanner                       | 문자열에서 데이터를 스캔하기 위한 클래스                             |
| NSSet                           | 고유한 객체의 집합을 나타내기 위한 클래스                           |
| NSShadow                        | 그림자 효과를 나타내기 위한 클래스                                   |
| NSSocketPort                    | 소켓 통신을 위한 포트 클래스                                        |
| NSSortDescriptor                | 정렬 기준을 나타내기 위한 클래스                                   |
| NSStream                        | 스트림을 나타내기 위한 클래스                                       |
| NSStringDrawingOptions          | 문자열을 그리는 데 사용되는 옵션을 나타내는 열거형                  |
| NSStringEncoding                | 문자열 인코딩을 나타내는 상수 값                                    |
| NSTextCheckingResult            | 텍스트 검사 결과를 나타내기 위한 클래스                            |
| NSThread                        | 스레드를 나타내기 위한 클래스                                       |
| NSTimeZone                      | 시간대 정보를 나타내기 위한 클래스                                 |
| NSTimer                         | 타이머 이벤트를 나타내기 위한 클래스                               |
| NSURLAuthenticationChallenge   | URL 연결의 인증에 대한 도전을 나타내기 위한 클래스                  |
| NSURLCache                      | URL 요청에 대한 캐시를 나타내기 위한 클래스                         |
| NSURLComponents                 | URL을 구성하고 조작하기 위한 클래스


[Foundation - Apple](https://developer.apple.com/documentation/foundation)
