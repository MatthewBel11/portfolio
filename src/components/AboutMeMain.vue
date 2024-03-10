<template>
    <div id = 'about' class = 'wrapper'>
    <div id="timeline">
        <div class="title">
            <h2 class = 'software'> About Me</h2>
            <div class="timeline">
                <div class="checkpoint">
                    <div>
                        <h3 class="cph3">
                            Why software engineering?
                        </h3>
                        <p class="cpWords">
                            After four years of dedicated study, I'm on the cusp of graduating as a Junior Software Engineer. Why? Simply put, I have an unbridled passion for creating things. 
                            Whether it's assembling a flatpack dining table at Ikea or crafting a fully responsive portfolio website, the joy of making is my driving force.

                            Yet, it's not just about the act of creating. Mathematics and challenges hold a special place in my heart, competing for the top spot alongside my love for making things. 
                            When you merge these three elements, you get the beautiful concoction known as Software Engineering. Well, pretty much...
                        </p>
                    </div>
                </div>

                <div class="checkpoint">
                    <div>
                        <h3 class="cph3">
                            What's next?
                        </h3>
                        <p class="cpWords">
                            fter completing this website, I've set my sights on two main goals. Firstly, I aim to gain industry experience—whether through a placement year,
                            volunteer work, or an internship. My objective is to expand my skill set and truly understand what it's like to work as an engineer.

                            Secondly, I'm working on enhancing my skills at home by pursuing online certificates such as Microsoft Azure Fundamentals,
                            all while engaging in personal projects. Currently, I'm focused on honing my Vue.js skills to create a website that is deliberately perplexing.
                            For instance, if you want to enter your phone number, get ready to roll a dice for each digit! The challenge is part of the fun.
                        </p>
                    </div>
                </div>

                <div class="checkpoint">
                    <div>
                        <h3 class="cph3">
                            Need to know stuff about me
                        </h3>
                        <p class="cpWords">
                            Personally, I believe a person's favorite movie or song speaks volumes about them. So, to offer you a glimpse into my favorites, the current song on endless replay is:
                             <a class='cpLink' href='https://open.spotify.com/track/3zdtYfRqOn1axEmHZTWivp?si=8d6bb69acb364a28'>Foreplay by Jalen Santoy</a>.
                              If you have the time, I'd wholeheartedly recommend giving it a listen.

                            Now, shifting gears to the film realm, fair warning - my favorite movie is the cliché but utterly captivating 'Dune 2.' Those three hours had me hooked,
                            and as soon as the credits rolled, the only thought on my mind was getting another ticket to watch it again. I think that speaks for itself.


                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    </div>
</template>

<style>


.title{
    margin-top: 10%;
    text-align: center;
    color: azure;
}

@media (max-width: 360px) {
    .software{
        font-size: 120%;
    }
}


.timeline{
    margin: 5em auto;
    max-width: 34em;
}

.checkpoint{
    max-width: 34em;
    padding-top: 2em;
    padding-bottom: 2em;
    position: relative;
}

.cpWords{
    position: relative;
    line-break: auto;
    overflow: hidden;
}

.checkpoint div{
    border: 2px solid #888;
    border-radius: 1em;
    padding: 1.5em;
}

.checkpoint p {
    line-height: 27px;
    color: #c5c5c5;
}

.checkpoint:nth-child(odd){
    border-left: 3px solid #888;
    padding-left: 3em;
    transform: translateX(16.9em);
}

.checkpoint:nth-child(even){
    border-right: 3px solid #888;
    padding-right: 3em;
    transform: translateX(-16.9em);
}

.checkpoint:nth-child(odd)::before,
.checkpoint:nth-child(even)::before {
    content: '';
    background: #888;
    width: 2.9em;
    height: 3px;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
}

.checkpoint:nth-child(odd)::before{
    left: 0;
}

.checkpoint:nth-child(even)::before{
    right: 0;
}

.checkpoint:nth-child(odd) div::before,
.checkpoint:nth-child(even) div::before {
    content: '';
    background: #888;
    width: 0.8em;
    height: 0.8em;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    border-radius: 50%;
}

.checkpoint:nth-child(odd) div::before{
    left: -0.5em;
}

.checkpoint:nth-child(even) div::before{
    right: -0.5em;
}

@media screen and (max-width: 1150px){
    .timeline{
        width: 80vw;
    }

    .timeline .checkpoint{
        width: 100%;
        transform: none;
        padding-left: 0;
        padding-right: 0;
        border: none;
    }

    .timeline .checkpoint::before{
        width: 3px;
        height: 4em;
        top: -2em;
        left: 50%;
        transform: translateX(-50%);
    }

    .timeline .checkpoint div::before{
        top: -0.5em;
        left: 50%;
        transform: translateX(-50%);

    }
}

    .cpLink{
        text-decoration: none;
        color: #6d6262;
    }

    .cpLink:hover{
        color: rgb(202, 202, 202);
    }

</style>