<script>
    import List, {Item, Text, Graphic, Separator, Subheader} from '@smui/list';
    export let currentPage;
    export let itemList = [];
</script>
<List>
    {#each itemList as item,index (item.text)}
        <Item href="javascript:void(0)" on:click={
            function() {
                currentPage = item;
            }
        } activated={item.activated}>
            <Graphic class="material-icons" aria-hidden="true">{item.icon}</Graphic>
            <Text>{item.text}</Text>
        </Item>
    {/each}
</List>
