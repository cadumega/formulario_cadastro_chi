https://cadumega.github.io/tela_login_cadastro_chi/
# Tela_login_cadastro_chi
 Formulário com transição.
 
 ![image](https://user-images.githubusercontent.com/72901445/113342162-870f2100-9304-11eb-841e-9053771fab18.png)

1 - Model Guide

Estruturar o html da melhor forma possível, menos css iremos precisar para fazer as alterações na tela de login e cadastro.

3 tipos de conteúdos :
Content Geralzao = Sign In e Create Account.

dividr em 2 colunas o first content, os estilos são parecidos
.first-column   // ao clicar em tab, automaticamente eu crio uma div     WELCOME BACK
```
<div class="first-column"></div>
```
.second-column         CREATE ACCOUNT
ul>li*3>a  / ao clicar em tab, automaticamente eu crio uma 
```
        <ul>
          <li><a href=""></a></li>
          <li><a href=""></a></li>
          <li><a href=""></a></li>
        </ul>
```

form.form
```
        <form action="" class="form"></form>
vou usar...
        <form class="form"></form>
```


___ intro html
```
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Login</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <div class="container">
    <div class="content first-content">
      <div class="first-column">
          <h2 class="title">welcome back!</h2>
          <p class="description">To keep connected with us</p>
          <p class="description"">please login with your personal info</p>            <button class="btn">sign in</button>
      </div>    
      <div class="second-column">
         <h2 class="title">create account</h2>
        <div class="social-media">
            <ul class="list-social-media">
               <ul>
                  <li><a href="#">facebook</a></li>
                  <li><a href="#">google+</a></li>
                  <li><a href="#">linkedin</a></li>
                </ul>
        </div><!-- social media -->
         <p class="description">or use your email for registration:</p>
          <form class="form">
            <input type="text" placeholder="Name">
            <input type="email" placeholder="Email">
            <input type="password" placeholder="Password">   
            <button class="btn">sign up</button>        
          </form>
        </div><!-- second column -->
      </div><!-- first content -->

    <div class="content second-content">
      <div class="first-column">
          <h2 class="title">hello, friend!</h2>
          <p class="description">Enter your personal details</p>
          <p class="description">and start journey with us</p>
          <button class="btn">sign up</button>
      </div>
        <div class="second-column">
          <h2 class="title">sign in to developer</h2>
          <div class="social-media">
            <ul class="list-social-media">
              <ul>
                <li><a href="#">facebook</a></li>
                <li><a href="#">google+</a></li>
                <li><a href="#">linkedin</a></li>
              </ul>
        </div><!-- social media -->
           <p class="description">or use your email account:</p>
            <form class="form">
             <input type="email" placeholder="Email">
             <input type="password" placeholder="Password">
             <a class="password" href="#">forgot your password?</a>
             <button class="btn">sign in</button>
           </form>
      </div><!-- second column -->
    </div><!-- second-content -->
  </div>

  <script src="js/app.js"></script>

</body>
</html>
```

_parte 2  
Acertar classes diferentes no html 
```
  <div class="container">
    <div class="content first-content">
      <div class="first-column">
          <h2 class="title title-primary">welcome back!</h2>
          <p class="description">To keep connected with us</p>
          <p class="description">please login with your personal info</p>            <button class="btn btn-primary">sign in</button>
      </div>  
```
CSS
```
/* importação de fonte */
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;700&display=swap');
```

```
/* resetar o css */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

```
/* importação de fonte */
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;700&display=swap');
/* resetar o css */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: 'Open Sans', sans-serif;
}
.container {
  display: flex;
  border: 2px solid red;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #ecf0f1;
}
.content {
  background-color: #fff;
  border-radius: 15px;
  width: 80%;
  height: 50%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
}
.content::before {
  content:"";
  position: absolute;
  background-color: #58af9b ;
  width: 40%;
  height: 100%;
}
.title {
  color: #fff;
  font-size: 28px;
  font-weight: bold;
  text-transform: capitalize;
}
.title-primary{
  color: #fff;
}
.description {
  font-size: 14px;
  font-weight: 300;
  color: #fff;
  line-height: 30px;
}
.btn {
  border-radius: 15px;
  text-transform: uppercase;
  color: #fff;
  font-size: 10px;
  padding: 10px 50px;
  cursor: pointer;
  font-weight: bold;
}
.btn-primary {
background-color: transparent;
  border: 1px solid #fff;
}
.btn-primary:hover{
  background: #fff;
  color: #58af9b;
}
.first-content {
  display: flex;
}
.first-column {
  text-align: center;
  flex: 1 0 auto;
  z-index: 10;
}
.second-column {
  flex: 2 0 auto
}
.list-social-media {
  display: flex;
}
.form {
  display: flex;
  flex-direction: column;
}
.second-content{
  position: absolute;
  display: none;
}
```

parte 3
https://fontawesome.com/
<script src="https://kit.fontawesome.com/265e216f38.js" crossorigin="anonymous"></script>
kit de fontes,ícones, só colar no html abaixo da referência ao html

No index html ,defini uma class para cada li , como item social media.

Centralizar circulo no item:
```
line-height: Xpx;
text-align: center;
deves conseguir.

