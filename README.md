inicialização front end ( abrindo aplicação)
  
    npm install
    npm update 
    npm start  
    npm s 
   
inicialização back end (abrindo swagger)

    ctrl + shift + b
    inicializar na DevIO.Api
     
soluções para possiveis erro na depedencia do front 

    npm cache clean --force
    npm pkill node
    npm install
  

api em: https://github.com/alfredo1995/WebAPI
  
<br>
  
Pronto! kkk Agora vamos ao passo a passo do desenvolvimento de SPA em Angular ;)   

    ng new --minimal -g MeuProjeto

Dando uma cara para aplicação 

    MeuProjeto > index.html

costumizar a paginia inicial index.html

    <!doctype html>
    <html lang="en">
    <head>
 
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrik-to-fit=no">
    <link rel="icon" type="image/x-icon" href="favicon.ico">

    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" crossorigin="anonymous">
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/font-awesome/4.3.1/css/font-awesome.min.cs" crossorigin="anonymous">

    <title>Minnha Aplicação Angular</title>
    </head>
    <body>
    <app-root></app-root>
    </body>
    </html>

Criar templateUrl em MeuProjeto > app > app.component.ts

    import { Component, inject, Injectable } from '@angular/core';

    @Component({
    selector: 'app-root',
    templateUrl: './app.component.html',
    })
    export class AppComponent {
    title = 'MeuProjeto';
    }

criar o app.component.html

    MeuProjeto > app > app.component.html

criar html de navegação e o corpo da pagina app.component.html

    <!--Navigation-->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">Minha Aplicacao</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarResponsive">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarRensponsive">
                <ul class="navbar-nav ml-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#">Produtos</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Sobre</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Contato</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Feature</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!--FIM do Navigation-->

    <!--Page Content-->
    <header class="bg-primary py-5 mb-5">
        <div class="container h-100">
            <div class="row h-100 align-items-center">
                <div class="col-lg-2">
                    <img src="https://angular.io/assets/images/logos/angular/angular.svg"/>
                </div>
                <div class="col-lg-10">
                    <h1 class="display-4 text-white mt-5 mb-2">Desenvolivimento SPA com Angular</h1>
                    <p class="lead mb-5 text-white">Aplicação está rodando com sucesso guy</p> 
                </div>
            </div>    
        </div>
    </header>

    <div class="container main-container">
        <div class="row text-center">
            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                    <img class="card-img-top" src="/assets/crossplat.jpg" height="164px" width="253px" alt="">
                    <div class="card-body">
                        <h4 class="card-title">Multiplataforma</h4>
                        <p class="card-text">Lorem ipsum dolor</p>
                    </div>
                    <div class="card-footer">
                        <a href="#" class="btn btn-primary">Saiba Mais</a>
                    </div>
                </div>
            </div>

            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                <img class="card-img-top" src="/assets/performance.jpg" height="164px" width="253px" alt="">
                <div class="card-body">
                    <h4 class="card-title">performance</h4>
                    <p class="card-text">Lorem ipsum dolor</p>
                </div>
                <div class="card-footer">
                    <a href="#" class="btn btn-primary">Saiba Mais</a>
                </div>
            </div>
            </div>

            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                <img class="card-img-top" src="/assets/produtividade.jpg" height="164px" width="253px" alt="">
                <div class="card-body">
                    <h4 class="card-title">Produtividade</h4>
                    <p class="card-text">Lorem ipsum dolor</p>
                </div>
                <div class="card-footer">
                    <a href="#" class="btn btn-primary">Saiba Mais</a>
                </div>
            </div>
            </div>

            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                <img class="card-img-top" src="/assets/full_dev.jpg" height="164px" width="253px" alt="">
                <div class="card-body">
                    <h4 class="card-title">Funcionalidade</h4>
                    <p class="card-text">Lorem ipsum dolor</p>
                </div>
                <div class="card-footer">
                    <a href="#" class="btn btn-primary">Saiba Mais</a>
                </div>
            </div>
            </div>
    </div>

    <!--FIM Page Content-->

    <!-- Footer -->
    <footer class="bg-dark fixed-bottom footer">
        <div>
            <p style="padding-top: 1px;" class="text-center text-white">alfredogomes1995@gmail.com</p>
        </div>
    </footer>



Definindo os componentes de navegação

    criar component para cada parte da aplicação ( menu , corpo e rodape )

terminal git bash

    ng g c navegacao/menu

