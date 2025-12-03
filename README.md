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

```
// const: same instance
const p1 = Point(1, 2);
const p2 = Point(1, 2); // identical(p1, p2) → true

// factory: cached instance
class Logger {
  static final _inst = Logger._();
  factory Logger() => _inst;
  Logger._();
}#
```

## JIT and AOT
JIT (Debug)
AOT (Release/Profile)
When
Runtime
Build time
Speed
Slower execution
Faster startup & exec
Hot Reload
✅
❌
Size
Larger
Optimized (tree shaking)
Obfuscation
Harder
Supported
↑ Вверх

Hot Restart and Hot Reload
Hot Reload: injects code, rebuilds tree, preserves state (initState not called).
Hot Restart: full app restart, resets state (main, initState called).
↑ Вверх

HashCode
Used in Set, Map. Must satisfy:

a == b ⇒ a.hashCode == b.hashCode
Prefer Object.hash(...) over manual impl.
↑ Вверх

Extension Methods
Add functionality to existing types without inheritance:

↑ Вверх

Mixin
Reusable behavior via with. No constructors. on restricts usage.


↑ Вверх

Sound Null Safety
Non-nullable by default (int, not int?).
Compile-time guarantee: no Null dereference.
late: non-nullable, init on first access.
required: named param must be provided.
↑ Вверх

Type System
Root: Object? (nullable) → Object (non-nullable).
Never: bottom type — no instance possible (e.g. throw).
↑ Вверх

late
Defers initialization of non-nullable field:

⚠️ Risk: LateInitializationError if read before assignment.

↑ Вверх

Generics
Parameterized types (List<T>) — type-safe, reduce duplication.

↑ Вверх

Dart VM
Runtime with: execution env, GC, native libs, debugger, profiler, ARM simulator.

↑ Вверх

Zones
Error-handling scopes:

Catch unhandled errors (prevent app crash)
Zone-local storage
Override print, scheduleMicrotask
Hooks on entry/exit.
↑ Вверх

Types of Errors
Category
Examples
Exception
TimeoutException, HttpException, FormatException
Error (non-recoverable)
AssertionError, OutOfMemoryError, NoSuchMethodError
↑ Вверх

Naming Rules
lowerCamelCase: vars, funcs
UpperCamelCase: classes, enums
snake_case: files
↑ Вверх

Never
Uninhabited type — function returning Never never returns normally (e.g. throw).

↑ Вверх

Covariant
Allows subtype to narrow parameter type:

dart
12
↑ Вверх

Annotations
Metadata (@override, @required). Any class with const constructor can be annotation.

↑ Вверх

int8, uint8, int16, uint16...
Used in dart:ffi. Sizes fixed across platforms.

Specifier
Bytes
Min
Max
int8
1
-128
127
uint8
1
0
255
int16
2
-32,768
32,767
uint16
2
0
65,535
↑ Вверх

Future
Represents async single value. States: pending → completed (value/error).

↑ Вверх

Future Constructors
Constructor
Use case
Future(() => ...)
Async via Timer.run
Future.delayed(d, () => ...)
Delayed execution
Future.error(e)
Pre-failed future
Future.microtask(() => ...)
Next microtask queue
Future.sync(() => ...)
Execute now, wrap in Future
Future.value(x)
Completed with value
↑ Вверх

await under the hood
dart
123
↑ Вверх

Event Loop & Microtasks
Two queues (FIFO):

Microtask queue: scheduleMicrotask, Future.then — higher priority.
Event queue: I/O, timers, gestures — processed after microtasks.
→ Ensures async continuations run before next event.

↑ Вверх

Completer
Manually complete a Future (e.g. bridge callback APIs):

dart
123
↑ Вверх

Stream
Async sequence of events. Two types:

Single-subscription: one listener (e.g. file read).
Broadcast: many listeners (e.g. UI events). Use StreamController.broadcast().
↑ Вверх

Generators (sync* / async*)
sync* → Iterable (sync sequence).
async* → Stream (async sequence).
Use yield, yield*.
↑ Вверх

Multithreading in Dart
Dart is single-threaded, but supports concurrency via:

Isolates (separate heaps, no shared memory)
Event loop + async/await (non-blocking I/O)
↑ Вверх

Isolate
Independent worker with own heap, event loop. Communicate via SendPort/ReceivePort.

Isolate.spawn(entryPoint, message)
Data must be primitive/serializable (no refs).
Isolate.exit(sendPort, value) → send + terminate; sendPort.send() → send only.
↑ Вверх

compute
Convenience for one-off isolate work:

dart
1
⚠️ Not for frequent calls (isolate spawn overhead).

↑ Вверх

Multithreading Issues
Deadlock, Race conditions, Lock Contention, Livelock.
↑ Вверх

Flutter
↑ Вверх

StatelessWidget and StatefulWidget
StatelessWidget: immutable, rebuilds entirely on parent change.
StatefulWidget: mutable state in State; rebuilds via setState.
↑ Вверх

Stateful Widget Lifecycle
dart
123
↑ Вверх

mounted and addPostFrameCallback
mounted: bool, true iff State is in tree. Always check before setState in async callbacks.
dart
123
fetchData().then((v) {
  if (mounted) setState(() => _data = v);
});
WidgetsBinding.instance.addPostFrameCallback: runs after current frame renders (e.g. show SnackBar right after build).
↑ Вверх

WidgetsBindingObserver
Listen to app-level events:

dart
12345678910111213
Use for:

Pause/resume background tasks
Save state on paused
Adjust for textScaleFactor changes.
↑ Вверх

BuildContext
Interface to Element. Used to:

Find ancestors: context.findAncestorWidgetOfExactType<T>()
Get inherited data: Theme.of(context), MediaQuery.of(context)
Access render object: (context as Element).renderObject
→ O(1) lookup for InheritedWidget via Element._inheritedWidgets hash map.

↑ Вверх

InheritedWidget
Efficiently propagate data down tree. Child uses context.dependOnInheritedWidgetOfExactType<T>() to:

Get data
Auto-rebuild when data changes (if updateShouldNotify returns true)
dart
1234567
↑ Вверх

Provider vs InheritedWidget
InheritedWidget
Provider
Boilerplate
High (subclass + of)
Low (Provider<T>, context.watch<T>())
Features
Basic propagation
ChangeNotifier, Stream, Future, scoping, error handling
Use case
Simple, no deps
Recommended for apps
→ Provider is built on top of InheritedWidget.

↑ Вверх

Trees (Widget / Element / Render)
Widget tree: immutable config (declarative UI).
Element tree: mutable instances (bridge, manages lifecycle).
Render tree: layout/paint (geometry, hit testing).
↑ Вверх

Widget
Immutable descriptor. == compares runtimeType + key. Not a tree — just config.

↑ Вверх

Element
Mutable instance of widget at location. Manages:

Widget ↔ RenderObject binding
State lifecycle
InheritedWidget lookup cache
Rebuild scheduling
↑ Вверх

RenderObject
Mutable, does layout/paint. Key properties:

parentData: layout hints from parent
constraints: size limits from parent
markNeedsLayout(), markNeedsPaint()
isRepaintBoundary: isolate paint (e.g. animations)
↑ Вверх

Types of Widgets
Category
Role
Examples
Proxy
Provide data to descendants
InheritedWidget, NotificationListener
Renderer
Direct layout/paint control
Padding, Align, Opacity, CustomPaint
Component
High-level composition
Text, Button, Scaffold
↑ Вверх

Types of Elements
ComponentElement: for StatelessWidget/StatefulWidget — calls build().
RenderObjectElement: for render widgets — owns RenderObject.
SingleChildRenderObjectElement (Padding)
MultiChildRenderObjectElement (Column)
SliverMultiBoxAdaptorElement (SliverList)
↑ Вверх

Element Lifecycle
Widget.createElement() → Element.mount(parent)
Child elements created, render objects linked
On widget change: if runtimeType+key match → update(); else → unmount + new element
On removal: deactivate() → (inactive ≤ 1 frame) → unmount()
Reinsertion (e.g. GlobalKey): activate() → reattach render object.
↑ Вверх

GlobalKey and LocalKey
GlobalKey: unique app-wide; preserves state on move (e.g. form).
LocalKey: unique among siblings:
ValueKey: stable identity (e.g. list item id)
ObjectKey: identity tied to object
UniqueKey: always new (force reset)
↑ Вверх

Flutter Runtime Architecture
12345
[App Code (Dart)]  
       ↓ WidgetsBinding  
[Flutter Framework] ←→ [Flutter Engine (C++, Skia/Impeller)]  
       ↓ Platform Channels  
[Platform (Android/iOS)]
↑ Вверх

Execution Model
main() runs
Event loop starts (microtask + event queues)
runApp() → WidgetsBinding.attachRootWidget()
First frame scheduled → beginFrame → drawFrame → render.
↑ Вверх

