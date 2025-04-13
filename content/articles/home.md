+++
date = '2025-04-12T09:12:44-06:00'
draft = true
title = 'Articles'
+++

{{< my_shortcode.inline >}}

<pre>
{{ $v1 := 6 }}
{{ $v2 := 7 }}
The product of {{ $v1 }} and {{ $v2 }} is {{ mul $v1 $v2 }}.
</pre>

{{< /my_shortcode.inline >}}