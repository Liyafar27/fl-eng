https://github.com/p0dyakov/flutter_interview/assets/80569772/68dccc7f-b4f2-4eca-932a-8f9fe5559b5f

**Repositories:**  
[Flutter Interview](https://github.com/p0dyakov/flutter_interview) •  
[Flutter Roadmap](https://github.com/p0dyakov/flutter_roadmap) •  
[Flutter Articles](https://github.com/p0dyakov/flutter_articles) •  
[Flutter Best Packages](https://github.com/p0dyakov/flutter_best_packages) •  
[Flutter Tools](https://github.com/p0dyakov/flutter_tools)

---

## Table of Contents

- [General](#general)  
- [OOP](#oop)  
- [SOLID](#solid)  
- [Git Flow](#git-flow)  
- [Data Structures](#data-structures)  
- [Imperative vs Declarative Programming](#imperative-vs-declarative-programming)  
- [Stack and Heap](#stack-and-heap)  
- [DAO, DTO, VO, BO](#dao-dto-vo-bo)  
- [DI and Service Locator](#di-and-service-locator)  
- [Dart](#dart)  
  - [final and const](#final-and-const)  
  - [factory vs const constructor](#factory-vs-const-constructor)  
  - [JIT and AOT](#jit-and-aot)  
  - [Hot Restart and Hot Reload](#hot-restart-and-hot-reload)  
  - [HashCode](#hashcode)  
  - [Extension Methods](#extension-methods)  
  - [Mixin](#mixin)  
  - [Sound Null Safety](#sound-null-safety)  
  - [Type System](#type-system)  
  - [late](#late)  
  - [Generics](#generics)  
  - [Dart VM](#dart-vm)  
  - [Zones](#zones)  
  - [Types of Errors](#types-of-errors)  
  - [Naming Rules](#naming-rules)  
  - [Never](#never)  
  - [Covariant](#covariant)  
  - [Annotations](#annotations)  
  - [int8, uint8, int16, uint16...](#int8-uint8-int16-uint16)  
  - [Future](#future)  
  - [Future Constructors](#future-constructors)  
  - [await under the hood](#await-under-the-hood)  
  - [Event Loop & Microtasks](#event-loop--microtasks)  
  - [Completer](#completer)  
  - [Stream](#stream)  
  - [Generators (`sync*` / `async*`)](#generators-sync--async)  
  - [Multithreading in Dart](#multithreading-in-dart)  
  - [Isolate](#isolate)  
  - [compute](#compute)  
  - [Multithreading Issues](#multithreading-issues)  
- [Flutter](#flutter)  
  - [StatelessWidget and StatefulWidget](#statelesswidget-and-statefulwidget)  
  - [Stateful Widget Lifecycle](#stateful-widget-lifecycle)  
  - [`mounted` and `addPostFrameCallback`](#mounted-and-addpostframecallback)  
  - [`WidgetsBindingObserver`](#widgetsbindingobserver)  
  - [`BuildContext`](#buildcontext)  
  - [`InheritedWidget`](#inheritedwidget)  
  - [`Provider` vs `InheritedWidget`](#provider-vs-inheritedwidget)  
  - [Trees (Widget / Element / Render)](#trees-widget--element--render)  
  - [Widget](#widget)  
  - [Element](#element)  
  - [RenderObject](#renderobject)  
  - [Types of Widgets](#types-of-widgets)  
  - [Types of Elements](#types-of-elements)  
  - [Element Lifecycle](#element-lifecycle)  
  - [GlobalKey and LocalKey](#globalkey-and-localkey)  
  - [Flutter Runtime Architecture](#flutter-runtime-architecture)  
  - [Execution Model](#execution-model)  
  - [`CustomPaint` and `CustomPainter`](#custompaint-and-custompainter)  
  - [`WidgetsFlutterBinding`](#widgetsflutterbinding)  
  - [Bindings](#bindings)  
  - [Platform Channels](#platform-channels)  
  - [Build Modes](#build-modes)  
  - [Package vs Plugin vs FFI Plugin](#package-vs-plugin-vs-ffi-plugin)  
  - [Animations](#animations)  
    - [Animation Stages](#animation-stages)  
    - [Types of Animations](#types-of-animations)  
    - [Tween](#tween)  
    - [`vsync` and `Ticker`](#vsync-and-ticker)  
  - [Frame Construction](#frame-construction)  
  - [Layout Calculation](#layout-calculation)  
  - [`BuildOwner` and `PipelineOwner`](#buildowner-and-pipelineowner)  
  - [Garbage Collector](#garbage-collector)  
  - [Task Runners](#task-runners)  
  - [`MediaQuery` — beyond size](#mediaquery--beyond-size)  
  - [`LayoutBuilder` vs `MediaQuery`](#layoutbuilder-vs-mediaquery)  
  - [`FutureBuilder` internals](#futurebuilder-internals)  
  - [`AppLifecycleState` — full breakdown](#applifecyclestate--full-breakdown)  
  - [Slivers — advanced](#slivers--advanced)  
- [Architecture](#architecture)  
  - [Clean Architecture](#clean-architecture)  
  - [State Management](#state-management)  
  - [Dependency Injection](#dependency-injection)  
  - [Architectural Patterns](#architectural-patterns)  
  - [Navigation](#navigation)  
- [Databases](#databases)  
- [Testing](#testing)  
  - [Types of Tests](#types-of-tests)  
  - [TDD](#tdd)  
- [Development Patterns](#development-patterns)  
- [Advanced Topics](#advanced-topics)  
  - [Tree Shaking](#tree-shaking)  
  - [Code-splitting (Deferred Components)](#code-splitting-deferred-components)  
  - [Internationalization (`gen-l10n`)](#internationalization-gen-l10n)  
  - [`FlutterActivity` responsibilities](#flutteractivity-responsibilities)  
  - [Accessibility Considerations](#accessibility-considerations)  
  - [Obfuscation](#obfuscation)  
  - [MITM Protection](#mitm-protection)  

---

## General

[↑ Вверх](#table-of-contents)

## OOP

`Object-oriented programming` — programming paradigm based on objects (instances of classes), with key principles:  
- **Abstraction**: modeling via abstract classes/interfaces  
- **Encapsulation**: bundling data + methods in a class  
- **Inheritance**: deriving new classes from existing ones  
- **Polymorphism**: using objects via shared interface, regardless of concrete type.

[↑ Вверх](#table-of-contents)

## SOLID

- **SRP**: A class should have only *one reason to change*.  
- **OCP**: Entities should be *open for extension, closed for modification*.  
- **LSP**: Subtypes must be *substitutable* for their base types.  
- **ISP**: Clients shouldn’t depend on interfaces they don’t use.  
- **DIP**: Depend on *abstractions*, not concretions.

[↑ Вверх](#table-of-contents)

## Git Flow

| Stage | Action |
|-------|--------|
| **Feature** | Branch `feature/x` from `develop` → merge back → delete |
| **Release** | Branch `release/vX.X` from `develop` → merge to `master` (tag) + `develop` → delete |
| **Hotfix** | Branch `hotfix/x` from `master` → merge to `master` + `develop` → delete |

[↑ Вверх](#table-of-contents)

## Data Structures

- `Array`, `Stack` (LIFO), `Queue` (FIFO), `Linked List`, `Tree`, `Graph`, `Hash Table`.

[↑ Вверх](#table-of-contents)

## Imperative vs Declarative Programming

- **Imperative**: *How* to achieve result (step-by-step).  
- **Declarative**: *What* result is needed (e.g. Flutter widgets).

[↑ Вверх](#table-of-contents)

## Stack and Heap

- **Stack**: LIFO, fast, fixed size (local vars, return addresses).  
- **Heap**: dynamic alloc, slower, GC-managed (objects, closures).

[↑ Вверх](#table-of-contents)

## DAO, DTO, VO, BO

- `DAO`: Data access (abstraction over DB).  
- `DTO`: Data transfer between layers (no logic).  
- `VO`: Immutable value object (`==`, `hashCode`).  
- `BO`: Business logic entity.

[↑ Вверх](#table-of-contents)

## DI and Service Locator

- **DI** (preferred): inject via constructor — testable, explicit deps.  
- **Service Locator** (anti-pattern): global access — hides deps, hard to test.

[↑ Вверх](#table-of-contents)

## Dart

[↑ Вверх](#table-of-contents)

### final and const

- `final`: runtime constant — new instance per usage.  
- `const`: compile-time constant — single shared instance (`identical`).

[↑ Вверх](#table-of-contents)

### factory vs const constructor

- `const constructor`: all fields `final`; creates *compile-time constant* (shared instance).  
- `factory constructor`: returns *existing or new* instance (e.g. singleton, pool, subtype). Cannot use `this`.

```dart
// const: same instance
const p1 = Point(1, 2);
const p2 = Point(1, 2); // identical(p1, p2) → true

// factory: cached instance
class Logger {
  static final _inst = Logger._();
  factory Logger() => _inst;
  Logger._();
}# fl-eng
