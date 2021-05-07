<script>
    export let color = 'green';
    export let opacity;
    export let id;
</script>

<div class="block {color} {opacity}" id={id}>

</div>

<style>
    .block {
        width: 100px;
        height: 100px;
        border: 1px solid black;
    }
    .green{
    background-color: green;
    }
    .red{
        background-color: red;
    }
    .blue{
        background-color: blue;
    }
    .opacity{
        opacity: 1;
    }
    .notOpacity{
        opacity: 0;
    }
</style>