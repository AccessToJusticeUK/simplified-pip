<template>
    <div class="section">
        <section>
            <header>
                <h1>{{ header }}</h1>
                <small>{{ description }}</small>
            </header>
            <div class="form">
                <p>Form goes here</p>
            </div>
            <footer>
                {{ pageNumber }}
            </footer>
        </section>
        <aside>
            {{ aside }}
        </aside>
    </div>
</template>

<script>
export default {
  name: 'Section',
  props: {
    header: String,
    description: String,
    pageNumber: Number
  }
}
</script>

<style scoped lang="scss">
    $grey-colour: rgb(102, 102, 102);
    $border-colour: rgb(210, 210, 210);

    div.section {
        background-color: white;
        margin-bottom: 37px;
        height: 1100px;
        width: 780px;
        -webkit-box-shadow: 5px 5px 10px rgba(204, 204, 204, 0.349019607843137);
        -moz-box-shadow: 5px 5px 10px rgba(204, 204, 204, 0.349019607843137);
        box-shadow: 5px 5px 10px rgba(204, 204, 204, 0.349019607843137);
    }

    section {
        display: flex;
        flex-direction: column;
        padding: 50px;

        & > header {
            color: $grey-colour;

            & > h1 {
                border-bottom: 1px solid $border-colour;
            }
        }

        footer {
            align-self: flex-end;
            text-align: right;
        }
    }
</style>
