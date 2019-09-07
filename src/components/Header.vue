<template>
    <header>
      <b-container>
        <nav class="navbar navbar-light navbar-expand-md">
          <img id="home" src="../assets/logo.svg" alt="Bakery">

          <button type="button" aria-label="Toggle navigation" aria-controls="nav-collapse" aria-expanded="false" class="navbar-toggler">
            <span class="navbar-toggler-icon"></span>
          </button>

          <div id="nav-collapse" class="navbar-collapse collapse">
            <ul class="navbar-nav ml-auto">
              <li ><a href="#home"      >HOME</a></li>
              <li ><a href="#about"     >SOBRE</a></li>
              <li ><a href="#products"  >RECEITAS</a></li>
              <li ><a href="#news"      >NOTÍCIAS</a></li>
              <li ><a href="#contact"   >CONTATO</a></li>
              <li ><a href="#" ><img src="../assets/search-solid.svg" alt="Procura"></a></li>
            </ul>
          </div>
        </nav>
      </b-container>
    </header>
</template>

<style scoped lang="scss">

.container{
  padding: 0px;

  .navbar{
    padding: 0.5rem .6rem;

    #home{
      height: 102px;
    }

    .navbar-nav{
      margin-top:20px;

      li{
      
        a{
          color: #515151;
          @media (min-width:992px) { padding: .45rem 2.15rem;}
          @media not all and (min-width:992px) {padding: .45rem .9rem;}
          font-size: 0.85rem;
          font-weight: 900;
          margin-left: 16px;
          margin-right: 2px;
          outline: none;

          &:hover {
            color: #a67b52;
            text-decoration: none;
          }
        }

        &:last-child a{
          border-left: 0.9px solid grey;
          padding-right: 5px;
          margin-left: 4px;

          img{
            height: 17px;
          }
        }
      }
    }
  }
}

</style>
