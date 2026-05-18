# React Native Starter Kit

A production-ready React Native starter kit built with Expo, designed to cut project setup from weeks to days. Used as the foundation for real client apps.

## Stack

| Category | Technology |
|---|---|
| Framework | Expo + React Native |
| Navigation | React Navigation v7 (typed) |
| State | Zustand + SecureStore persistence |
| Server State | TanStack React Query |
| Forms | react-hook-form + Zod |
| API | Axios + interceptors + exponential backoff |
| Styling | StyleSheet + custom theme system |
| Animations | react-native-reanimated ~3.10.0 |
| Bottom Sheet | @gorhom/bottom-sheet v4 |

## What's Included

### Navigation
- Typed `AuthStack`, `AppStack`, `BottomTabs`, `RootNavigator`
- Splash screen → auth hydration → correct stack

### Auth
- Phone + OTP + Register + Welcome screens
- Zustand auth store persisted via SecureStore
- `useLogin`, `useOTP`, `useRegister` hooks

### API Layer
- Axios instance with base URL config
- Request + response interceptors
- Exponential backoff retry on network failure

### Theme System
- Dark / light mode support
- `useTheme` hook for any component
- Single `colors.ts` to swap per project
- Typography, spacing, radius, shadow tokens

### Component Library
`Button` `Input` `Divider` `Card` `Badge` `Avatar` `Loader` `Skeleton` `EmptyState` `Toast` `Modal` `BottomSheet` `Header` `ListItem`

### Forms Module
- `useAppForm` — `useForm` + `zodResolver` wrapper
- `FormField` — bridges RHF Controller to any input
- `auth.schema.ts`, `profile.schema.ts`

### Utilities
- Permissions — gallery, location (request + check)
- Offline banner — animated, realtime NetInfo listener
- App loading state — animated splash with hydration guard

### Dev Playground
UI Lab screen with preview screens for every component in the library.

## Folder Structure

```
src/
├── components/
│   ├── forms/          # FormField
│   └── ui/             # Component library
│       └── ComponentName/
│           ├── AppComponentName.tsx
│           ├── styles.ts
│           ├── types.ts
│           ├── constants.ts
│           └── index.ts
├── features/
│   └── auth/           # Auth screens, hooks, store
├── hooks/              # useAppForm, useTheme, etc.
├── navigation/         # Typed stacks + RootNavigator
├── schemas/            # Zod schemas
├── services/           # API layer
├── store/              # Zustand stores
├── theme/              # Colors, typography, spacing
└── utils/              # Permissions, network
```

## Getting Started

```bash
# Clone
git clone https://github.com/irf0/react-native-starter-kit.git
cd react-native-starter-kit

# Install
npm install

# Start
npx expo start
```

## Per Project Setup

To use this kit for a new project, change only these files:

```
src/theme/colors.ts     → swap brand colors
src/config/             → API base URL, app name
assets/                 → logo, splash image
app.json                → app name, bundle ID
```

## Used In Production

This kit is the foundation for **Akbar's Darbar** — a restaurant ordering app with 500+ downloads, 4.6 Play Store rating, generating Rs. 5–8L in restaurant revenue.

## License

MIT
