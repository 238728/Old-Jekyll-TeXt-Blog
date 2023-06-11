---
layout: page
title: Editor.md
permalink: /tools/editor.md
modify_date: 2023-06-11
pageview: false   
sidebar:
    nav: tools
---
<!DOCTYPE=html>
<link rel="stylesheet" href="/editormd/css/editormd.css" />
<div id="test-editor">
    <textarea style="display:none;"></textarea>
</div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
<script src="/editormd/editormd.min.js"></script>
<script type="text/javascript">
    $(function() {
        var editor = editormd("test-editor", {
            mode: "markdown",
            width: "100%",
            height: 640,
            emoji: true,
            tex: true,          // TeX(LaTeX), based on KaTeX
            flowChart: true,          // flowChart.js only support IE9+
            sequenceDiagram: true,          // sequenceDiagram.js only support IE9+
            placeholder: "Edit Markdown...",
            previewCodeHighlight: true,   
            path: "/editormd/lib/"
        });
    });
</script>
