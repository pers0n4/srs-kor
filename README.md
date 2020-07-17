# Software Requirements Specification

- [Considerations for producing a good SRS](#considerations-for-producing-a-good-srs)
  - [1. SRS의 특성(Nature of the SRS)](#1-srs의-특성nature-of-the-srs)
  - [2. SRS의 배경(Environment of the SRS)](#2-srs의-배경environment-of-the-srs)
  - [3. 좋은 SRS의 특징(Characteristics of a good SRS)](#3-좋은-srs의-특징characteristics-of-a-good-srs)
  - [4. SRS의 협업(Joint preparation of the SRS)](#4-srs의-협업joint-preparation-of-the-srs)
  - [5. SRS 개선(SRS evolution)](#5-srs-개선srs-evolution)
  - [6. 프로토타이핑(Prototyping)](#6-프로토타이핑prototyping)
  - [7. SRS에 설계 포함하기(Embedding design in the SRS)](#7-srs에-설계-포함하기embedding-design-in-the-srs)
  - [8. SRS에 프로젝트 요구사항 포함하기(Embedding project requirements in the SRS)](#8-srs에-프로젝트-요구사항-포함하기embedding-project-requirements-in-the-srs)
- [The parts of an SRS](#the-parts-of-an-srs)
  - [1. 소개(Introduction)](#1-소개introduction)
    - [1.1. 목적(Purpose)](#11-목적purpose)
    - [1.2. 범위(Scope)](#12-범위scope)
    - [1.3. 용어 및 약어 정의(Definitions, acronyms and abbreviations)](#13-용어-및-약어-정의definitions-acronyms-and-abbreviations)
    - [1.4. 참고자료(References)](#14-참고자료references)
    - [1.5. 개요(Overview)](#15-개요overview)
  - [2. 전체 시스템 개요(Overall description)](#2-전체-시스템-개요overall-description)
    - [2.1. 제품 관점(Product perspective)](#21-제품-관점product-perspective)
      - [2.1.1. 시스템 인터페이스(System interfaces)](#211-시스템-인터페이스system-interfaces)
      - [2.1.2. 사용자 인터페이스(User interfaces)](#212-사용자-인터페이스user-interfaces)
      - [2.1.3. 하드웨어 인터페이스(Hardware interfaces)](#213-하드웨어-인터페이스hardware-interfaces)
      - [2.1.4. 소프트웨어 인터페이스(Software interfaces)](#214-소프트웨어-인터페이스software-interfaces)
      - [2.1.5. 통신 인터페이스(Communications interfaces)](#215-통신-인터페이스communications-interfaces)
      - [2.1.6. 메모리 제약사항(Memory constraints)](#216-메모리-제약사항memory-constraints)
      - [2.1.7. 운영(Operations)](#217-운영operations)
      - [2.1.8. 사이트 적용 요건(Site adaption requirements)](#218-사이트-적용-요건site-adaption-requirements)
    - [2.2. 제품 기능(Product functions)](#22-제품-기능product-functions)
    - [2.3. 사용자 특성(User characteristics)](#23-사용자-특성user-characteristics)
    - [2.4. 제약사항(Constraints)](#24-제약사항constraints)
    - [2.5. 가정 및 의존성(Assumptions and dependencies)](#25-가정-및-의존성assumptions-and-dependencies)
    - [2.6. 단계별 요구사항(Apportioning of requirements)](#26-단계별-요구사항apportioning-of-requirements)
  - [3. 상세 요구사항(Specific requirements)](#3-상세-요구사항specific-requirements)
    - [3.1. 외부 인터페이스 요구사항(External interface requirements)](#31-외부-인터페이스-요구사항external-interface-requirements)
      - [3.1.1. 사용자 인터페이스(User interfaces)](#311-사용자-인터페이스user-interfaces)
      - [3.1.2. 하드웨어 인터페이스(Hardware interfaces)](#312-하드웨어-인터페이스hardware-interfaces)
      - [3.1.3. 소프트웨어 인터페이스(Software interfaces)](#313-소프트웨어-인터페이스software-interfaces)
      - [3.1.4. 통신 인터페이스(Communications interfaces)](#314-통신-인터페이스communications-interfaces)
    - [3.2. 기능 요구사항(Functional requirements)](#32-기능-요구사항functional-requirements)
    - [3.3. 성능 요구사항(Performance requirements)](#33-성능-요구사항performance-requirements)
    - [3.4. 논리적 데이터베이스 요구사항(Logical database requirements)](#34-논리적-데이터베이스-요구사항logical-database-requirements)
    - [3.5. 설계 제약사항(Design constraints)](#35-설계-제약사항design-constraints)
      - [3.5.1. 표준 준수(Standards compliance)](#351-표준-준수standards-compliance)
    - [3.6. 소프트웨어 시스템 속성(Software system attributes)](#36-소프트웨어-시스템-속성software-system-attributes)
      - [3.6.1. 신뢰성(Reliability)](#361-신뢰성reliability)
      - [3.6.2. 가용성(Availability)](#362-가용성availability)
      - [3.6.3. 보안성(Security)](#363-보안성security)
      - [3.6.4. 유지 보수성(Maintainability)](#364-유지-보수성maintainability)
      - [3.6.5. 이식성(Portability)](#365-이식성portability)
    - [3.7. 상세 요구사항의 구성(Organizing the specific requirements)](#37-상세-요구사항의-구성organizing-the-specific-requirements)
      - [3.7.1. 시스템 모드(System mode)](#371-시스템-모드system-mode)
      - [3.7.2. 사용자 부류(User class)](#372-사용자-부류user-class)
      - [3.7.3. 객체(Objects)](#373-객체objects)
      - [3.7.4. 특징(Feature)](#374-특징feature)
      - [3.7.5. 자극(Stimulus)](#375-자극stimulus)
      - [3.7.6. 반응(Response)](#376-반응response)
      - [3.7.7. 기능 계층(Functional hierarchy)](#377-기능-계층functional-hierarchy)
      - [3.7.8. Additional comments](#378-additional-comments)
  - [4. 추가 정보(Supporting information)](#4-추가-정보supporting-information)
    - [4.1. Table of contents and index(목차와 인덱스)](#41-table-of-contents-and-index목차와-인덱스)
    - [4.2. 부록(Appendixes)](#42-부록appendixes)
- [Annex](#annex)
  - [A. SRS templates](#a-srs-templates)
    - [A.1. Template of SRS Section 3 organized by mode: Version 1](#a1-template-of-srs-section-3-organized-by-mode-version-1)
    - [A.2. Template of SRS Section 3 organized by mode: Version 2](#a2-template-of-srs-section-3-organized-by-mode-version-2)
    - [A.3. Template of SRS Section 3 organized by user class](#a3-template-of-srs-section-3-organized-by-user-class)
    - [A.4. Template of SRS Section 3 organized by object](#a4-template-of-srs-section-3-organized-by-object)
    - [A.5. Template of SRS Section 3 organized by feature](#a5-template-of-srs-section-3-organized-by-feature)
    - [A.6. Template of SRS Section 3 organized by stimulus](#a6-template-of-srs-section-3-organized-by-stimulus)
    - [A.7. Template of SRS Section 3 organized by functional hierarchy](#a7-template-of-srs-section-3-organized-by-functional-hierarchy)
    - [A.8. Template of SRS Section 3 showing multiple organizations](#a8-template-of-srs-section-3-showing-multiple-organizations)

## Considerations for producing a good SRS

### 1. SRS의 특성(Nature of the SRS)

- SRS 작성자가 다루어야 할 기본 내용
  1. 기능성(Functionality)
     > - 소프트웨어가 수행하는 작업이 무엇인가?
  1. 외부 인터페이스(External interfaces)
     > - 소프트웨어가 사람, 하드웨어, 다른 소프트웨어와 어떻게 상호작용 하는가?
  1. 성능(Performance)
     > - 속도, 가용성, 반응 시간, 다양한 소프트웨어 기능의 복구 속도가 어느 정도인가?
  1. 속성(Attributes)
     > - 이식성, 정확성, 유지 보수성, 보안성 및 고려사항이 무엇인가?
  1. 구현에 부과된 설계 제약사항(Design constraints imposed on an implementation)
     > - 적용해야 하는 표준, 구현하는 언어, 데이터베이스 무결성 정책, 리소스 제약사항, 운영체제가 무엇인가?

### 2. SRS의 배경(Environment of the SRS)

> - IEEE Std 610.12-1990에 정의된 전체 프로젝트 계획에서 SRS가 담당하는 부분을 고려하는 것이 중요하다.
> - IEEE Std 1074-1997에서는 단계별 소프트웨어의 수명 주기와 각 단계에 해당하는 입력을 설명한다.
> - SRS는 소프트웨어 개발 프로세스에서 특정 역할을 담당하고 있으므로 작성자는 해당 역할을 벗어나지 않도록 주의해야 한다.
> - SRS가 따라야 하는 규칙
>   1. 모든 소프트웨어 요구사항을 정확하게 정의해야 한다. 요구사항은 해결되어야 하는 작업의 특성 또는 프로젝트의 특성으로 인해 생겨날 수 있다.
>   1. 설계 혹은 구현에 관한 상세한 내용을 포함해서는 안 된다. 이와 같은 내용은 설계 단계에서 포함되어야 한다.
>   1. 소프트웨어에 제약사항을 추가로 부과해서는 안 된다. 이런 속성은 소프트웨어 품질보증 계획(Software Quality Assurance Plan)과 같은 문서에서 명세 되어야 한다.

### 3. 좋은 SRS의 특징(Characteristics of a good SRS)

1. 정확성(Correct)
   > - SRS에 명시된 모든 요구사항이 소프트웨어가 만족시켜야 하는 내용에 해당한다면 SRS는 correct하다.
1. 확실성(Unambiguous)
   > - SRS에 명시된 모든 요구사항이 단 한 가지 뜻으로 해석된다면 SRS는 unambiguous하다.
   > - 최소한 고유한 용어를 사용하여 제품의 각 특성을 설명해야 한다.
   > - 특정 맥락에서 사용된 용어가 여러 의미를 가질 수 있는 경우, 해당 용어에 관한 구체적인 뜻을 glossary에 포함하는 것이 좋다.
   > - 모호함을 회피하는 방법
   >   1. 자연 언어의 위험을 인지하고 회피하기(Natural language pitfalls)
   >      - 자연어는 본질이 모호하다.
   >      - 자연어가 사용된 SRS는 모호한 언어의 사용을 판단할 수 있는 독립적인 당사자가 검토하는 것이 좋다.
   >   1. 요구사항 명세 언어(Requirements specification languages)
   >      - 자연어가 포함하는 모호성을 회피하기 위한 한 가지 방법은 SRS를 요구사항 명세 언어로 표현하는 것이다.
   >      - 명세 언어를 사용할 때의 단점
   >        1. 언어를 배울 때 걸리는 시간
   >        1. 기술적인 지식이 부족한 사용자의 이해
   >      - 명세 언어를 사용할 때의 장점
   >        1. 요구사항을 효과적으로 표현
   >        1. 미묘한 요구사항의 반영
   >   1. 표현 도구(Representation tools)
1. 완전성(Complete)
   > - SRS가 아래 조건들을 만족한다면 SRS는 complete하다.
   > - SRS가 complete하기 위한 조건
   >   1. 기능성, 성능, 설계 제약사항, 속성, 외부 인터페이스와 관련된 모든 요구사항을 인지하고 처리해야 한다.
   >   1. 소프트웨어에서 실현될 수 있는 모든 입력 값의 상황에 대한 반응이 정의되어야 한다.
   >      - 유효한 입력 값과 유효하지 않은 입력 값 모두에 대한 응답을 지정하는 것이 중요함
   >   1. SRS의 모든 그림, 표, 다이어그램에 관한 full label이 참조되어야 하고, 모든 용어와 측정 단위가 정의되어야 한다.
   > - TBD(to be determined)라는 용어를 사용하는 SRS는 완전한 SRS가 아니다.
   1. TBD가 필요한 상황
      > - 상황을 해결할 수 있도록 TBD를 발생시키는 조건에 관한 설명
      > - TBD를 없애기 위해 해야 할 일, TBD의 제거에 책임이 있는 사람, 언제 제거되어야 하는지에 관한 설명
1. 일관성(Consistent)
   > - SRS가 어떤 상위의 문서와도 충돌하지 않는다면 SRS는 consistent하다.
   > - SRS에서 발생할 수 있는 충돌의 유형
   >   1. 현실 세계의 객체에 지정된 특성의 충돌
   >   1. 두 행동 사이의 논리적 혹은 시간적 충돌
   >   1. 같은 객체를 설명하는 둘 이상의 요구사항에서 서로 다른 용어의 사용
1. 중요도/안정 우선순위(Ranked for importance and/or stability)
   > - SRS의 각 요구사항은 중요도나 안정성에 따라 등급이 매겨진다.
   > - 요구사항의 등급을 식별할 때의 이점
   >   1. 고객에게 숨겨진 가정 사항을 명확하게 할 수 있다.
   >   1. 개발자가 소프트웨어 정확하게 설계하고 제품의 각 부분에 적절한 수준의 노력을 할 수 있도록 한다.
   1. 안정도(Degree of stabillity)
      > - 안정성은 소프트웨어 시스템이 지원하는 단체, 기능, 사람들에 의해 영향을 받는 앞으로 다가올 사건에 대한 경험이나 지식에 근거하여 어떤 요구사항의 예상 변경 횟수로 표현될 수 있다.
   1. 필요도(Degree of necessity)
      > - 요구사항의 순위를 지정하는 또 다른 방법으로는 요구사항을 필수, 조건, 선택 사항의 종류로 구분하는 것이다.
      1. 필수(Essential)
         > - 제공되지 않는다면 소프트웨어는 수용될 수 없다.
      1. 조건(Conditional)
         > - 소프트웨어를 향상할 수 있는 요구사항이지만, 존재하지 않더라도 수용할 수 없는 제품은 아니다.
      1. 선택(Optional)
         > - 가치가 있거나, 그렇지 않을 수 있는 기능으로 SRS를 초과하는 기회를 제공한다.
1. 검증 가능성(Verifiable)
   > - SRS에 기술된 모든 요구사항을 검증할 수 있다면 SRS는 verifiable하다.
   > - 일반적으로 모호한 요구사항은 검증할 수 없다.
1. 수정 가능성(Modifiable)
   > - SRS의 구조와 스타일을 유지하면서 요구사항을 쉽고, 완전하고, 일관되게 변경할 수 있다면 SRS는 modifiable하다.
   > - 수정 가능한 SRS가 되기 위한 조건
   >   1. 목차, 인덱스, 명시적 상호 참조가 있는 사용하기 쉬운 구조를 가져야 한다.
   >   1. 중복되지 않아야 한다. (같은 요구사항이 SRS의 다른 곳에 나타나지 않아야 한다.)
   >   1. 요구사항을 혼합하여 표현하지 말고, 각 요구사항을 별도로 표현해야 한다. > >
   >      > - 중복 자체는 오류가 아니지만, 오류로 이어질 수 있다.
   >      > - 중복성이 때로는 SRS를 더 읽기 쉽게 만드는 데 도움이 될 수 있지만, 문서가 업데이트될 때 문제가 발생할 수 있다.
   >      > - 중복이 필요할 때 SRS는 명시적 상호 참조를 포함하여 이를 수정할 수 있도록 해야 한다.
1. 추적 가능성(Traceable)
   > - SRS의 각 요구사항의 출처가 명확하고, 향후 개발 또는 개선 문서에서 참조할 수 있다면 SRSsms traceable하다.
   > - 추적 가능한 SRS의 유형
   >   1. Backwared traceability
   >      - 각 요구사항이 이전 문서의 출처를 명시적으로 참조한다.
   >   1. Forward traceability - 각 요구사항이 고유한 이름이나 참조 번호를 갖는다. > >
   >      > - SRS의 forward traceability는 소프트웨어의 운영 및 유지 보수 단계에서 특히 중요하다.
   >      > - 코드와 설계 문서가 수정됨에 따라 변경될 수 있는 전체 요구사항을 필수로 확인할 수 있어야 한다.

### 4. SRS의 협업(Joint preparation of the SRS)

> - 소프트웨어 개발 프로세스는 완성된 소프트웨어가 무엇을 해야 하는지를 공급자와 고객의 합의하는 것에서 시작된다.
> - SRS를 공동으로 작성해야 하는 이유
>   1. 고객은 일반적으로 소프트웨어 설계와 개발 프로세스를 이해하지 못한다.
>   1. 공급자는 일반적으로 고객이 만족할 만한 시스템의 요구사항을 지정하기에 충분할 만큼 고객의 문제와 활동 분야를 이해하지 못한다.

### 5. SRS 개선(SRS evolution)

> - SRS는 소프트웨어의 개발 진행에 따라 발전이 필요할 수 있다. (프로젝트가 시작되는 시점에 일부 세부 정보를 지정하는 것이 불가능했을 수 있다.)
> - SRS에서 결함, 단점, 부정확한 정보가 발견될 경우 추가로 변경될 수 있다.
> - SRS를 수정할 때 고려해야 하는 내용
>   1. 앞으로의 개정이 예상되는 상황에서도 요구사항은 변경되는 시점에서 완전하고 철저하게 명세 되어야 한다.
>   1. 예상된 변경을 확인, 제어, 추적, 보고하기 위한 절차를 시작해야 한다.
>      1. 변화에 대한 정확하고 완전한 추적
>      1. 현재의 SRS와 대체된 부분의 검토

### 6. 프로토타이핑(Prototyping)

> - 프로토타이핑은 프로젝트의 요구사항 부분에서 자주 사용된다.
> - 시스템의 특성을 나타내는 프로토타입을 빠르고 쉽게 생성하는 방법의 가이드: ASTM E1340-96
> - 프로토타이핑이 유용한 이유
>   1. 고객은 SRS를 읽고 반응하는 것보다 프로토타입을 보고 반응할 가능성이 더 높으므로 신속한 피드백을 제공할 수 있다.
>   1. 프로토타입은 시스템의 예기치 못한 동작을 보여줌에 따라 해답을 제시할 뿐만 아니라 새로운 질문을 제시한다.
>   1. 프로토타입에 기초한 SRS는 개발 중 변동이 크지 않아 개발 시간이 단축된다. > >
>      > - 프로토타입은 소프트웨어 요구사항을 도출하는 방법으로 사용해야 한다.
>      > - 화면이나 보고서 형식의 일부 특성은 프로토타입에서 직접 추출할 수 있다.
>      > - 다른 요구사항은 프로토타입으로 실험을 실행함으로써 추론할 수 있다.

### 7. SRS에 설계 포함하기(Embedding design in the SRS)

> - 요구사항은 외부적으로 보이는 시스템의 기능이나 속성으로 지정한다.
> - 설계는 시스템의 하위 구성 요소 또는 다른 하위 구성 요소의 인터페이스를 설명한다.
> - SRS 작성자는 요구되는 설계 제약사항을 확인하고 특정 설계를 명확하게 구분해야 한다.
> - SRS는 수행할 서비스에 초점을 맞춰야 하며, 어떤 위치에서 어떤 결과를 초래하는지를 알기 위해 어떤 기능을 수행할 것인지를 지정해야 한다.
> - SRS에 포함되지 않는 내용
>   1. 소프트웨어를 모듈로 분할
>   1. 모듈에 할당되는 기능
>   1. 모듈 사이의 정보 또는 제어 흐름
>   1. 데이터 구조

1. 필요한 설계 요구사항(Necessary design requirements) 1. 특정한 기능을 분리된 모듈로 유지한다. 1. 프로그램의 일부 영역 사이에 제한된 통신만 허용한다. 1. 중요한 변수에 대한 데이터 무결성을 검사한다.
   > > - 유효한 설계 제약 조건의 예로는 물리적 요구사항, 성능 요구사항, 소프트웨어 개발 표준, 소프트웨어 품질 보증 표준이 있다.
   > > - 요구사항은 오로지 외부 관점에서 명시되어야 한다.
   > > - 모델을 활용하여 요구사항을 설명할 때는 외부 동작만 나타내며 설계는 지정하지 않는다.

### 8. SRS에 프로젝트 요구사항 포함하기(Embedding project requirements in the SRS)

> - SRS는 소프트웨어를 생산하는 프로세스가 아니라 소프트웨어 제품 그 자체에 관한 내용을 다루어야 한다.
> - 프로젝트 요구사항은 소프트웨어 생산과 관련된 계약 문제에 대해 고객과 공급자 사이의 이해를 나타내므로 SRS에 포함해서는 안 된다.
> - SRS에 포함되어서는 안 되는 프로젝트 항목
>   1. 비용(Cost)
>   1. 배포 일정(Delivery schedules)
>   1. 보고 절차(Reporting procedures)
>   1. 소프트웨어 개발 방법(Software development method)
>   1. 품질 보증(Quality assurance)
>   1. 유효성 및 검증 기준(Validation and verification criteria)
>   1. 인수 절차(Acceptance procedures)

## The parts of an SRS

### 1. 소개(Introduction)

#### 1.1. 목적(Purpose)

> - SRS의 목적을 설명한다.
> - SRS의 대상을 지정한다.

#### 1.2. 범위(Scope)

> - 소프트웨어의 이름으로 소프트웨어 제품을 식별한다.
> - 소프트웨어가 무엇을 하고, 필요한 경우 무엇을 하지 않는지 설명한다.
> - 소프트웨어의 장점, 목적, 목표를 설명한다.

#### 1.3. 용어 및 약어 정의(Definitions, acronyms and abbreviations)

> - SRS에서 사용되는 용어, 머리글자, 약어를 정의한다.
> - 부록(appendix) 또는 다른 문서의 참조를 통해 제공될 수 있다.

#### 1.4. 참고자료(References)

> - SRS의 외부에서 참고한 모든 문서의 목록을 제공한다.
> - 각 문서의 제목, 보고서 번호(해당하는 경우만), 날짜, 출판 단체로 식별한다.
> - 참고자료에 접근할 수 있는 출처를 지정한다.

#### 1.5. 개요(Overview)

> - SRS의 나머지 부분이 포함하고 있는 내용을 설명한다.
> - SRS가 어떻게 구성되어 있는지 설명한다.

### 2. 전체 시스템 개요(Overall description)

> - 제품 및 제품 요구사항에 영향을 미치는 일반적인 요인을 설명해야 한다.
> - 특정 요구사항을 설명하지 않고, 상세 요구사항(Specific requirements)에 관한 배경을 제공한다.

#### 2.1. 제품 관점(Product perspective)

> - 제품을 관련된 다른 제품과의 관계를 중심으로 봐야 한다.
> - 제품이 독립적인 경우 명시되어야 하고, 더 큰 시스템의 구성 요소로 정의된다면 시스템의 요구사항을 소프트웨어의 기능과 관계시켜야 하며 시스템과 소프트웨어 사이의 인터페이스를 식별해야 한다.

##### 2.1.1. 시스템 인터페이스(System interfaces)

> - 각 시스템 인터페이스를 나열한다.
> - 시스템 요구사항을 달성하기 위한 소프트웨어 기능과 시스템에 일치하는 인터페이스에 관해 설명한다.

##### 2.1.2. 사용자 인터페이스(User interfaces)

> 1. 소프트웨어 제품과 사용자 간 인터페이스의 논리적 특성을 지정한다.
>    - 소프트웨어 요구사항을 충족하는 데 필요한 구성 특성(필요한 화면 형식, 페이지 또는 창 레이아웃, 보고서나 메뉴의 내용, 프로그래밍 가능한 기능 키의 사용 가능)을 포함
> 1. 시스템을 사용해야 하는 사람에게 최적화된 모든 측면을 설명한다.

##### 2.1.3. 하드웨어 인터페이스(Hardware interfaces)

> - 소프트웨어 제품과 시스템의 하드웨어 컴포넌트 사이에 각 인터페이스의 논리적 특성을 지정해야 한다.
> - 지원하는 기기의 종류와 지원 방법, 사용하는 프로토콜 등에 관한 내용을 다룬다.

##### 2.1.4. 소프트웨어 인터페이스(Software interfaces)

> - 다른 필수 소프트웨어(데이터 관리 시스템, 운영체제, 수학 패키지)의 사용과 다른 시스템과의 인터페이스를 지정한다.
> - 각 소프트웨어 제품에 대해 제공되어야 하는 정보
>   1. Name
>   1. Mnemonic
>   1. Specification number
>   1. Version number
>   1. Source
> - 각 인터페이스에 대해 제공되어야 하는 정보
>   1. 소프트웨어와 인터페이스 하는 목적
>   1. 인터페이스에서 사용되는 메시지의 내용과 형식에 관한 정의
>      - 문서화된 인터페이스를 자세하게 설명할 필요는 없지만, 인터페이스를 정의하는 문서에 대한 참조가 필요하다.

##### 2.1.5. 통신 인터페이스(Communications interfaces)

> - 로컬 네트워크 프로토콜과 같은 통신에 대한 다양한 인터페이스를 지정해야 한다.

##### 2.1.6. 메모리 제약사항(Memory constraints)

> - 1차 및 2차 메모리에 적용 가능한 특성과 한계를 명시해야 한다.

##### 2.1.7. 운영(Operations)

> - 지정해야 하는 운영 작업의 종류
>   1. 사용자 그룹의 다양한 운영 모드
>   1. Interactive한 작업 기간과 unattended한 작업의 기간
>   1. 데이터 처리 지원 기능
>   1. 백업 및 복구 동작 > >
>      > - 사용자 인터페이스 항목의 일부로 지정되기도 한다.

##### 2.1.8. 사이트 적용 요건(Site adaption requirements)

> - 특정 사이트, misson, 또는 동작 모드(grid value, safety, etc)에 특화된 어떤 데이터나 초기화 순서에 대한 요구사항을 정의한다.
> - 소프트웨어를 특정 설치에 알맞도록 수정해야 하는 사이트 또는 mission과 관련된 특징을 지정한다.

#### 2.2. 제품 기능(Product functions)

> - 소프트웨어가 수행하는 주요 기능에 대한 요약을 제공한다.
>   - 필요한 기능의 요약은 상위 수준의 명세서로부터 가져올 수 있다.
> - 준수해야 하는 사항
>   1. 고객이나 다른 사람이 봤을 때 기능 목록을 보고 이해할 수 있도록 기능이 구성되어야 한다.
>   1. 텍스트 또는 그래픽을 통해 기능들 사이의 관계를 보여줄 수 있다.
>      - 여기에서 표현되는 다이어그램은 설계를 보여주기 위함이 아니라 변수 사이의 논리적 관계를 단순하게 보여주기 위한 것이다.

#### 2.3. 사용자 특성(User characteristics)

> - 교육 수준, 경험, 기술적 전문 지식을 포함하여 제품의 대상이 되는 사용자의 일반적인 특성을 설명해야 한다.
> - 세부적인 요구사항을 기술하는 데 사용되어서는 안 되고, 세부 요구사항이 나중에 명시되는 이유로 제공되어야 한다.

#### 2.4. 제약사항(Constraints)

> - 개발자의 선택을 제한할 모든 항목에 관한 일반적인 설명을 제공해야 한다.
> - 포함되는 내용
>   1. Regulatory plocies
>   1. Hardware limitations (e.g., signal timing requirements)
>   1. Interfaces to other applications
>   1. Parallel operation
>   1. Audit functions
>   1. Control functions
>   1. Higher-order language requirements
>   1. Signal handshake protocols(e.g., XON-XOFF, ACK-NACK)
>   1. Reliability requirements
>   1. Criticality of the application
>   1. Safety and security considerations

#### 2.5. 가정 및 의존성(Assumptions and dependencies)

> - SRS에서 명시한 요구사항에 영향을 미치는 요소들을 나열해야 한다.
> - 이 요소들은 소프트웨어의 설계 제약사항이 아니라 SRS의 요구사항에 영향을 미칠 수 있는 변경 사항들이다.

#### 2.6. 단계별 요구사항(Apportioning of requirements)

> - 시스템의 향후 버전으로 지연될 수 있는 요구사항을 식별해야 한다.

### 3. 상세 요구사항(Specific requirements)

> - 설계자가 요구사항을 만족하는 시스템을 설계할 수 있도록 모든 요구사항을 상세하게 포함해야 한다.
> - 테스터가 시스템이 위 요건을 충족하는지 테스트해야 한다.
> - 모든 요구사항은 사용자, 운영자, 다른 외부 시스템에 의해 외부적으로 인지할 수 있어야 한다.
> - 이 요구사항에는 시스템에 대한 모든 입력(자극)과 출력(응답) 그리고 입력 또는 출력 지원에 대한 응답으로 실행되는 모든 기능에 관한 설명이 포함되어야 한다.
> - 상세 요구사항을 작성하기 위한 원칙
>   1. 상세 요구사항은 "Characteristics of a good SRS"에 설명한 모든 특성을 준수하도록 작성되어야 한다.
>   1. 상세 요구사항은 관련이 있는 이전 문서들과 상호 참조되어야 한다.
>   1. 모든 요구사항은 고유하게 식별할 수 있어야 한다.
>   1. 가독성을 높이기 위해 요구사항을 구성할 때 주의를 기울여야 한다.

#### 3.1. 외부 인터페이스 요구사항(External interface requirements)

> - 소프트웨어 시스템의 모든 입력과 출력에 관해 자세히 설명해야 한다.
> - "Overall description"의 인터페이스 설명을 보완하되, 그곳의 정보가 반복되지 않아야 한다.
> - 포함되는 외부 인터페이스의 내용 및 형식
>   1. Name of item
>   1. Description of purpose
>   1. Source of input or destination of output
>   1. Valid range, accuracy, and/or tolerance
>   1. Units of measure
>   1. Timing
>   1. Relationships to other inputs/outputs
>   1. Screen formats/organization
>   1. Window formats/organization
>   1. Data formats
>   1. Command formats
>   1. End messages

##### 3.1.1. 사용자 인터페이스(User interfaces)

##### 3.1.2. 하드웨어 인터페이스(Hardware interfaces)

##### 3.1.3. 소프트웨어 인터페이스(Software interfaces)

##### 3.1.4. 통신 인터페이스(Communications interfaces)

#### 3.2. 기능 요구사항(Functional requirements)

> - 기능 요구사항은 소프트웨어가 입력을 처리하고 출력을 생성하는 기본적인 행동을 정의해야 한다.
> - 포함하는 행동들
>   1. Validity checks on the inputs
>   1. Exact sequence of operations
>   1. Responses to abnormal situations, including
>      1. Overflow
>      1. Communication facilities
>      1. Error handling and recovery
>   1. Effect of parameters
>   1. Relationship of outputs to inputs, including
>      1. Input/output sequences
>      1. Formulas for input to output conversion

#### 3.3. 성능 요구사항(Performance requirements)

> - 소프트웨어 또는 소프트웨어와 사람의 상호작용에 대하여 수치화된 정적/동적 요구사항이 명시되어야 한다.
> - 수치화된 정적 요구사항의 종류
>   1. 지원할 터미널 수
>   1. 지원할 동시 접속 사용자 수
>   1. 처리할 정보의 양과 유형작업 및 데이터의 양

#### 3.4. 논리적 데이터베이스 요구사항(Logical database requirements)

> - 데이터베이스에 저장할 정보에 관한 논리적 요구사항을 지정해야 한다.
> - 논리적 요구사항의 종류
>   1. Types of information used by various functuons
>   1. Frequency of use
>   1. Accessing capabilities
>   1. Data entities and their relationships
>   1. Integrity constraints
>   1. Data retention requirements

#### 3.5. 설계 제약사항(Design constraints)

> - 다른 표준, 하드웨어 한계 등에 의해 부과될 수 있는 설계 제약사항을 명시해야 한다.

##### 3.5.1. 표준 준수(Standards compliance)

> - 표준이나 규정에서 파생된 요구사항을 기술한다.
> - 포함될 수 있는 내용
>   1. Report format
>   1. Data naming
>   1. Accounting procedures
>   1. Audit tracing

#### 3.6. 소프트웨어 시스템 속성(Software system attributes)

> - 요구사항으로 사용될 수 있는 소프트웨어의 여러 가지 속성 중 제품이 객관적으로 입증되는 데 필요한 속성을 명시해야 한다.

##### 3.6.1. 신뢰성(Reliability)

> - 배포될 때 소프트웨어 시스템의 필수 신뢰성을 확립하는 데 필요한 요소를 명시해야 한다.

##### 3.6.2. 가용성(Availability)

> - 검사, 복구, 재시작과 같이 전체 시스템에 대해 정의된 가용성 수준을 보장하는 데 필요한 요소가 지정되어야 한다.

##### 3.6.3. 보안성(Security)

> - 실수 또는 악의적인 접근, 사용, 수정, 파괴, 공개로부터 소프트웨어를 보호하기 위한 요소를 명시해야 한다.
> - 포함될 수 있는 요구사항
>   1. Utilize certain cryptographical techinques
>   1. Keep specific log or history data sets
>   1. Assign certain functions to diffrent modules
>   1. Restrict communication between some areas of the program
>   1. Check data integrity for critical variables

##### 3.6.4. 유지 보수성(Maintainability)

> - 소프트웨어 자체를 쉽게 유지 보수할 수 있는 속성을 명시해야 한다.
> - 모듈화, 인터페이스, 복잡성 등과 관련된 요구사항이 있을 수 있다.

##### 3.6.5. 이식성(Portability)

> - 소프트웨어를 다른 호스트 시스템 또는 운영체제로 쉽게 이식할 수 있는 속성을 명시해야 한다.
> - 포함될 수 있는 속성의 종류
>   1. Percentage of components with host-dependent code
>   1. Percentage of code that is dependent
>   1. Use of a proven portable language
>   1. Use of a particular compiler or language subset
>   1. Use of a particular operation system

#### 3.7. 상세 요구사항의 구성(Organizing the specific requirements)

> - 시스템의 세부 요구사항은 광범위한 경향이 있으므로 자료를 이해하기에 가장 적합한 방식으로 구성하는 방법을 세심하게 고려해야 한다.

##### 3.7.1. 시스템 모드(System mode)

> - 일부 시스템은 운영 모드에 따라 상당히 다르게 작동할 수 있다.
>   - 예: 제어 시스템은 연습, 일반, 긴급 등의 여러 모드가 있을 수 있다.
> - 모드를 기준으로 구성하는 경우 [A.1](#a1-template-of-srs-section-3-organized-by-mode-version-1)과 [A.2](#a2-template-of-srs-section-3-organized-by-mode-version-2)를 사용한다.

##### 3.7.2. 사용자 부류(User class)

> - 일부 시스템은 사용자의 부류에 따라 서로 다른 기능을 제공한다.
>   - 예: 엘리베이터 제어 시스템은 승객, 정비원, 소방관에게 서로 다른 기능을 제공한다.
> - 사용자 부류에 따라 구성하는 경우 [A.3](#a3-template-of-srs-section-3-organized-by-user-class)를 사용한다.

##### 3.7.3. 객체(Objects)

> - 객체는 시스템에서 현실 세계와 대응되는 개체이다.
> - 객체에는 각 각체의 상태(attributes) 및 객체의 행위(functions)가 포함된다.
>   - 이러한 행위는 services, methods, processes라고도 한다.
> - 객체에 따라 구성하는 경우 [A.4](#a4-template-of-srs-section-3-organized-by-object)를 사용한다.

##### 3.7.4. 특징(Feature)

> - 특징은 시스템에 의해 외부적으로 요구되는 서비스로서 원하는 결과를 얻기 위해서는 입력이 필요할 수도 있다.
>   - 예: 전화 시스템에서 특징들은 지역 내 통화, 착신 전환, 화상 통화를 포함한다.
> - 일반적으로 각 특징은 자극-반응의 순서로 설명된다.
> - 특징에 따라 구성하는 경우 [A.5](#a5-template-of-srs-section-3-organized-by-feature)를 사용한다.

##### 3.7.5. 자극(Stimulus)

> - 일부 시스템은 자극의 측면에서 기능들을 설명할 때 가장 잘 구성될 수 있다.
>   - 예: 항공기 자동 착륙 시스템은 동력 상실, 윈드시어 등을 위해 구성될 수 있다.
> - 자극에 따라 구성하는 경우 [A.6](#a6-template-of-srs-section-3-organized-by-stimulus)를 사용한다.

##### 3.7.6. 반응(Response)

> - 일부 시스템은 반응 생성을 지원하는 기능들을 설명할 때 가장 잘 구성될 수 있다.
>   - 예: 직원 시스템의 기능은 급여 생성과 관련된 기능들, 직원 목록 생성과 관련된 기능 등으로 구성될 수 있다.
> - 반응에 따라 구성하는 경우 [A.6](#a6-template-of-srs-section-3-organized-by-stimulus)를 사용한다.

##### 3.7.7. 기능 계층(Functional hierarchy)

> - 위 조직 체계 중 유용한 수단이 없다면, 전체 기능은 공통 입력, 공통 출력 또는 공통 내부 데이터 접근에 의해 구성된 기능의 계층으로 구성될 수 있다.
> - 데이터 흐름 다이어그램과 데이터 사전을 사용하여 기능과 데이터 사이의 관계를 보여줄 수 있다.
> - 기능 계층별로 구성하는 경우 [A.7](#a7-template-of-srs-section-3-organized-by-functional-hierarchy)을 사용한다.

##### 3.7.8. Additional comments

> - 새로운 SRS를 고려할 때 두 가지 이상의 조직 기법이 적합할 수 있다.
>   - 이 경우 명세에 따른 시스템의 상세 요구사항에 맞춘 다중 계층의 요구사항을 구성한다.
> - 사용자 분류와 기능을 결합하는 구성은 [A.8](#a8-template-of-srs-section-3-showing-multiple-organizations)을 참고한다.

### 4. 추가 정보(Supporting information)

> - 추가 정보는 SRS를 더욱 사용하기 쉽게 한다.

#### 4.1. Table of contents and index(목차와 인덱스)

> - 목차와 인덱스는 매우 중요하므로 일반적인 compositional practices를 따라야 한다.

#### 4.2. 부록(Appendixes)

> - 부록은 SRS의 일부로 간주하지 않으며, 항상 필요한 것도 아니다.
> - 부록이 포함하는 내용
>   1. Sample input/output formats, descriptions of cost analysis studies, or results of user surveys
>   1. Supporting or background information that can help the readers of the SRS
>   1. A description of the problems to be solved by the software
>   1. Special packaging instructions for the code and the media to mmet security, export, initial loading, or other requirements > >
>      > - 부록이 포함된 경우 SRS는 부록이 요구사항의 일부로 간주하는지 명시해야 한다.

## Annex

### A. SRS templates

#### A.1. Template of SRS Section 3 organized by mode: Version 1

1. Specific requirements
   1. External interface requirements
      1. User interfaces
      1. Hardware interfaces
      1. Software interfaces
      1. Communication interfaces
   1. Functional requirements
      1. Mode 1
         1. Functional requirements 1.1
         1. ...
         1. Functional requirements 1.n
      1. Mode 2
         1. ...
   1. Performance requirements
   1. Design constraints
   1. Software system attributes
   1. Other requirements

#### A.2. Template of SRS Section 3 organized by mode: Version 2

1. Specific requirements
   1. Functional requirements
      1. Mode 1
         1. External interface requirements
            1. User interfaces
            1. Hardware interfaces
            1. Software interfaces
            1. Communication interfaces
         1. Functional requirements
            1. Functional requirements 1
            1. ...
            1. Functional requirements n
      1. Mode 2
         1. ...
   1. Design constraints
   1. Software system attributes
   1. Other requirements

#### A.3. Template of SRS Section 3 organized by user class

1. Specific requirements
   1. External interface requirements
      1. User interfaces
      1. Hardware interfaces
      1. Software interfaces
      1. Communication interfaces
   1. Functional requirements
      1. User class 1
         1. Functional requirements 1.1
         1. ...
         1. Functional requirements 1.n
      1. User class 2
         1. ...
   1. Performance requirements
   1. Design constraints
   1. Software system attributes
   1. Other requirements

#### A.4. Template of SRS Section 3 organized by object

1. Specific requirements
   1. External interface requirements
      1. User interfaces
      1. Hardware interfaces
      1. Software interfaces
      1. Communication interfaces
   1. Classes/Objects
      1. Class/Object 1
         1. Attributes
            1. Attribute 1
            1. ...
            1. Attribute n
         1. Functions
            1. Functional requirements 1.1
            1. ...
            1. Functional requirements 1.n
         1. Messages
      1. Class/Object 2
         1. ...
   1. Performance requirements
   1. Design constraints
   1. Software system attributes
   1. Other requirements

#### A.5. Template of SRS Section 3 organized by feature

1. Specific requirements
   1. External interface requirements
      1. User interfaces
      1. Hardware interfaces
      1. Software interfaces
      1. Communication interfaces
   1. System features
      1. System feature 1
         1. Introduction/Purpose of feature
         1. Stimulus/Response sequence
         1. Associated functional requirements
            1. Functional requirements 1
            1. ...
            1. Functional requirements n
      1. System feature 2
         1. ...
   1. Performance requirements
   1. Design constraints
   1. Software system attributes
   1. Other requirements

#### A.6. Template of SRS Section 3 organized by stimulus

1. Specific requirements
   1. External interface requirements
      1. User interfaces
      1. Hardware interfaces
      1. Software interfaces
      1. Communication interfaces
   1. Functional requirements
      1. Stimulus 1
         1. Functional requirements 1
         1. ...
         1. Functional requirements n
      1. Stimulus 2
         1. ...
   1. Performance requirements
   1. Design constraints
   1. Software system attributes
   1. Other requirements

#### A.7. Template of SRS Section 3 organized by functional hierarchy

1. Specific requirements
   1. External interface requirements
      1. User interfaces
      1. Hardware interfaces
      1. Software interfaces
      1. Communication interfaces
   1. Functional requirements
      1. Information flows
         1. Data flow diagram 1
            1. Data entities
            1. Pertinents processes
            1. Topology
         1. Data flow diagram 2
            1. ...
      1. Process descriptions
         1. Process 1
            1. Input data entities
            1. Algorithm or formula of process
            1. Affected data entities
         1. Process 2
            1. ...
      1. Data construct specifications
         1. Construct 1
            1. Record type
            1. Constituent fields
         1. Construct 2
            1. ..
      1. Data dictionary
         1. Data elemnet 1
            1. Name
            1. Representation
            1. Units/Format
            1. Precision/Accuracy
            1. Range
         1. Data element 2
            1. ...
   1. Performance requirements
   1. Design constraints
   1. Software system attributes
   1. Other requirements

#### A.8. Template of SRS Section 3 showing multiple organizations

1. Specific requirements
   1. External interface requirements
      1. User interfaces
      1. Hardware interfaces
      1. Software interfaces
      1. Communication interfaces
   1. Functional requirements
      1. User class 1
         1. Feature 1.1
            1. Introduction/Purpose of feature
            1. Stimulus/Response sequence
            1. Associated functional requirements
         1. ...
         1. Feature 1.n
            1. ...
      1. User class 2
         1. ...
   1. Performance requirements
   1. Design constraints
   1. Software system attributes
   1. Other requirements