MeuProjeto > navegacao> menu > menu.component.ts

    import { Component } from '@angular/core';

    @Component({
    selector: 'app-menu',
    templateUrl: './menu.component.html'
    })
    export class MenuComponent { }

terminal git bash

    ng g c navegacao/home

MeuProjeto > navegacao> home > home.component.ts

    import { Component } from '@angular/core';

    @Component({
    selector: 'app-home',
    templateUrl: './home.component.html'
    })
    export class HomeComponent { }


terminal git bash

    ng g c navegacao/footer

MeuProjeto > navegacao> footer > footer.component.ts

    import { Component } from '@angular/core';

    @Component({
    selector: 'app-footer',
    templateUrl: './footer.component.html'
    })
    export class FooterComponent { }

extrair a parte de navegação do app.component.html 

    <!--Navigation-->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">Minha Aplicacao</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarResponsive">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarRensponsive">
                <ul class="navbar-nav ml-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#">Produtos</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Sobre</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Contato</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Feature</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

criar dentro da pasta menu > menu.component.html > jogar o arquivo nav extraido

    <!--Navigation-->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">Minha Aplicacao</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarResponsive">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarRensponsive">
                <ul class="navbar-nav ml-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#">Produtos</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Sobre</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Contato</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Feature</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    
    <!--FIM do Navigation-->

extrair a parte de <!--Page Content--> do app.component.html 

    <!--Page Content-->
    <header class="bg-primary py-4 mb-4">
        <div class="container h-100">
            <div class="row h-100 align-items-center">
                <div class="col-lg-2">
                    <img src="https://angular.io/assets/images/logos/angular/angular.svg"/>
                </div>
                <div class="col-lg-10">
                    <h1 class="display-4 text-white mt-5 mb-2">Desenvolivimento SPA com Angular</h1>
                    <p class="lead mb-5 text-white">Aplicação está rodando com sucesso</p> 
                </div>
            </div>    
        </div>
    </header>

    <div class="container main-container">
        <div class="row text-center">
            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                    <img class="card-img-top" src="https://hml.vertigo.com.br/wp-content/uploads/2018/04/mobile-apps-768x577-1.jpg" height="164px" width="253px" alt="">
                    <div class="card-body">
                        <h4 class="card-title">Multiplataforma</h4>
                        <p class="card-text">Lorem Ipsum é uma simulação de texto da indústria tipográfica e vem sendo utilizado desde o século XVI</p>
                    </div>
                    <div class="card-footer">
                        <a href="#" class="btn btn-primary">Saiba Mais</a>
                    </div>
                </div>
            </div>

            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                <img class="card-img-top" src="https://vooozer.com/wp-content/uploads/2018/05/Teste-de-performance-de-site-1280x720.png" height="164px" width="253px" alt="">
                <div class="card-body">
                    <h4 class="card-title">performance</h4>
                    <p class="card-text">Lorem Ipsum é uma simulação de texto da indústria tipográfica e vem sendo utilizado desde o século XVI</p>
                </div>
                <div class="card-footer">
                    <a href="#" class="btn btn-primary">Saiba Mais</a>
                </div>
            </div>
            </div>

            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                <img class="card-img-top" src="https://files.caetreinamentos.com.br/blog/wp-content/uploads/2019/09/27215227/produtividade-banner.png" height="164px" width="253px" alt="">
                <div class="card-body">
                    <h4 class="card-title">Produtividade</h4>
                    <p class="card-text">Lorem Ipsum é uma simulação de texto da indústria tipográfica e vem sendo utilizado desde o século XVI</p>
                </div>
                <div class="card-footer">
                    <a href="#" class="btn btn-primary">Saiba Mais</a>
                </div>
            </div>
            </div>

            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                <img class="card-img-top" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTxR3U-sPuYc8YbUTshKfsRUcWqeRbzRXBArxneL4YU7DRHRgdCHb640rKF3nERR9Q4mbg&usqp=CAU" height="164px" width="253px" alt="">
                <div class="card-body">
                    <h4 class="card-title">Funcionalidade</h4>
                    <p class="card-text">Lorem Ipsum é uma simulação de texto da indústria tipográfica e vem sendo utilizado desde o século XVI</p>
                </div>
                <div class="card-footer">
                    <a href="#" class="btn btn-primary">Saiba Mais</a>
                </div>
            </div>
            </div>
    </div>

    <!--FIM Page Content-->

