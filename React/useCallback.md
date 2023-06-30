# useCallback

useCallback은 react에서 기본적으로 제공하는 hook중의 하나로 함수를 캐싱하여 재사용 할 수 있게 해주는 훅이다.

```javascript
const Parent = () => {
    const [input, setInput] = useState('');
    const onSave = () => {
        //save
        console.log(input);
    };
    
    const onChangeInput = (e) => {
        setInput(e.target.value);
    }
    
    return (
        <div>
            <input onChange={onChangeInput}/>
            <Children onSave={onSave}/>
        </div>
    )
}
```

이런식으로 넘겨줄때 input의 값이 변할때마다 컴포넌트가 re rendering되게 되면서 onSave함수도 새 함수로 선언이 된다.
그러면 자연스럽게 Children컴포넌트도 re rendering이 되게 되어서 효율적으로 좋지 않게 되는데

```javascript
import {useCallback} from "React";

const Parent = () => {
    const [input, setInput] = useState('');
    const onSave = useCallback(() => {
        //save
        console.log(input);
    }, []);
    
    const onChangeInput = (e) => {
        setInput(e.target.value);
    }
    
    return (
        <div>
            <input onChange={onChangeInput}/>
            <Children onSave={onSave}/>
        </div>
    )
}
```

이렇게 함수를 useCallback의 첫번째 인자에 넣으면 해당 함수는 캐싱된다.
다만 함수자체가 캐싱되어있기 때문에 onSave 내에서 input의 value는 콘솔을 찍어봐도 항상 '' 이다.

useCallback의 2번째 인자는 어떤 변수를 넣느냐에 따라 캐싱을 초기화하는 것을 결정한다.


```javascript
import {useCallback} from "React";

const Parent = () => {
    const [input, setInput] = useState('');
    const onSave = useCallback(() => {
        //save
        console.log(input);
    }, [input]);
    
    const onChangeInput = (e) => {
        setInput(e.target.value);
    }
    
    return (
        <div>
            <input onChange={onChangeInput}/>
            <Children onSave={onSave}/>
        </div>
    )
}
```

이렇게 할 경우 input값이 바뀔때마다 새롭게 캐싱을 하여 input에 대한 변경사항을 onSave내에서 확인할 수 있게 된다.
