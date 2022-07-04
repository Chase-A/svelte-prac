<script>
    export let margined = false;
    let expanded = true	
    let orientation = ''
    function handleClick(){
        expanded = !expanded
        expanded ? orientation = 'transform: rotate(0deg)': orientation = 'transform: rotate(180deg)'
    }
    </script>

<section style={margined && 'margin: 15px 8px'}>
    <div class='top-bar'>
        <h1>title</h1>
        <button class='arrow' on:click={handleClick} style={orientation}>^</button>
        </div>
        {#if expanded}
        <p class='text'>
            Ut Lorem officia sit aliquip adipisicing. Esse incididunt officia reprehenderit dolor ad adipisicing sit mollit occaecat cillum sunt quis aute. Magna ut occaecat mollit non nulla consequat irure enim consectetur culpa id nulla do.
        </p>
        {/if}
    </section>
    
    <style>
        

        section{
            border: 4px solid #000;
            position: relative;
            text-align: left;
            box-shadow: 5px 5px #000;
            padding: 5px;
            border-radius: 14px;
            background-color: rgba(250, 128, 114, 0.356);
        }
        h1{
            padding: .25rem;
        }
        .top-bar{
            display: flex;
            justify-content: space-between;
            width: 100%;
        }
        .arrow{
            font-size: 1.5rem;
            font-weight: 900;
            position: relative;
            right: .25rem;
            border: none;
            background: none;
            transform-origin: 7px 12px;
        }
        .text{
            padding: .25rem;
        }
    </style>