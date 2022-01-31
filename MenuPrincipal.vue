<template>
<section id="menu-principal">
    <div class="container">
    <nav>
        <ul>
            <li><a href="#">INICIO</a></li>
            <li><a href="#">HOMBRE</a></li>
            <li><a href="#">MUJER</a></li>
            <li><a href="#">NIÑO</a></li>
            <li><a href="#">OUTLET</a></li>
            <li><a href="#">CLUBES</a></li>
        </ul>
    </nav>
    <div class=grupo>
        <a class="registro" href="#">REGISTRO</a>
        <a class="login" href="#">INICIAR SESIÓN</a>
    </div>
</div>
</section>
  
</template>

<script>
export default {
}
</script>

<style>
section#menu-principal {
    background: black;
    z-index:999;
    padding:0.7rem;
}
section#menu-principal .container {
    display: flex;
    justify-content: space-between;
}
section#menu-principal .container nav ul {
    display:flex;
    list-style: none;
    padding: 0;
    margin:0rem 0.7rem;
}
section#menu-principal .container nav ul li a, .registro:hover, .login:hover{
    background-color: black;
    text-decoration: none;
    color:white;
    font-weight: 700;
    padding-left: 1rem;
    padding-right: 1rem;
}
section#menu-principal .container nav ul li a:hover,.active, .registro, .login {
    background-color:black;
    text-decoration: none;
    color:white;
    font-weight: 700;
    padding: 1rem;
}
</style>