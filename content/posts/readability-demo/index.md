---
slug: "readability-demo"
title: "Readability Demo"
subtitle: "Rewriting text to any comprehension level or length"
date: 2023-07-16T14:03:53-05:00
draft: false
---

# About this demo
- Select the article from the dropdown below
- Set the reading *level* and *length*
- Read why and how I made this demo in my [full post here](/posts/readability).

<!--begin-->

<script>
    function updateText() {
        var art = document.getElementById('demo-article').value;
        var lev_v = document.getElementById('demo-lev').value;
        var len_v = document.getElementById('demo-len').value;
        var lev = Object.keys(LEVEL)[lev_v];
        var len = Object.keys(LENGTH)[len_v];

        Array.from(document.querySelectorAll('div.slide-show')).forEach(
            div => { div.classList.remove('slide-show'); });
        console.log(art + '-' + lev + '-' + len);
        document.getElementById(art + '-' + lev + '-' + len).classList.add('slide-show');
    }
</script>

<style>

    #demo-form {
        border:1px solid #dda;
        padding:0.5em;
        background:#ffe;
        margin-bottom:2em;
    }

    .slide-pane {
        display: none;
    }

    .slide-param {
        border-bottom: 1px solid #0594cb;
        height:2em;
        padding: 0;
        margin: 1em 0;
    }

    .slide-param-lev {
        font-size:1.2em;
        float:left;
        font-weight:bold;
    }

    .slide-param-len {
        clear:both;
        float:right;
        margin-top:0.5em;
        margin-bottom:2em;
    }

    .slide-body {
        clear:both;
        margin: 0;
        padding: 0.5em 1em;
        border-left: 4px solid #0594cb;
        background: #eee;
    }

    .slide-show {
        display: block !important;
    }
</style>

{{% include "autogen.md" %}}

<script>
    updateText();
</script>