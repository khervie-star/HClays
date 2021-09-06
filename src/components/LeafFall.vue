<template>
    <div id="leaves">
        <i><img src="../assets/leaves/1634105.png" width="50%"></i>
        <i><img src="../assets/leaves/309723.png" width="50%"></i>
        <i><img src="../assets/leaves/1674790.png" width="50%"></i>
        <i><img src="../assets/leaves/309723.png" width="50%"></i>
        <i><img src="../assets/leaves/1634105.png" width="50%"></i>
        <i><img src="../assets/leaves/309723.png" width="50%"></i>
        <i><img src="../assets/leaves/1634105.png" width="50%"></i>
        <i><img src="../assets/leaves/2038350.png" width="50%"></i>
        <i><img src="../assets/leaves/1634105.png" width="50%"></i>
        <i><img src="../assets/leaves/309723.png" width="50%"></i>
        <i><img src="../assets/leaves/1634105.png" width="50%"></i>
        <i><img src="../assets/leaves/307150.png" width="50%"></i>
        <i><img src="../assets/leaves/2038350.png" width="50%"></i>
        <i><img src="../assets/leaves/1634105.png" width="50%"></i>
        <i><img src="../assets/leaves/2038350.png" width="50%"></i>
        <i><img src="../assets/leaves/1634105.png" width="50%"></i>
        <i><img src="../assets/leaves/2038350.png" width="50%"></i>
        <i><img src="../assets/leaves/1634105.png" width="50%"></i>
        <i><img src="../assets/leaves/2038350.png" width="50%"></i>
        <i><img src="../assets/leaves/1634105.png" width="50%"></i>
        <i><img src="../assets/leaves/2038350.png" width="50%"></i>
      </div>
</template>


<style scoped>

#leaves {position: fixed;top: -100px;width:100%;text-align: right; z-index: 100;}

#leaves i {
    margin-left: 50px;
    display: inline-block;
    background-color: transparent;
    transform: skew(20deg); 
    z-index: 1;
    -webkit-animation: falling 5s 0s infinite;
}

#leaves i img{
    width: 60px;
    height: 50px;
}

#leaves i:nth-of-type(2n) { -webkit-animation: falling2 5s 0s infinite; }
#leaves i:nth-of-type(3n) { -webkit-animation: falling3 5s 0s infinite; }



i:nth-of-type(n)    { height:23px; width:30px; }
i:nth-of-type(n):before { width:7px; height:5px; top:17px; right:1px; }
i:nth-of-type(n):after { width:2px; height:17px; left: 12px; top:0px; }

i:nth-of-type(2n+1)    { height:11px; width:16px; }
i:nth-of-type(2n+1):before { width:4px; height:3px; top:7px; right:0px; }
i:nth-of-type(2n+1):after { width:2px; height:6px; left: 5px; top:1px; }

i:nth-of-type(3n+2)  { height:17px; width:23px; }
i:nth-of-type(3n+2):before  { height:4px; width:4px; top:12px; right:1px; }
i:nth-of-type(3n+2):after  { height:10px; width:2px; top:1px; left:8px; }

#leaves i:nth-of-type(n)   { -webkit-animation-delay: 1.9s;}
#leaves i:nth-of-type(2n)  { -webkit-animation-delay: 3.9s;}
#leaves i:nth-of-type(3n)  { -webkit-animation-delay: 2.3s;}
#leaves i:nth-of-type(4n)  { -webkit-animation-delay: 4.4s;}
#leaves i:nth-of-type(5n)  { -webkit-animation-delay: 5s;  }
#leaves i:nth-of-type(6n)  { -webkit-animation-delay: 3.5s;}
#leaves i:nth-of-type(7n)  { -webkit-animation-delay: 2.8s;}
#leaves i:nth-of-type(8n)  { -webkit-animation-delay: 1.5s;}
#leaves i:nth-of-type(9n)  { -webkit-animation-delay: 3.3s;}
#leaves i:nth-of-type(10n) { -webkit-animation-delay: 2.5s;}
#leaves i:nth-of-type(11n) { -webkit-animation-delay: 1.2s;}
#leaves i:nth-of-type(12n) { -webkit-animation-delay: 4.1s;}
#leaves i:nth-of-type(13n) { -webkit-animation-delay: 1s;  }
#leaves i:nth-of-type(14n) { -webkit-animation-delay: 4.7s;}
#leaves i:nth-of-type(15n) { -webkit-animation-delay: 3s;  }

/* #leaves i img:nth-of-type(n)    { fill: red }
#leaves i img:nth-of-type(2n+2)  { fill: blue } */
#leaves i:nth-of-type(4n+1)  { fill: teal; }
 
#leaves i:nth-of-type(n)    { opacity: .7;}
#leaves i:nth-of-type(3n+1)  { opacity: .5;}
#leaves i:nth-of-type(3n+2)  { opacity: .3;}

#leaves i:nth-of-type(n)   {transform: rotate(180deg);}


#leaves i:nth-of-type(n), span:nth-of-type(n) { -webkit-animation-timing-function:ease-in-out;}

@-webkit-keyframes falling {
    
    0% {
        -webkit-transform:
            translate3d(300,0,0)
            rotate(0deg);
    }
    
    100% {
        -webkit-transform:
            translate3d(-350px,700px,0)
            rotate(90deg);
        opacity: 0;
    }
}

@-webkit-keyframes falling3 {
     0% {
        -webkit-transform:
            translate3d(0,0,0)
            rotate(-20deg);
    }
    
    100% {
        -webkit-transform:
            translate3d(-230px,640px,0)
            rotate(-70deg);
        opacity: 0;
    }
}

@-webkit-keyframes falling2 {
     0% {
        -webkit-transform:
            translate3d(0,0,0)
            rotate(90deg);
    }
    
    100% {
        -webkit-transform:
            translate3d(-400px,680px,0)
            rotate(0deg);
        opacity: 0;
    }
} 
</style>