<!-- <script context="module" ✂prettier:content✂="CiAgICBpbXBvcnQgZnMgZnJvbSAiZnMiOwogICAgY29uc3QgZGlyID0gZnMucmVhZGRpcigpOwo=" ✂prettier:content✂="e30=" ✂prettier:content✂="e30=" ✂prettier:content✂="e30=" ✂prettier:content✂="e30=" ✂prettier:content✂="e30=" ✂prettier:content✂="e30=">{}</script> -->
<script>
    import Folder from "./Folder.svelte";
    // export let dir;
    const tree = __dirname;
    const folders = tree.split("/");
    let root = [
        {
            type: "folder",
            name: "Important work stuff",
            files: [{ type: "file", name: "quarterly-results.xlsx" }],
        },
        {
            type: "folder",
            name: "Animal GIFs",
            files: [
                {
                    type: "folder",
                    name: "Dogs",
                    files: [
                        { type: "file", name: "treadmill.gif" },
                        { type: "file", name: "rope-jumping.gif" },
                    ],
                },
                {
                    type: "folder",
                    name: "Goats",
                    files: [
                        { type: "file", name: "parkour.gif" },
                        { type: "file", name: "rampage.gif" },
                    ],
                },
                { type: "file", name: "cat-roomba.gif" },
                { type: "file", name: "duck-shuffle.gif" },
                { type: "file", name: "monkey-on-a-pig.gif" },
            ],
        },
        { type: "file", name: "TODO.md" },
    ];
</script>

<p>{folders.length}</p>
<Folder name="ici" files={folders} extended />
<p>
    {#each folders as folder}
        <span>{folder}<br /></span>
    {/each}
</p>

<Folder name="Home" files={root} expanded />
