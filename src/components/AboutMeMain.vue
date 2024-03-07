<template>
    <div id = 'about' class = 'wrapper'>
    <div id="timeline">
        <div class="title">
            <h2 class = 'software'> About Me</h2>
            <div class="timeline">
                <div class="checkpoint">
                    <div>
                        <h3 class="cph3">
                            Abit more about me!
                        </h3>
                        <p class="cpWords">
                            My journey towards becoming a software engineer commenced during my A-levels in 2020. It was in this academic phase that I discovered my passion for coding. Intrigued by the possibilities, I immersed myself in learning Python, initiating a series of home projects to hone my coding skills and delve deeper into the world of software development.
                        </p>
                    </div>
                </div>

                <div class="checkpoint">
                    <div>
                        <h3 class="cph3">
                            Why software engineering?
                        </h3>
                        <p class="cpWords">
                            After two years of dedicated effort, I successfully completed my A-levels and secured admission to Newcastle University, where I enrolled in the Computer Science program with a specialization in software engineering. During my first year, I delved into fundamental courses such as Computing, Computer Systems Design, and Architectures, and Foundations of Data Science. Engaging in numerous projects, including a large-scale collaborative effort, broadened my skill set and provided invaluable practical experience.
                        </p>
                    </div>
                </div>

                <div class="checkpoint">
                    <div>
                        <h3 class="cph3">
                            What's next?
                        </h3>
                        <p class="cpWords">
                            In the period from March 2023 to May 2023, I embarked on a virtual internship, focusing on app development. Following a comprehensive app flowchart, my team and I designed a work productivity app using Flutter. This hands-on experience not only enhanced my understanding of software development processes but also reinforced my commitment to continuous learning and practical application of skills gained in academic settings.
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

</style>