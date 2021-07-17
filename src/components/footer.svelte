<script>
    let date = new Date();
    let fullYear = date.getFullYear();
    let source = "https://github.com/AGhosh2020/The-SHA512-Hash-Generator";
</script>
<footer>
    <p>Copyright &copy; {fullYear} Aniruddha Ghosh</p>    
    <p>Font use in the website : Space Grotesk</p>
    <p>Available at : <a href="https://fonts.floriankarsten.com/space-grotesk" target="_blank">fonts.floriankarsten.com/space-grotesk</a></p>
    <div>
        The website code is an open source and it's code is published in
        <br>
        <a href={source} target="_blank" ><img src="img/GitHub_Logo.png" alt="GitHub"></a>
        <p>Click the GitHub Logo and it will open a new tab to the website source code of GitHub page</p>
    </div>
</footer>
<style>
    footer{
        text-align:center;
    }
    p{
        font-size:15px;
    }
    img{
        height:31px;
        width:70px;
    }
    div{
        display: inline;
    }
    :global(body.dark) img{
        filter: invert(100%);

    }
    :global(body.dark) a{
        color:white;
    }
    :global(body.dark) a:hover{
        color:rgba(255, 255, 255, 0.596);
    }
</style>