Onde X é igual à height do teu div..
```

tag do ícone no campo, position  absolut usando top bottom etc.. ou por span com bootstrap


label... tab...  
```
<label for=""></label>
```
colocar os inputs dentro da label
propriedade display do ícone, é display inline block. o input mantem em linha também.
se fosse display block, ficaria um embaixo do outro.

margin e padding para acertar posicionamentos .

Para mudar a cor do ícone ao passar o mouse, utilizei de 2 classes 
```
.link-social-media:hover .item-social-media{
  background-color: #58af9b;
  color: #fff;
  border-color:#58af9b;
}
```

Normalmente uso só :
```
.btn-second:hover {
  background-color:  #fff;
  border: 1px solid #58af9b;
  color:#58af9b;
}
```


passar o mouse e já ter clique fácil
 o cursor só mudava quando ele entrava em cima do icone, ai vc colocou a tag "a" para abraçar todo o conteúdo, vc poderia somente usar o display: block; do css e ele já pegaria toda a tag "li". momento 25 até 27.
ou setar como display: list-item.

Verificar second content , hover + fácil verificar

```
/* importação de fonte */
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;700&display=swap');
/* resetar o css */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: 'Open Sans', sans-serif;
}
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 80vh;
  background-color: #ecf0f1;
}
.content {
  background-color: #fff;
  border-radius: 15px;
  width: 980px;
  height: 60%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
}
.content::before {
  content:"";
  position: absolute;
  background-color: #58af9b ;
  width: 40%;
  height: 100%;
  border-radius: 15px;
  /* left: 60%; */
}
.title {
  color: #fff;
  font-size: 28px;
  font-weight: bold;
  text-transform: capitalize;
}
.title-primary {
  color: #fff;
}
.title-second {
  color: #58af9b;
}
.description {
  font-size: 14px;
  font-weight: 300;
  line-height: 30px;
}
.description-primary {
  color: #fff;
}
.description-second {
  color: #7f8c8d;
}
.btn {
  border-radius: 15px;
  text-transform: uppercase;
  color: #fff;
  font-size: 11px;
  padding: 10px 50px;
  cursor: pointer;
  font-weight: bold;
  width: 150px;
  align-self: center;
  border: none;
  margin: 15px; 
}
.btn-primary {
  background-color: transparent;
  border: 1px solid #fff;
}
.btn-primary:hover{
  background: #fff;
  color: #58af9b;
}
.btn-second {
  background-color: #58af9b;
  border: 1px solid  #58af9b;
}
.btn-second:hover {
  background-color:  #fff;
  border: 1px solid #58af9b;
  color:#58af9b;
}
.first-content {
  display: flex;
}
.first-column {
  text-align: center;
  flex: 1 0 auto;
  z-index: 10;
}
.second-column {
  flex: 2 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.list-social-media {
  display: flex;
}
.item-social-media {
  border: 1px solid #bdc3c7;
  border-radius: 50%;
  width: 35px;
  height:  35px;
  text-align: center;
  list-style-type: none;
  display: inline;
  float: left;
  line-height: 35px;   /*  centralizar item no círculo */
  margin:10px 10px 10px 2px;
}
.link-social-media {
  color: #95a5a6;
}
.link-social-media:hover .item-social-media{
  background-color: #58af9b;
  color: #fff;
  border-color:#58af9b;
}
.item-social-media a{
  color: #95a5a6;
  text-align: center;
}
.form {            
  display: flex;
  flex-direction: column;
  width: 55%;
  
}
.form input {
  height: 45px;
  width: 100%;
  border: none;
  background-color: #ecf0f1;
}
.label-input {
  display: flex;
  align-items: center;
  margin: 8px;
  background-color: #ecf0f1;
  border-radius: 20px;
}
.icon-modify {
  color: #7f8c8d;
  padding: 0 5px;
}
/* SECOND CONTENT */
.second-content{
  position: absolute;
  display: none;
}
.second-content .first-column {
  order:2;
}
.second-content .second-column {
  order:1;
}
```


```
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://kit.fontawesome.com/265e216f38.js" crossorigin="anonymous"></script>
</head>
<body>
  <div class="container">
    <div class="content first-content">
      <div class="first-column">
          <h2 class="title title-primary">welcome back!</h2>
          <p class="description description-primary">To keep connected with us</p>
          <p class="description description-primary">please login with your personal info</p>            <button class="btn btn-primary">sign in</button>
      </div>    
      
      <div class="second-column">
         <h2 class="title title-second">create account</h2>
         <div class="social-media">
            <ul class="list-social-media">
               <ul>
                <a class='link-social-media' href='#'>
                  <li class='item-social-media'>
                    <i class="fab fa-facebook-f"></i>
                  </li>
                </a>
                <a class='link-social-media' href='#'>
                  <li class='item-social-media'>
                    <i class="fab fa-google-plus-g"></i>
                  </li>
                </a>
                <a class='link-social-media' href='#'>
                  <li class='item-social-media'>
                    <i class="fab fa-linkedin-in"></i>
                  </li>
                </a>
                </ul>
         </div><!-- social media -->
         <p class="description description-second">or use your email for registration:</p>
          <form class="form">
            <label class='label-input' for="">
              <i class='far fa-user  icon-modify'></i>
              <input type="text" placeholder="Name">
            </label>
            <label class='label-input' for="">
              <i class='far fa-envelope icon-modify'></i>
              <input type="email" placeholder="Email">
            </label>
            <label class='label-input' for="">
              <i class='fas fa-lock icon-modify'></i>
              <input type="password" placeholder="Password"> 
            </label>
           
            <button class="btn btn-second">sign up</button>        
          </form>
      </div><!-- second column -->
    </div><!-- first content -->
    <div class="content second-content">
      <div class="first-column">
          <h2 class="title ">hello, friend!</h2>
          <p class="description ">Enter your personal details</p>
          <p class="description ">and start journey with us</p>
          <button class="btn btn-primary">sign up</button>
      </div>
        <div class="second-column">
          <h2 class="title ">sign in to developer</h2>
          <div class="social-media">
            <ul class="list-social-media">
              <ul>
                <li><a href="#">facebook</a></li>
                <li><a href="#">google+</a></li>
                <li><a href="#">linkedin</a></li>
              </ul>
        </div><!-- social media -->
           <p class="description"> or use your email account:</p>
            <form class="form">
             <input type="email" placeholder="Email">
             <input type="password" placeholder="Password">
             <a class="password" href="#">forgot your password?</a>
             <button class="btn btn-second">sign in</button>
           </form>
      </div><!-- second column -->
    </div><!-- second-content -->
  </div>
  <script src="js/app.js"></script>
</body>
</html>
```

_________________
1- Responsivo em determinado breakpoint ao diminuir a tela ou para mobile. Além da animação diferente debaixo para cima, em vez de esquerda para direita.

Media query ao chegar em determinada largura, que o css irá mudar , alterando a largura do container que era de desktop para mobile ou tablet. Para passar essa informação utilizamos as media querys.
Acima de 1040px é todo o css que desenvolvi. Logo o código terá limitações definidas.

Desktop first ou mobile first, no qual você irá basear o layout.
```
@media screen and (max-width:1040px) {
  
}
```
