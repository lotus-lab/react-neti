# react-neti

This tool is for handling the network connectivity checks, developed based on hooks,

It checks the network connectivity status of your device in real time through polling.

# Example

## Hooks

```tsx
import React from "react";
import { useConnection } from "react-neti";

export const App = () => {
  const { connection } = useConnection();
  return <div>{connection ? "Online" : "Offline"}</div>;
};
```

## Components

```tsx
import React from "react";
import { OnlineWrapper, OfflineWrapper } from "react-neti";
export const App = () => {
  const { connection } = useConnection();
  return (
    <>
      <OnlineWrapper>
        I will appear only when there is internet connection available
      </OnlineWrapper>
      <OfflineWrapper>
        I will appear only when there is no internet connection
      </OfflineWrapper>
    </>
  );
};
```