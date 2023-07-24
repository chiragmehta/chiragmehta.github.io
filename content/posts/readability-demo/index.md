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
- Read why and how I made this [here](/posts/readability).

<script>
    function updateText() {
        var art = document.getElementById('demo-article').value;

        if(!document.querySelector('input[name="demo-lev"]:checked'))
            document.getElementsByName('demo-lev')[0].checked = true;
        var lev = document.querySelector('input[name="demo-lev"]:checked').value;

        if(!document.querySelector('input[name="demo-len"]:checked'))
            document.getElementsByName('demo-len')[0].checked = true;
        var len = document.querySelector('input[name="demo-len"]:checked').value;

        Array.from(document.querySelectorAll('div.slide-show')).forEach(
            div => { div.classList.remove('slide-show'); });
        console.log(art + '-' + lev + '-' + len);
        document.getElementById(art + '-' + lev + '-' + len).classList.add('slide-show');
    }
</script>

<style>

    div.tip, .toc {
        display:none;
    }

    h1#read-params {
        margin-bottom:0;
    }

    #demo-form {
        border:1px solid #dda;
        padding:0;
        background:#ffe;
        margin-bottom:2em;
    }

    #demo-form div.row {
        margin:1em 0.5em;
    }

    #demo-form label.col {
        min-width:25%;
    }

    #demo-form select#demo-article {
        font-size:1.2em;
        width:75%;
        max-width:75%;
    }

    #demo-form .radio-btn {
        display: inline-block;
        margin:0;
        margin-right:6px;
        cursor: pointer;
    }

    #demo-form .radio-btn input {
        display: none;
    }

    #demo-form .radio-btn span {
        padding: 0.5em;
        font-size:0.9em;
        border: 1px solid #5badf0;
        color: #333;
        background-color: #fff;
        transition: background-color .2s;
    }

    #demo-form .radio-btn input:checked + span {
        background-color: #5badf0;
        color: #fff;
    }

    .slide-pane {
        display: none;
    }

    .slide-param {
        padding: 0;
        margin: 1em 0 3em;
    }

    .slide-param-art {
        font-size:1.5em;
        text-align:center;
        font-weight:bold;
        border-bottom: 1px solid #0594cb;
    }

    .slide-param-lev {
        font-size:0.9em;
        color:#666;
        float:left;
    }

    .slide-param-len {
        font-size:0.9em;
        color:#666;
        float:right;
    }

    .slide-show {
        display: block !important;
    }

    .slide-body {
        clear:both;
        margin: 0;
        padding: 0.5em 1em;
        border-left: 4px solid #0594cb;
        background: #eee;
    }

    .slide-body h1 {
        font-size:1.3em;
        color:#000;
    }

    .slide-body h1:first-child {
        margin-top:0.2em;
    }

    .slide-body h2 {
        font-size:1.15em;
        font-weight:normal;
        color:#000;
    }

    .slide-body h3 {
        padding-left:1em;
        font-size:1em;
        font-weight:bold;
        color:#000;
    }

    .slide-body p {
        padding-left:1em;
    }

    @media only screen and (max-width: 400px) {
        #single .content,  #single .content > h1 {
            margin:0;
        }
        .slide-param {
            margin:1em 0;
        }
        .slide-param-lev, .slide-param-len {
            text-align:center;
            float:inherit;
        }
    }


</style>

{{% include "autogen.md" %}}

<script>
    updateText();
</script>

<!--begin-->