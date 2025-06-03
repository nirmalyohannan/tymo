# Tymo Project Rules

## Project Architecture

### Clean Architecture Layers

1. **Presentation Layer**:

   - Contains UI components (widgets, pages)
   - Handles user interactions
   - Uses BLoC/Cubit for state management

2. **Domain Layer**:

   - Contains business logic
   - Defines entities and use cases
   - Independent of frameworks

3. **Data Layer**:
   - Implements repositories
   - Handles data sources (Firebase, local storage)
   - Converts models to/from entities

## Feature-Based Structure

### Folder Organization

```
lib/
├── features/
│   ├── feature1/
│   │   ├── data/
│   │   │   ├── datasources/
│   │   │   ├── models/
│   │   │   └── repositories/
│   │   ├── domain/
│   │   │   ├── entities/
│   │   │   ├── repositories/
│   │   │   └── usecases/
│   │   └── presentation/
│   │       ├── bloc/
│   │       ├── pages/
│   │       └── widgets/
│   └── feature2/
│       └── ...
├── core/
│   ├── error/
│   ├── network/
│   ├── theme/
│   ├── usecases/
│   └── utils/
└── main.dart
```

### Firebase Integration Rules

1. All Firebase services accessed through repository interfaces
2. Firebase-specific code isolated to data layer
3. Use `firebase_options.dart` for initialization
4. Follow Firebase security rules in console

### Coding Standards

1. Follow official Flutter style guide
2. Use BLoC pattern for complex state
3. Widgets should be small and reusable
4. All public methods documented
5. Test coverage >80%

### Dependency Rules

1. Domain layer has no dependencies
2. Presentation depends on domain
3. Data depends on domain
4. No direct UI-to-data layer access

### Naming Conventions

1. Files: `snake_case.dart`
2. Classes: `PascalCase`
3. Methods: `camelCase`
4. Variables: `camelCase`
5. Constants: `SCREAMING_SNAKE_CASE`