CustomPaint and CustomPainter
CustomPaint: widget embedding CustomPainter.
CustomPainter: logic in paint(Canvas, Size).
shouldRepaint(covariant old): true → repaint on setState.
Use RepaintBoundary to cache complex drawings.
dart
123456
class _LinePainter extends CustomPainter {
  @override void paint(Canvas canvas, Size size) {
    canvas.drawLine(Offset.zero, Offset(size.width, size.height), Paint());
  }
  @override bool shouldRepaint(_LinePainter old) => false;
}
↑ Вверх

WidgetsFlutterBinding
Glue framework ↔ engine. Mixins:

GestureBinding
ServicesBinding
SchedulerBinding
PaintingBinding
SemanticsBinding
RendererBinding
WidgetsBinding
↑ Вверх

Bindings
Binding
Responsibility
SchedulerBinding
Frame scheduling (onBeginFrame, onDrawFrame)
RendererBinding
Render tree ↔ engine sync
WidgetsBinding
Widget tree lifecycle, addPostFrameCallback
↑ Вверх

Platform Channels
Async Dart ↔ native (Java/Kotlin/Swift) comms. Types:

MethodChannel: call native methods
EventChannel: receive native streams
BasicMessageChannel: raw binary (e.g. StandardMessageCodec)
⚠️ Only main isolate.

↑ Вверх

Build Modes
Mode
Compiler
Use
debug
JIT
Development (hot reload)
profile
AOT
Performance profiling
release
AOT
Production (obfuscation, tree shaking)
↑ Вверх

Package vs Plugin vs FFI Plugin
Type
Dart-only
Native code
Use
Package
✅
❌
Utilities, widgets
Plugin
✅
✅ (platform channels)
Hardware access
FFI Plugin
✅
✅ (Dart FFI + C/C++)
High-perf native (no channel overhead)
↑ Вверх

Animations
Animation Stages
AnimationController(vsync: this)
vsync → SchedulerBinding → engine onBeginFrame
Engine → onDrawFrame → controller ticks
addListener → setState → rebuild.
Types of Animations
Tween: predefined start/end (TweenAnimationBuilder)
Physics-based: simulate real motion (SpringSimulation).
Tween
Interpolates between values: Tween(begin: 0.0, end: 300.0).animate(controller).

vsync and Ticker
vsync: prevents off-screen animation jank (no frames when app backgrounded).
TickerProviderStateMixin (single) vs TickerProviderStateMixin (multiple).
SingleTickerProviderStateMixin preferred (lighter).
↑ Вверх

Frame Construction
External event (e.g. setState) → scheduleFrame()
Engine → onBeginFrame → run tickers (animations)
Engine → onDrawFrame → layout → paint → scene
post-frame callbacks → done.
↑ Вверх

Layout Calculation
Constraints flow down (parent → child)
Sizes flow up (child → parent)
Parent positions children.
↑ Вверх

BuildOwner and PipelineOwner
BuildOwner: manages element tree rebuilds (scheduleBuildFor, buildScope).
PipelineOwner: manages render tree updates (layout, paint, compositing).
↑ Вверх

Garbage Collector
Two generations:

Young: Scavenge (copy live → survivor space)
Old: Mark-sweep-compact (parallel mark, concurrent sweep).
↑ Вверх

Task Runners
Runner
Runs on
Purpose
Platform
Main native thread
Plugin code (Android: main thread)
UI
Dart isolate
Dart code, build/layout
Raster
GPU thread (CPU-bound!)
Skia/Impeller rasterization
IO
Background
Asset loading, I/O
↑ Вверх

MediaQuery — beyond size
Use for:

textScaleFactor (accessibility)
platformBrightness (light/dark mode)
highContrast, disableAnimations (a11y)
viewInsets (keyboard avoidance)
→ Prefer MediaQuery over hardcoded sizes.

↑ Вверх

LayoutBuilder vs MediaQuery
LayoutBuilder
MediaQuery
Input
Parent’s layout constraints
Device/screen properties
When rebuild?
Parent layout changes
Orientation, keyboard, locale, a11y changes
Use case
Responsive to container size (e.g. grid columns)
Responsive to device (e.g. phone vs tablet)
Example:

dart
1234
↑ Вверх

FutureBuilder internals
Avoid rebuilding Future in build() (creates new future → resets state).
Pass pre-constructed Future:
dart
123456
States: ConnectionState.waiting → snapshot.hasData / hasError.
↑ Вверх

AppLifecycleState — full breakdown
State
Meaning
resumed
Foreground, interactive
inactive
Paused (e.g. incoming call), may resume
paused
Background (Android), suspended (iOS)
detached
Engine running, but no UI attached (e.g. during navigation pop, or headless isolate)
→ Handle paused/detached to pause expensive tasks.

