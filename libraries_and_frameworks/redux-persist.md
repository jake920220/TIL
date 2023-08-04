# redux-persist

redux-persist 는 redux store가 브라우저 새로고침을 하면 휘발되는 것을 localStorage 혹은 sessionStorage에 state를 저장하여
새로고침을 하더라도 날아가는 것을 방지하게 해주는 라이브러리이다.

굳이 따지자면 사용자가 state값을 localStorage에 저장하고, 새로고침 시 스토리지에 있는 값을 조회하여 불러온 뒤 그것을 redux store에
다시 값을 씌워주는 일련의 작업들을 대신 해준다고 볼 수 있다.

로그인을 하고 세션을 유지하는 데에 store에 들어간 user정보나 token값을 유지시키는데에 이용하였다.


기존의 reducer에서는 건드릴 것이 크게 없고

```javascript
//store.js

import {
    persistStore,
    persistReducer,
    FLUSH,
    REHYDRATE,
    PAUSE,
    PERSIST,
    PURGE,
    REGISTER,
} from "redux-persist";
import storage from "redux-persist/lib/storage";

const persistConfig = {
    key: "root",
    storage,
    whitelist: ["auth", "user"],
    version: 1,
};

const persistedReducer = persistReducer(persistConfig, authReducer);


export const store = configureStore({
    reducer: {
        datePicker: datePickerModalReducer,
        auth: persistedReducer,
    },
    middleware: (getDefaultMiddleware) =>
        getDefaultMiddleware({
            serializableCheck: {
                ignoredActions: [
                    FLUSH,
                    REHYDRATE,
                    PAUSE,
                    PERSIST,
                    PURGE,
                    REGISTER,
                ],
            },
        }),
});

export const persistor = persistStore(store);

```

```javascript
//App.js
import { store, persistor } from "./redux/store";
import { PersistGate } from "redux-persist/integration/react";

const App = () => {
    const queryClient = new QueryClient({
        defaultOptions: {
            queries: {
                refetchOnWindowFocus: false, // default: true
            },
        },
    });

    return (
        <Provider store={store}>
            <PersistGate loading={null} persistor={persistor}>
                <QueryClientProvider client={queryClient}>
                    <ThemeProvider theme={theme["light"]}>
                        <GlobalStyle />
                        {route()}
                        <DatepickerModal />
                    </ThemeProvider>
                    <ReactQueryDevtools initialIsOpen={false} />
                </QueryClientProvider>
            </PersistGate>
        </Provider>
    );
};

export default App;

```
