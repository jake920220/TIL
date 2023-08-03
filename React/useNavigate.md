# useNavigate in React-router-dom v6

react router v6 에서부터는 useHistory가 사라졌고 useNavigate 훅으로 대체되었다.

기존의

```javascript
    history.push("/uri");
```
부분은

```javascript
    navigate("/uri");
```

로 대체되었고

```javascript
    history.replace("/uri");
```
부분은
```javascript
    navigate('/uri', {replace: true});
```
로 대체되었다.

또한 뒤로가기 또한

```javascript
    history.goBack();
```
에서

```javascript
    navigate(-1);
```
이런 방식으로 변경이 되었다.

직관성은 좀 더 떨어진 것 같다.
