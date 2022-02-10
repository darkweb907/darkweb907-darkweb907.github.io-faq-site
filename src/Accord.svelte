<script>
    export let question;
    export let answer;
    export let img;
    let family= true;
</script>
<div class=  "faq">
        <div class="accord">
            <div class="accord-head">
                <h3> {question}</h3>
                <span style="align-self: center;" on:click="{()=>{family= !family}}"><img class:rotate={family} src="{img}" alt="arrow" ></span> 
            </div>
            <div class="accord-text" class:family={family}>
                <p>{answer}</p>
            </div>
        </div>
</div>
<style>
    span{ 
        cursor: pointer;
    }
    
    .accord{
        border-radius: 8px;
        border-bottom: 1px solid hsl(240, 5%, 91%);
        text-align: start;
    }
 .accord-head{
        display:flex;
        justify-content:space-between;
    }
     .rotate{
     transform: rotate(180deg);
    } 
    .family{
        display:none;
    }
</style>