criar dentro da pasta home > home.component.html > jogar o arquivo nav extraido

    <!--Page Content-->
    <header class="bg-primary py-4 mb-4">
        <div class="container h-100">
            <div class="row h-100 align-items-center">
                <div class="col-lg-2">
                    <img src="https://angular.io/assets/images/logos/angular/angular.svg" />
                </div>
                <div class="col-lg-10">
                    <h1 class="display-4 text-white mt-5 mb-2">Desenvolivimento SPA com Angular</h1>
                    <p class="lead mb-5 text-white">Aplicação está rodando com sucesso</p>
                </div>
            </div>
        </div>
    </header>

    <div class="container main-container">
        <div class="row text-center">
            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                    <img class="card-img-top"
                        src="https://hml.vertigo.com.br/wp-content/uploads/2018/04/mobile-apps-768x577-1.jpg" height="164px"
                        width="253px" alt="">
                    <div class="card-body">
                        <h4 class="card-title">Multiplataforma</h4>
                        <p class="card-text">Lorem Ipsum é uma simulação de texto da indústria tipográfica e vem sendo
                            utilizado desde o século XVI</p>
                    </div>
                    <div class="card-footer">
                        <a href="#" class="btn btn-primary">Saiba Mais</a>
                    </div>
                </div>
            </div>

            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                    <img class="card-img-top"
                        src="https://vooozer.com/wp-content/uploads/2018/05/Teste-de-performance-de-site-1280x720.png"
                        height="164px" width="253px" alt="">
                    <div class="card-body">
                        <h4 class="card-title">performance</h4>
                        <p class="card-text">Lorem Ipsum é uma simulação de texto da indústria tipográfica e vem sendo
                            utilizado desde o século XVI</p>
                    </div>
                    <div class="card-footer">
                        <a href="#" class="btn btn-primary">Saiba Mais</a>
                    </div>
                </div>
            </div>

            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                    <img class="card-img-top"
                        src="https://files.caetreinamentos.com.br/blog/wp-content/uploads/2019/09/27215227/produtividade-banner.png"
                        height="164px" width="253px" alt="">
                    <div class="card-body">
                        <h4 class="card-title">Produtividade</h4>
                        <p class="card-text">Lorem Ipsum é uma simulação de texto da indústria tipográfica e vem sendo
                            utilizado desde o século XVI</p>
                    </div>
                    <div class="card-footer">
                        <a href="#" class="btn btn-primary">Saiba Mais</a>
                    </div>
                </div>
            </div>

            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card h-100">
                    <img class="card-img-top"
                        src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTxR3U-sPuYc8YbUTshKfsRUcWqeRbzRXBArxneL4YU7DRHRgdCHb640rKF3nERR9Q4mbg&usqp=CAU"
                        height="164px" width="253px" alt="">
                    <div class="card-body">
                        <h4 class="card-title">Funcionalidade</h4>
                        <p class="card-text">Lorem Ipsum é uma simulação de texto da indústria tipográfica e vem sendo
                            utilizado desde o século XVI</p>
                    </div>
                    <div class="card-footer">
                        <a href="#" class="btn btn-primary">Saiba Mais</a>
                    </div>
                </div>
            </div>
        </div>

        <!--FIM Page Content-->

extrair a parte de <!-- Footer -->  do app.component.html 

    <!-- Footer -->
    <footer class="bg-dark fixed-bottom footer">
        <div>
            <p style="padding-top: 1px;" class="text-center text-white">alfredogomes1995@gmail.com</p>
        </div>
    </footer>

criar dentro da pasta home > home.component.html > jogar o arquivo nav extraido

    <!-- Footer -->
    <footer class="bg-dark fixed-bottom footer">
        <div>
            <p style="padding-top: 1px;" class="text-center text-white">alfredogomes1995@gmail.com</p>
        </div>
    </footer>

chamando os component em app.component.html

    <app-menu></app-menu>
    <app-home></app-home>
    <app-footer></app-footer>


definindo roteamento e configurações

    abrir git bash na pasta da aplicação

criar component

    ng g c institucional/sobre

git bash 

    ng g c institucional/contato


criar arquivo de configuração de rotas em app > app.routes.ts

    import { RouteConfigLoadStart, Routes } from "@angular/router";
    import { ContatoComponent } from "./institucional/contato/contato.component";
    import { SobreComponent } from "./institucional/sobre/sobre.component";
    import { HomeComponent } from "./navegacao/home/home.component";

    export const rootRouterConfig: Routes = 
    [
        {path: '', redirectTo: '/home', pathMatch: 'full'},
        {path: 'home', component: HomeComponent},
        {path: 'contato', component: ContatoComponent},
        {path: 'sobre', component: SobreComponent}
    ];


