# ReactMovieWebService

<!-- REACT JS note -->
<!-- 22-09-26 -->
1. React JS의 규칙중 하나. => html을 페이지에 직접 작성하지 않는다.
2. React JS = 어플리케이션이 interactive하도록 만들어주는 library.
3. react-dom = libray, 또는 package. React element들을 HTML body에 둘 수 있도록 해준다.
4. render = React element를 가지고 HTML로 만들어 배치한다. 사용자에게 보여준다. 
   React.render();의 형태로 사용함.
5. React JS는 렌더링할 때 업데이트 해야하는(값이 변한) HTML 부분만을 업데이트 시켜준다.
6. React JS는 변수(element)에 property 값으로 event listner를 직접 등록할 수 있다. ex) onClick, onChange
7. JSX = JavaScript를 확장한 문법. html과 생긴게 비슷하다. JavaScript + html
   JSX를 사용하기 위해서는 Babel을 설치해야한다. Babel은 JSX 코드를 브라우저가 이해할 수 있는 형태로 바꿔준다. Babel standalone을 이용해서 다운로드한다. Babel 링크를 넣을때는 type="text/babel";을 넣어줘야한다.
8. JSX를 이용하여 렌더링 하는 방법 
   <!-- 변수의 이름 첫글자는 반드시 "대문자"로 써야한다. 소문자로 쓰면 html 요소가 되버림. -->
   <!-- const Container = () => (
            <div> 
                <Button />  
                <Title />
            </div>
        );  
    -->

   <!-- 변수들을 "함수"로 만들어줘야 한다. 함수로 만들시 return은 필수!
        ex1) const Title= () => {   

        };

        ex2) function Title() {
            return (

            );
        };
   -->
   9. React JS 함수 내에서 변수를 사용할때에는 중괄호를 열어주고 변수 이름을 담아주면 된다. 
   ex) {counter}
   <!-- 22-09-27 -->
   10. useState = [data, f] 데이터와 이 데이터의 값을 바꿀 수 있는 함수가 들어있는 배열을 준다.
       데이터의 값이 변하면(state 바뀌면) 자동으로 리렌더링을 일으킨다. React.useState();의 형태로 사용함.
       ex) const [] = React.useState(); 
       -()안에 값을 넣어서 데이터의 초기값을 설정해줄수 있음. (아무것도 안넣어도됨) 
       ex) const [] = React.useState(1);
       -[]안에는 배열의 이름을 마음대로 지정해줄 수 있다. 위에서 설명했듯이 첫번째 값은 데이터가 되고 
       두번째 값은 그 데이터 값을 변경할 수 있는 함수가 들어감.
        ex) const [data, setData] = React.useState(1);
   11. useState 함수를 사용해서 state의 값을 업데이트해줄 때, 업데이트 해줄 값을 함수로 계산할 수 있다.
       ex) setData((current) => current + 1); 보기와 같이 함수가 기본적으로 전달해주는 현재 값(current state)를 활용해서 업데이트 해줄 수 있다. React는 이 current가 확실히 현재 값이라는것을 보장하고있음.
   12. JSX 안에서 if문을 사용할 수 있다. 하지만 작성하는 방식은 html과 다름.
       ex) {index === "0" ? <amount /> : null}
   13. 컴포넌트는 어떤 JSX를 반환하는 함수다.
   14. property = 속성
   15. 컴포넌트 내의 태그안에서 style property를 사용하여 스타일을 바꿀 수 있다.
   16. 부모 컴포넌트에서 자식 컴포넌트로 property(속성)들을 보내줄 수 있다.
   17. React에서 사용하는 모든 컴포넌트들은 ()괄호로 argument(인자)를 받는다.
   18. 컴포넌트에서 전달받는 argument(인자) = props라고 부른다. 
   19. props로는 boolean값(true, false), string(문자), function(함수)를 보낼 수 있다.
   20. React.memo(); = React JS에게 props가 변경되지 않는다면 다시 그릴 필요가 없음을 알려주는것.
   ex) const MemorizedBtn = React.memo(Btn); ()괄호안에 넣은 컴포넌트가 render될 때 props가 변경되지않는 부분이 
   있다면 그 부분은 다시 render하지 말아달라고 부탁하는것.(바뀌는 부분만 리렌더링하도록.)

   21. PropTypes = 어떤 타입의 prop을 받고있는지 체크해준다. 만약 타입이 맞지않다면 콘솔창에서 경고 문구를 띄워줌.
   ex) Btn.propTypes = {
        text: PropTypes.string,
        fontSize: PropTypes.number,
   };
       -만약 이 prop들을 정확히 "갖고 있어야만 한다"는것을 확실히 하고 싶다면 isRequierd를 붙여주면 됨.
   ex) Btn.propTypes = {
        text: PropTypes.string,isRequierd,
        fontSize: PropTypes.number,isRequierd,
   }; 
   (PropTypes를 사용하려면 script를 설치해야함.)
   <!-- creact-react-app -->
   22. creact-react-app으로 파일을 생성하려면 cmd창에 다음과 같이 작성해야한다.(파일 경로 설정 가능)
    npx creact-react-app 파일이름(마음대로)
    -로딩이 끝난 후 파일이름을 입력하면 생성된 파일이 열림.
   23. creact-react-app으로 생성된 파일의 라이브 서버(웹사이트)를 열려면 터미널에 
    npm-run-start 또는 npm-start라고 입력해주면 된다.  
   24. 모든 폴더가 src 폴더 안에 있어야한다.
   25. 가장 중요한 파일은 index.js 파일이다.
   26. 처음 파일이 열렸을 때 작성되어있는 기본 코드들은 필요한것만 남기고 지워준다. 파일은 index.js, App.js만 남김.
   27. 파일을 가져오는 코드
   ex) import 파일이름 from "경로"
   28. 파일을 내보내는 코드
   ex) export default 파일이름;
   29. propTypes를 체크하려면 터미널에서 npm i prop-types를 입력해서 설치한다. 그리고 import해온다.
    import PropTypes from "prop-types";
   30. creact-react-app으로 작업할때, css에 관한 두가지 선택지를 가질 수 있다.
       1. 한개의 css 파일 만들기.(평범한 css 파일. css 파일을 import 해오면 됨.) => 단점 : 전역적인 파일이라 파일의 모든 코드에 적용됨.
       2. 컴포넌트안에서 style prop 사용하기. => 단점 : html 파일에 style이 직접적으로 들어감.
   31. 30번에 대한 해결책으로 CSS module을 사용할 수 있다. 각각의 컴포넌트를 사용하는 파일에 각각의 이름으로 css 파일을 만들어서 적용시켜준다. 이름.module.css
   ex) Button.js 파일에서 Button.module.css 파일을 import해와서 사용함.
   32. style을 적용시키고 싶은 부분에 className을 정해준다. 
       -className도 모듈화해서 사용이 가능.
       -creact-react-app은 랜덤한 클래스 이름을 만들어서 붙여줌. 같은 클래스 이름을 사용하더라도 문제되지 않음.
   <!-- 22-09-28 -->
   33. useEffect() = 코드를 언제 실행할지 선택할 수 있게 해줌. 코드를 한번만 실행하거나 특정한 아이템에 변화가 있을때 실행하도록.
   1. 코드를 한번만 실행함 ([]를 비워놓는다면.)
   2. 한개의 아이템만 지켜보도록함.
   3. 여러개의 아이템을 지켜보도록함.
   -두개의 argument를 인자로 가짐. 
   -첫번째 argument: EventCallback 우리가 실행시키고 싶은 코드 
   -두번째 argument: DependencyList react.js가 지켜봐야하는것들 []
   ex) useEffect(() => {

   }, []);
   []안에 원하는걸 뭐든지 지켜보도록 적어줄 수 있음.

   34. Cleanup function = 함수가 종료될 때 코드를 실행할 수 있게 해준다. useEffect 함수 내에서 사용.
   ex) useEffect(() => {
        console.log("hi);
        return () => console.log("bye");
   }, []);