↑ Вверх

Slivers — advanced
Slivers = lazy, scroll-aware render objects.

SliverAppBar: collapsible app bar
SliverPersistentHeader: sticky headers (pinned: true)
SliverGrid, SliverList: lazy grids/lists
SliverFillRemaining: fill remaining space
SliverToBoxAdapter: wrap non-sliver in sliver
Use CustomScrollView to combine slivers.

dart
1234567
↑ Вверх

Architecture
↑ Вверх

Clean Architecture
Layers:

Data: sources (API, cache), repos
Domain: entities, use cases (business logic)
Presentation: UI, state (BLoC, ViewModels)
→ Dependencies flow inward (Domain ← Presentation; Domain ← Data).

↑ Вверх

State Management
Approach
Pros
Cons
Use
BLoC
Predictable, testable, scalable
Boilerplate, steep learning
Complex apps (your preference ✅)
Provider
Lightweight, Flutter-integrated
Limited for complex logic
Medium apps
Vanilla setState
Simple
Unscalable, violates SRP
Prototypes, tiny widgets
→ You prefer BLoC + Dio + no local DB.

↑ Вверх

Dependency Injection
Manual DI: constructor injection (explicit, no framework).
get_it / Riverpod: service locator / provider-based.
→ Avoid global singletons.
↑ Вверх

Architectural Patterns
Pattern
Flow
Use
MVVM
View ←→ ViewModel ←→ Model
Data binding (Flutter: StreamBuilder)
MVP
View → Presenter → Model → View
Testable UI logic
BLoC
UI → Sink(event) → BLoC → Stream(state) → UI
Your stack ✅
↑ Вверх

Navigation
Navigator 2.0 (declarative, complex routing)
go_router (recommended): deep links, route guards, path params
auto_route: codegen, type-safe, protected routes.
↑ Вверх

Databases
DB
Pros
Cons
Use
Hive
Pure Dart, fast, codegen
No relations, in-memory
Small configs, caches
SharedPrefs
Simple, sync read
Primitive only, platform quirks
Settings, flags
Drift
SQL, relations, all platforms
Boilerplate, slower
Complex data, offline
→ You avoid local DBs — prefer remote + cache.

↑ Вверх

Testing
Types of Tests
Type
Scope
Tools
Unit
Single function/class
test
Widget
Single widget
flutter_test, WidgetTester
Integration
Full app flow
integration_test, flutter_driver
↑ Вверх

TDD
Write failing test
Implement minimal code to pass
Refactor
→ Ensures test coverage, design clarity.
↑ Вверх

Development Patterns
Generative: Factory, Builder, Singleton
Structural: Adapter, Decorator, Proxy
Behavioral: Observer, Strategy, Command
↑ Вверх

Advanced Topics
Tree Shaking
Removes unused code at compile time (AOT).

Works on static analysis — avoid dynamic calls (noSuchMethod, reflection).
Effective in Dart due to strong typing.
↑ Вверх

Code-splitting (Deferred Components)
Split APK/AAB into on-demand modules (e.g. admin panel, onboarding).

Android: Play Feature Delivery
iOS: On-Demand Resources
deferred keyword + loadLibrary().
↑ Вверх

Internationalization (gen-l10n)
Modern Flutter way (replaces intl):

Define .arb files: app_en.arb, app_ru.arb
flutter gen-l10n → generates AppLocalizations
Use: AppLocalizations.of(context).helloWorld
→ Type-safe, tooling support.

↑ Вверх

FlutterActivity responsibilities
On Android, FlutterActivity handles:

Launch screen display
Status bar configuration
Dart entrypoint (main) selection
Initial route
Transparent rendering
Instance state save/restore.
↑ Вверх

Accessibility Considerations
Semantics() widget: label, hint, traits
Sufficient contrast (MediaQuery.platformBrightness)
Test with TalkBack / VoiceOver
Avoid Column(children: [Icon(), Text()]) — wrap in Semantics(container: true).
↑ Вверх

Obfuscation
flutter build --obfuscate --split-debug-info=...
Renames classes/methods; debug symbols stored separately.
Does not encrypt strings or logic — combine with R8/ProGuard.
↑ Вверх

MITM Protection
HTTPS only + certificate pinning (dio + dio_http2_adapter)
Validate certs (avoid badCertificateCallback: (_) => true)
Use secure DNS (DoH/DoT).
Never log sensitive data.



