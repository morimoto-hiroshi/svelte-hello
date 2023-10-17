<style>
    .sv-style {
        margin: 1em;
        padding: 1em;
        background-color: rgba(255,222,222,1);
        border: solid 1px orange;
    }
</style>

<script>
    //-- part1 --
    let color = "red";
    const changeColor = (() => {
        color = color === 'red' ? 'green' : 'red';
    });
    //-- part2 --
    let isShowContent = true;
    const changeShowContent = (() => {
        isShowContent = !isShowContent;
    })
</script>

<section class="sv-style">
    <h1>Svelteの場合</h1>
    <p style="color: {color}; font-size: 150%; font-weight: bold;">文字の色が変わります</p>
    <button on:click="{changeColor}">文字を{color === 'red' ? '緑色' : '赤色'}にする。</button>
</section>
<section class="sv-style">
    {#if isShowContent}
    <p>文字が消えたり、見えたり...</p>
    {/if}
    <button on:click="{changeShowContent}">文字が{isShowContent ? '消えます' : '表示されます'}。</button>
</section>