configurar a rota criada no model

    MeuProjeto > app > app.modules.ts

importa o caminho da rota e fixar os provides em app.modules.ts

    import { RouterModule } from '@angular/router';
    import { APP_BASE_HREF } from '@angular/common';

    imports: [
    BrowserModule,
    [RouterModule.forRoot(rootRouterConfig, { useHash: false})]
    ],

    @NgModule({
    imports: [
        BrowserModule,
        [RouterModule.forRoot(rootRouterConfig, { useHash: false})]
    ],
    providers: [
        {provide: APP_BASE_HREF, useValue: '/'}
    ],    

substuir a <app-home> pela diretiva de navegação

    app.component.html = <router-outlet></router-outlet>

criar views do sobre e contato 

    app > sobre > sobre.component.html
    app > contato > contato.component.html

costumizar view do component contato.component.html

        <!-- Page Content -->
        <div class="container main-container">

            <!-- Jumbotron Header -->
            <header class="jumbotron my-4">
                <h1 class="display-3">Contato!</h1>
                <p class="lead">Aqui você pode colocar um mapa para informar seu local de trabalho.</p>
            </header>

            <form class="mbr-form">
                <div class="row row-sm-offset">
                    <div class="col-md-4 multi-horizontal" data-for="name">
                        <div class="form-group">
                            <label class="form-control-label mbr-fonts-style display-7" for="name-form1-2w">Nome</label>
                            <input type="text" class="form-control" name="name" data-form-field="Name" required=""
                                id="name-form1-2w">
                        </div>
                    </div>
                    <div class="col-md-4 multi-horizontal" data-for="email">
                        <div class="form-group">
                            <label class="form-control-label mbr-fonts-style display-7" for="email-form1-2w">E-mail</label>
                            <input type="email" class="form-control" name="email" data-form-field="Email" required=""
                                id="email-form1-2w">
                        </div>
                    </div>
                    <div class="col-md-4 multi-horizontal" data-for="phone">
                        <div class="form-group">
                            <label class="form-control-label mbr-fonts-style display-7" for="phone-form1-2w">Telefone</label>
                            <input type="tel" class="form-control" name="phone" data-form-field="Phone" id="phone-form1-2w">
                        </div>
                    </div>
                </div>
                <div class="form-group" data-for="message">
                    <label class="form-control-label mbr-fonts-style display-7" for="message-form1-2w">Mensagem</label>
                    <textarea type="text" class="form-control" name="message" rows="7" data-form-field="Message"
                        id="message-form1-2w"></textarea>
                </div>

                <span class="input-group-btn">
                    <button href="" type="submit" class="btn btn-primary btn-form display-4">Enviar</button>
                </span>
            </form>
        </div>
        <br>

    costumizar view do component sobre.component.html

    <div class="bg-light">
        <div class="container py-5">
            <div class="row h-100 align-items-center py-5">
                <div class="col-lg-6">
                    <h1 class="display-4">Quem somos</h1>
                    <p class="lead text-muted mb-0">Utilize a criatividade aqui!</p>
                </div>
                <div class="col-lg-6 d-none d-lg-block"><img
                        src="https://res.cloudinary.com/mhmd/image/upload/v1556834136/illus_kftyh4.png" alt=""
                        class="img-fluid"></div>
            </div>
        </div>
    </div>

    <div class="bg-white py-5">
        <div class="container py-5">
            <div class="row align-items-center mb-5">
                <div class="col-lg-6 order-2 order-lg-1"><i class="fa fa-bar-chart fa-2x mb-3 text-primary"></i>
                    <h2 class="font-weight-light">Lorem ipsum dolor sit amet</h2>
                    <p class="font-italic text-muted mb-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
                        eiusmod tempor incididunt ut labore et dolore magna aliqua.</p><a href="#"
                        class="btn btn-light px-5 rounded-pill shadow-sm">Learn More</a>
                </div>
                <div class="col-lg-5 px-5 mx-auto order-1 order-lg-2"><img
                        src="https://res.cloudinary.com/mhmd/image/upload/v1556834139/img-1_e25nvh.jpg" alt=""
                        class="img-fluid mb-4 mb-lg-0"></div>
            </div>
            <div class="row align-items-center">
                <div class="col-lg-5 px-5 mx-auto"><img
                        src="https://res.cloudinary.com/mhmd/image/upload/v1556834136/img-2_vdgqgn.jpg" alt=""
                        class="img-fluid mb-4 mb-lg-0"></div>
                <div class="col-lg-6"><i class="fa fa-leaf fa-2x mb-3 text-primary"></i>
                    <h2 class="font-weight-light">Lorem ipsum dolor sit amet</h2>
                    <p class="font-italic text-muted mb-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
                        eiusmod tempor incididunt ut labore et dolore magna aliqua.</p><a href="#"
                        class="btn btn-light px-5 rounded-pill shadow-sm">Learn More</a>
                </div>
            </div>
        </div>
    </div>

    <div class="bg-light py-5">
        <div class="container py-5">
            <div class="row mb-4">
                <div class="col-lg-5">
                    <h2 class="display-4 font-weight-light">Our team</h2>
                    <p class="font-italic text-muted">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
                </div>
            </div>

            <div class="row text-center">
                <!-- Team item-->
                <div class="col-xl-3 col-sm-6 mb-5">
                    <div class="bg-white rounded shadow-sm py-5 px-4"><img
                            src="https://res.cloudinary.com/mhmd/image/upload/v1556834132/avatar-4_ozhrib.png" alt=""
                            width="100" class="img-fluid rounded-circle mb-3 img-thumbnail shadow-sm">
                        <h5 class="mb-0">Manuella Nevoresky</h5><span class="small text-uppercase text-muted">CEO -
                            Founder</span>
                        <ul class="social mb-0 list-inline mt-3">
                            <li class="list-inline-item"><a href="#" class="social-link"><i
                                        class="fa fa-facebook-f"></i></a></li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-twitter"></i></a>
                            </li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-instagram"></i></a>
                            </li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-linkedin"></i></a>
                            </li>
                        </ul>
                    </div>
                </div>
                <!-- End-->

                <!-- Team item-->
                <div class="col-xl-3 col-sm-6 mb-5">
                    <div class="bg-white rounded shadow-sm py-5 px-4"><img
                            src="https://res.cloudinary.com/mhmd/image/upload/v1556834130/avatar-3_hzlize.png" alt=""
                            width="100" class="img-fluid rounded-circle mb-3 img-thumbnail shadow-sm">
                        <h5 class="mb-0">Samuel Hardy</h5><span class="small text-uppercase text-muted">CEO - Founder</span>
                        <ul class="social mb-0 list-inline mt-3">
                            <li class="list-inline-item"><a href="#" class="social-link"><i
                                        class="fa fa-facebook-f"></i></a></li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-twitter"></i></a>
                            </li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-instagram"></i></a>
                            </li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-linkedin"></i></a>
                            </li>
                        </ul>
                    </div>
                </div>
                <!-- End-->

                <!-- Team item-->
                <div class="col-xl-3 col-sm-6 mb-5">
                    <div class="bg-white rounded shadow-sm py-5 px-4"><img
                            src="https://res.cloudinary.com/mhmd/image/upload/v1556834133/avatar-2_f8dowd.png" alt=""
                            width="100" class="img-fluid rounded-circle mb-3 img-thumbnail shadow-sm">
                        <h5 class="mb-0">Tom Sunderland</h5><span class="small text-uppercase text-muted">CEO -
                            Founder</span>
                        <ul class="social mb-0 list-inline mt-3">
                            <li class="list-inline-item"><a href="#" class="social-link"><i
                                        class="fa fa-facebook-f"></i></a></li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-twitter"></i></a>
                            </li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-instagram"></i></a>
                            </li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-linkedin"></i></a>
                            </li>
                        </ul>
                    </div>
                </div>
                <!-- End-->

                <!-- Team item-->
                <div class="col-xl-3 col-sm-6 mb-5">
                    <div class="bg-white rounded shadow-sm py-5 px-4"><img
                            src="https://res.cloudinary.com/mhmd/image/upload/v1556834133/avatar-1_s02nlg.png" alt=""
                            width="100" class="img-fluid rounded-circle mb-3 img-thumbnail shadow-sm">
                        <h5 class="mb-0">John Tarly</h5><span class="small text-uppercase text-muted">CEO - Founder</span>
                        <ul class="social mb-0 list-inline mt-3">
                            <li class="list-inline-item"><a href="#" class="social-link"><i
                                        class="fa fa-facebook-f"></i></a></li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-twitter"></i></a>
                            </li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-instagram"></i></a>
                            </li>
                            <li class="list-inline-item"><a href="#" class="social-link"><i class="fa fa-linkedin"></i></a>
                            </li>
                        </ul>
                    </div>
                </div>
                <!-- End-->

            </div>
        </div>
    </div>

linkar as view nos menus de navegações 

    menu.component.html

    link diretivar trocando os href pelos [routerLink]="['/']" em menu.component.html

        <a class="navbar-brand" [routerLink]="['/home']" routerLinkActive="router-link-active" ]>Minha Aplicacao</a>

        <li class="nav-item">
            <a class="nav-link" [routerLink]="['/sobre']">Sobre</a>
            </li>
            <li class="nav-item">
            <a class="nav-link" [routerLink]="['/contato']">Contato</a>
        </li>   
        
menu.component.html

    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top ">
        <div class="container">
            <a class="navbar-brand" [routerLink]="['/home']" routerLinkActive="router-link-active" >Minha App Angular</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarResponsive">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarResponsive">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link" [routerLink]="['/produtos']" routerLinkActive="router-link-active" >Produtos</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" [routerLink]="['/sobre']" routerLinkActive="router-link-active" >Sobre</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" [routerLink]="['/contato']" routerLinkActive="router-link-active" >Contato</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" [routerLink]="['/feature-data-binding']" >Features</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    <!-- FIM Navigation -->

dataBind

    ng g c demos/DataBinding

app.routes.ts
    
    {path: 'feature-data-binding', component: DataBindingComponent}

criar interporlação app > demos > data-binding.component.ts

    import { Component, OnInit } from '@angular/core';
    @Component({
    selector: 'app-data-binding',
    templateUrl: './data-binding.component.html',
    styles: [
    ]
    })
    export class DataBindingComponent {
    
    public contadorClique: number = 0;

    }

interpolar app > demos > data-binding.component.html

    <div class="">
        <h3>interpolação</h3>

        <p>o numero de cliques é: {{contadorClique}} </p>
    </div>


exibição  data-binding.component.html

    <div class="">
        <h3>interpolação</h3>

        <p>o numero de cliques é: {{contadorClique}} </p>
    </div>

    <div class="">
        <h3>Property Binding</h3>

        <button class="btn btn-info" disabled></button>
    </div>

    <div class="">
        <h3>Event Binding</h3>

        <button class="btn btn-warning" (click)="adicionarClique()">Clique em Mim!</button>
    </div>

    <div class="">
        <h3>Two-way Binding</h3>

        <!-- <input type="text" (keyUp)='keyUp($event)' placeholder="Digite seu nome">
            <label>seu nome é: {{nome}} </label> -->

        <input type="text" [(ngModel)]="nome" (ngModelChange)='nome = $event' placeholder="Digite seu nome">
        <label>seu nome é: {{nome}} </label>
    </div>


exibição  data-binding.component.ts

    import { Component, OnInit } from '@angular/core';

    @Component({
    selector: 'app-data-binding',
    templateUrl: './data-binding.component.html',
    styles: [
    ]
    })
    export class DataBindingComponent {
    
    public contadorClique: number = 0;
    public nome: string = "";

    adicionarClique(){
        this.contadorClique++;
    }

    keyUp(event: any){
        this.nome = event.target.value;
    }
    }

importando o FormsModule no app.modules.ts

    import { FormsModule } from '@angular/forms';
    import { Server } from 'http'
import { endianness } from 'os'
import { ProdutoService } from 'src/app/produtos/produtos.service'
        
    imports: [
        BrowserModule,
        FormsModule,
    

 
consumindo dados do fake back end

    npm install -g json-server

Rodando o npm json server
        
    Set-ExecutionPolicy Unrestricted -Scope CurrentUser

Se necessario abra o PowerShell em modo ADM
    
    aperta Windows + X

    Set-ExecutionPolicy Unrestricted -Scope CurrentUser

execute os comando json novamente

    npm install -g json-server
    Set-ExecutionPolicy Unrestricted -Scope CurrentUser

criar o serviço responsalve por acessar o fake back endianness

    criar pasta > produtos > ProdutoService.cs
    
declarar a class ProdutoService.cs

    import { Injectable } from '@angular/core';

import { ListaProdutoComponent } from 'src/app/produtos/lista-produto/lista-produto.component'
    @Injectable()
    export class ProdutoService{}   

fixar a url do end point (service)
    @Injectable()
    export class ProdutoService {

        protected UrlServiceV1: string = "http://localhost:3000/";

        }
    }

criar metodo para retornar uma ListaProdutoComponent
    @Injectable()
    export class ProdutoService {

        protected UrlServiceV1: string = "http://localhost:3000/";

        obterProdutos() : Observable<Produto[]> {
            return this.http
            .get<Produto[]>(this.UrlServiceV1 + "produtos");
        }}
    
acesando end point externo usando a class HttpClient ( injectar no construtor)
    @Injectable()
    export class ProdutoService {

    constructor(private http: HttpClient) { }

        protected UrlServiceV1: string = "http://localhost:3000/";

        obterProdutos() : Observable<Produto[]> {
            return this.http
            .get<Produto[]>(this.UrlServiceV1 + "produtos");
        }
    }

Class ProdutoService.service.ts

    import { Injectable } from '@angular/core';
    import { HttpClient } from "@angular/common/http";
    import { Produto } from './produto';
    import { Observable } from 'rxjs';
    @Injectable()
    export class ProdutoService {

    constructor(private http: HttpClient) { }

        protected UrlServiceV1: string = "http://localhost:3000/";

        obterProdutos() : Observable<Produto[]> {   
            return this.http
            .get<Produto[]>(this.UrlServiceV1 + "produtos");
        }
    }

consumindo o serviço atraves do componente 

    app.routes.ts
    
adiciona nas rotas o caminho do produto 

    { path: 'produtos', component: ListaProdutoComponent },
    { path: 'produto-detalhe/:id', component: ListaProdutoComponent }

    app.routes.ts 

    import { Routes } from '@angular/router';
    import { HomeComponent } from './navegacao/home/home.component';
    import { ContatoComponent } from './institucional/contato/contato.component';
    import { SobreComponent } from './institucional/sobre/sobre.component';
    import { DataBindingComponent } from './demos/data-binding/data-binding.component';
    import { ListaProdutoComponent } from './produtos/lista-produto/lista-produto.component';

    export const rootRouterConfig: Routes = [
        { path: '', redirectTo: '/home', pathMatch: 'full'},
        { path: 'home', component: HomeComponent},
        { path: 'contato', component: ContatoComponent },
        { path: 'sobre', component: SobreComponent },
        { path: 'feature-data-binding', component: DataBindingComponent },
        { path: 'produtos', component: ListaProdutoComponent },
        { path: 'produto-detalhe/:id', component: ListaProdutoComponent }
    ];

criar view de produto lista-produto.component.html

    <div class="container main-container">

        <div class="row text-center">
            
            <div *ngFor="let produto of produtos" class="col-md-4" style="padding-bottom: 30px;">
                <div class="card h-100">
                    <a class="text-decoration-none" [routerLink]="['/produto-detalhe', produto.id]">
                        <div style="align-content:center;">
                            <img src="/assets/{{ produto.imagem }}" height="164px" width="253px" alt="">
                        </div>
                    </a>
                    <h4 class="card-title">{{ produto.nome | titlecase }}</h4>

                    <div [ngSwitch]="produto.promocao">
                        <p *ngSwitchCase="true">Promoção!</p>
                        <p *ngSwitchCase="false">Por apenas:</p>
                    </div>

                    <div *ngIf="produto.promocao" class="card-body">
                        <div><h4 class="card-text">De:
                            <small><del>{{ produto.valor | currency:'BRL':true:'1.2-2':'pt' }}</del></small>
                            Por: {{ produto.valorPromo | currency:'BRL':true:'1.2-2':'pt' }}
                        </h4></div>
                    </div>

                    <div *ngIf="!produto.promocao" class="card-body">
                        <div><h4>{{ produto.valor | currency:'BRL':true:'1.2-2':'pt' }}</h4></div>
                    </div>

                    <div class="card-footer">
                        <a class="btn btn-primary" [routerLink]="['/carrinho',produto.id]">
                            <span class="fa fa-shopping-cart"></span> Comprar
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>

receber os dados e gerar uma Lista em ListaProdutoComponent.ts

    import { Component, OnInit } from '@angular/core';

    import { Produto } from '../produto';
    import { ProdutoService } from '../produtos.service';

    @Component({
    selector: 'app-lista-produto',
    templateUrl: './lista-produto.component.html'
    })
    export class ListaProdutoComponent implements OnInit {

    constructor(private produtoService: ProdutoService) { }

    public produtos: Produto[];

    ngOnInit() {
        this.produtoService.obterProdutos()
        .subscribe(
            produtos => {
            this.produtos = produtos;
            console.log(produtos);
            },
            error => console.log(error)
        );
    }
    }


adicionar o suporte HttpClient no modulo app.module.ts

    import { HttpClientModule } from '@angular/common/http';

    imports: [
        BrowserModule,
        FormsModule,
        HttpClientModule,
        [RouterModule.forRoot(rootRouterConfig, { useHash: false})]
      ],

class app.module.ts

    import { BrowserModule } from '@angular/platform-browser';
    import { NgModule } from '@angular/core';
    import { RouterModule } from '@angular/router';
    import { APP_BASE_HREF } from '@angular/common';
    import { FormsModule }   from '@angular/forms';
    import { HttpClientModule } from '@angular/common/http';

    import { registerLocaleData } from '@angular/common';
    import localePt from '@angular/common/locales/pt';
    registerLocaleData(localePt);

    import { AppComponent } from './app.component';
    import { MenuComponent } from './navegacao/menu/menu.component';
    import { HomeComponent } from './navegacao/home/home.component';
    import { FooterComponent } from './navegacao/footer/footer.component';
    import { SobreComponent } from './institucional/sobre/sobre.component';
    import { ContatoComponent } from './institucional/contato/contato.component';
    import { rootRouterConfig } from './app.routes';
    import { DataBindingComponent } from './demos/data-binding/data-binding.component';
    import { ProdutoService } from './produtos/produtos.service';
    import { ListaProdutoComponent } from './produtos/lista-produto/lista-produto.component';

    @NgModule({
    declarations: [
        AppComponent,
        MenuComponent,
        HomeComponent,
        FooterComponent,
        SobreComponent,
        ContatoComponent,
        DataBindingComponent,
        ListaProdutoComponent
    ],
    imports: [
        BrowserModule,
        FormsModule,
        HttpClientModule,
        [RouterModule.forRoot(rootRouterConfig, { useHash: false})]
    ],
    providers: [
        ProdutoService,
        {provide: APP_BASE_HREF, useValue: '/'}
    ],
    bootstrap: [AppComponent]
    })
    export class AppModule { }

informar os dados de cada Produto usando interpoletion

    <h4 class="card-title">{{ produto.nome | titlecase }}</h4>

    <div [ngSwitch]="produto.promocao">
        <p *ngSwitchCase="true">Promoção!</p>
        <p *ngSwitchCase="false">Por apenas:</p>
    </div>

    <div *ngIf="produto.promocao" class="card-body">
        <div><h4 class="card-text">De:
            <small><del>{{ produto.valor | currency:'BRL':true:'1.2-2':'pt' }}</del></small>
            Por: {{ produto.valorPromo | currency:'BRL':true:'1.2-2':'pt' }}
        </h4></div>
    </div>

lista-Produto.component.Html 

    <div class="container main-container">

        <div class="row text-center">
            
            <div *ngFor="let produto of produtos" class="col-md-4" style="padding-bottom: 30px;">
                <div class="card h-100">
                    <a class="text-decoration-none" [routerLink]="['/produto-detalhe', produto.id]">
                        <div style="align-content:center;">
                            <img src="/assets/{{ produto.imagem }}" height="164px" width="253px" alt="">
                        </div>
                    </a>
                    <h4 class="card-title">{{ produto.nome | titlecase }}</h4>

                    <div [ngSwitch]="produto.promocao">
                        <p *ngSwitchCase="true">Promoção!</p>
                        <p *ngSwitchCase="false">Por apenas:</p>
                    </div>

                    <div *ngIf="produto.promocao" class="card-body">
                        <div><h4 class="card-text">De:
                            <small><del>{{ produto.valor | currency:'BRL':true:'1.2-2':'pt' }}</del></small>
                            Por: {{ produto.valorPromo | currency:'BRL':true:'1.2-2':'pt' }}
                        </h4></div>
                    </div>

                    <div *ngIf="!produto.promocao" class="card-body">
                        <div><h4>{{ produto.valor | currency:'BRL':true:'1.2-2':'pt' }}</h4></div>
                    </div>

                    <div class="card-footer">
                        <a class="btn btn-primary" [routerLink]="['/carrinho',produto.id]">
                            <span class="fa fa-shopping-cart"></span> Comprar
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>

  
