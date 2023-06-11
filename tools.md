---
layout: page
titles:
  # @start locale config
  en      : &EN       Thoughts
  en-GB   : *EN
  en-US   : *EN
  en-CA   : *EN
  en-AU   : *EN
  zh-Hans : &ZH_HANS  随想录
  zh      : *ZH_HANS
  zh-CN   : *ZH_HANS
  zh-SG   : *ZH_HANS
  zh-Hant : &ZH_HANT  隨想錄
  zh-TW   : *ZH_HANT
  zh-HK   : *ZH_HANT
  ko      : &KO       아이디어
  ko-KR   : *KO
  fr      : &FR       Pensées
  fr-BE   : *FR
  fr-CA   : *FR
  fr-CH   : *FR
  fr-FR   : *FR
  fr-LU   : *FR
  # @end locale config
mode: immersive
article_header:
  type: overlay
  theme: dark
  background_image: 
    src: https://ts1.cn.mm.bing.net/th/id/R-C.2f4c6399fdca966b3230b64ad3f6b051?rik=sPVNDRJw%2fWtXeg&riu=http%3a%2f%2fpic101.huitu.com%2fpic%2f20171111%2f617553_20171111151045739050_0.jpg&ehk=DP2w86l%2b06BhQIjcDk3KYojhl6kqDXYuABeU%2fXFx%2fao%3d&risl=&pid=ImgRaw&r=0&sres=1&sresct=1
sidebar:
    nav: tools
---
## Editor.md
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

