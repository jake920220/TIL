# Redux Toolkit

## 개념

Redux의 복잡한 설정과 다양한 서드파티 라이브러리들 (redux-saga, redux-thunk, ...) 등으로
redux의 러닝커브가 높고 코드양이 복잡하고 방대해지자 redux 개발진들이 개발한것.

차이점으로는 slice라는 개념이 생겼는데 action과 reducer, key, initialState 가 하나로 합쳐져있는
구조로 되어있다.

## 사용법

configureStore로 store를 구성하고, createSlice로 slice를 생성해주기만 하면 설정이 전부이다. 간단하다.

<br>

`store.js`
```javascript
import { configureStore } from "@reduxjs/toolkit";

import modalReducer from "./ModalSlice";

export const store = configureStore({
    reducer: {
        modal: modalReducer,
    },
});
```
<br>

`modalSlice.js`
```javascript
import { createSlice } from "@reduxjs/toolkit";

const modalSlice = createSlice({
    name: "modal",
    initialState: {
        isOpen: false,
        modalType: null,
        title: "",
        modalProps: null,
    },
    reducers: {
        openModal: (state, action) => {
            if (!action.payload) return console.log("no payload");
            const { modalType, modalProps } = action.payload;
            state.isOpen = true;
            state.modalType = modalType;
            state.title = modalProps?.title || "";
            state.modalProps = modalProps;
        },
        closeModal: (state) => {
            state.isOpen = false;
            state.modalType = null;
            state.title = "";
            state.modalProps = null;
        },
    },
});

export const { openModal, closeModal } = modalSlice.actions;
export default modalSlice.reducer;
```

`App.js`
```javascript
import { Provider } from "react-redux";
import { store } from "./redux/store";

const App = () => {
    return (
        <Provider store={store}>
            ...route
        </Provider>
    )
}

export default App;
```

<br>

`use cases`
```javascript
import { useDispatch } from "react-redux";
import { openModal } from "../../redux/ModalSlice";

...

dispatch(openModal(...modalProps));
```
