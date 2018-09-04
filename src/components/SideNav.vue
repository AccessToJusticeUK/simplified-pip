<template>
    <div class="sidenav">
        <header>
            <div class="highlight">
                <h1>Simplified PiP</h1>
                <small>For agencies assisting clients</small>
            </div>
        </header>
        <nav class="buttons">
            <button type="button">Print</button>
            <button type="button">Tips</button>
        </nav>
        <nav class="navigation">
            <ul>
                <li class="active">Section 1</li>
                <li>Section 2 – About your health condition or disability</li>
                <li>Section 3 – How your health condition or disability affects your day-to-day life</li>
                <li>Section 4 – What to do now</li>
            </ul>
        </nav>
    </div>
</template>

<style scoped lang="scss">
    $band-colour: rgb(255, 102, 2);

    div.sidenav {
        width: 250px;
        margin-right: 40px;
    }

    header {
        height: 95px;
        display: flex;
        align-items: center;

        & h1 {
            margin-bottom: 0.1em;
        }
    }

    div.highlight {
        border-left: 5px solid $band-colour;
        padding-left: 10px;
    }
</style>
