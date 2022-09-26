# ReactMovieWebService
ReactMovieWebService

<!-- REACT JS -->
<!-- 22-09-26 -->
1. React JS의 규칙중 하나. => html을 페이지에 직접 작성하지 않는다.
2. React JS = 어플리케이션이 interactive하도록 만들어주는 library.
3. react-dom = libray, 또는 package. React element들을 HTML body에 둘 수 있도록 해준다.
4. render = React element를 가지고 HTML로 만들어 배치한다. 사용자에게 보여준다. 
   React.render();의 형태로 사용함.
5. React JS는 업데이트 해야하는 HTML을 업데이트 시켜준다.
6. React JS는 변수(element)에 property 값으로 event listner를 직접 등록할 수 있다.
7. JSX = JavaScript를 확장한 문법. html과 생긴게 비슷하다.
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