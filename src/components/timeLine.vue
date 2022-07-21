<template>
    <div class="main">
        <div class="head">Step to Step</div>
        <div class="container">
            <ul>
                <li>
                    <h3 class="heading">FrontEnd Developer</h3>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fugit excepturi accusamus minus
                        totam </p>
                    <a href="#">Read More ></a>

                </li>
                <li>
                    <h3 class="heading">BackEnd Developer</h3>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fugit excepturi accusamus minus
                        totam </p>
                    <a href="#">Read More ></a>

                 
                </li>
                <li>
                    <h3 class="heading">Full Stack Developer</h3>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fugit excepturi accusamus minus
                        totam </p>
                    <a href="#">Read More ></a>
                  
                </li>
                <li>
                    <h3 class="heading">App Developer</h3>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fugit excepturi accusamus minus
                        totam </p>
                    <a href="#">Read More ></a>
                   
                </li>
                <li>
                    <h3 class="heading">App Developer</h3>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fugit excepturi accusamus minus
                        totam </p>
                    <a href="#">Read More ></a>
                  
                </li>
            </ul>
        </div>
    </div>
</template>

<script setup>


</script>


<style>
.main {
    width: 100%;
    height: auto;
    display: grid;
    place-items: center;
    background-color: var(--vt-c-black);
}

.main .head {
    font-size: 30px;
    color: var(--vt-c-green);
    position: relative;
    margin-top: 35px;
    margin-bottom: 55px;
}


/* Container Css Start  */

.container {
    width: 50%;
    height: auto;
    margin: auto 0;
    margin-bottom: 63px;
    position: relative;
}

.container ul {
    list-style: none;
}

.container ul::after {
    content: " ";
    position: absolute;
    width: 2px;
    height: 100%;
    left: 50%;
    top: 0;
    transform: translateX(-50%);
    background-image: linear-gradient(to bottom, var(--vt-c-green), var(--vt-c-indigo));
}

.container ul li {
    width: 50%;
    height: auto;
    padding: 15px 20px;
    background-color: rgb(32, 32, 32);
    border-radius: 8px;
    box-shadow: 1px 1px 15px rgba(0, 0, 0, 0.218);
    position: relative;
    margin-bottom: 30px;
    z-index: 99;
}

.container ul li:nth-child(4) {
    margin-bottom: 0;
}

.container ul li .circle {
    position: absolute;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background-color: #e100ff7a;
    top: 0;
    display: grid;
    place-items: center;
}

.circle::after {
    content: ' ';
    width: 12px;
    height: 12px;
    background-color: #7f00ff;
    border-radius: 50%;
}

ul li:nth-child(odd) .circle {
    transform: translate(50%, -50%);
    right: -30px;
}

ul li:nth-child(even) .circle {
    transform: translate(-50%, -50%);
    left: -30px;
}

ul li .date {
    position: absolute;
    width: 130px;
    height: 33px;
    background-image: linear-gradient(to right, #7f00ff, #e100ff);
    border-radius: 15px;
    top: -45px;
    display: grid;
    place-items: center;
    color: #fff;
    font-size: 13px;
    box-shadow: 1px 2px 12px rgba(0, 0, 0, 0.318);
}

.container ul li:nth-child(odd) {
    float: left;
    clear: right;
    text-align: right;
    transform: translateX(-30px);
}

ul li:nth-child(odd) .date {
    right: 20px;
}

.container ul li:nth-child(even) {
    float: right;
    clear: left;
    transform: translateX(-10px);
}

ul li .heading {
    font-size: 17px;
    color: rgb(91, 14, 216);
}

ul li p {
    font-size: 13px;
    color: #666;
    line-height: 18px;
    margin: 6px 0 4px 0;
}

ul li a {
    font-size: 13px;
    text-decoration: none;
    color: rgb(18, 54, 214);
    transition: all 0.3s ease;
}


@media only screen and (min-width:798px) and (max-width: 1100px) {
    .container {
        width: 80%;
    }
}

@media only screen and (max-width: 798px) {
    .container {
        width: 70%;
        transform: translateX(20px);
    }

    .container ul::after {
        left: -40px;
    }

    .container ul li {
        width: 100%;
        float: none;
        clear: none;
        margin-bottom: 80px;
    }

    .container ul li .circle {
        left: -40px;
        transform: translate(-50%, -50%);
    }

    .container ul li .date {
        left: 20px;
    }

    .container ul li:nth-child(odd) {
        transform: translateX(0px);
        text-align: left;
    }

    .container ul li:nth-child(even) {
        transform: translateX(0px);
    }
}

@media only screen and (max-width: 550px) {
    .container {
        width: 80%;
    }

    .container ul::after {
        left: -20px;
    }

    .container ul li .circle {
        left: -20px;
    }
}
</style>