# Monografia TEP — Protocolo de Notas e Referências

## Big Picture

<a href="referencial/big_picture_tcc_tep.svg">
  <img src="referencial/big_picture_tcc_tep.svg" alt="Big picture da monografia TEP">
</a>

> Clique na imagem para abrir a versão interativa — cada card navega para a nota correspondente.

---

> TESTE
<svg width="100%" viewBox="0 0 680 1180" role="img" style="" xmlns="http://www.w3.org/2000/svg">
<title style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">Narrativa do TCC: do problema do TEP ao CPS proposto</title>
<desc style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">Cadeia argumentativa mostrando como cada referência contribui para a proposta de supervisão via Kubernetes, do problema original até os limites honestos da implementação</desc>
<defs>
  <marker id="arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
    <path d="M2 1L8 5L2 9" fill="none" stroke="context-stroke" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
  </marker>
<mask id="imagine-text-gaps-ul1xh6" maskUnits="userSpaceOnUse"><rect x="0" y="0" width="680" height="1180" fill="white"/><rect x="264.921875" y="31" width="150.45086669921875" height="22" fill="black" rx="2"/><rect x="203.421875" y="50.5" width="274.5936279296875" height="19" fill="black" rx="2"/><rect x="237.3671875" y="78" width="204.74176025390625" height="19" fill="black" rx="2"/><rect x="273.140625" y="107" width="133.53485107421875" height="22" fill="black" rx="2"/><rect x="142.9140625" y="143" width="113.65988159179688" height="22" fill="black" rx="2"/><rect x="139.46875" y="162.5" width="121.11181640625" height="19" fill="black" rx="2"/><rect x="426.9375" y="143" width="126.41986083984375" height="22" fill="black" rx="2"/><rect x="414.53125" y="162.5" width="151.76983642578125" height="19" fill="black" rx="2"/><rect x="227.484375" y="190" width="224.5057373046875" height="19" fill="black" rx="2"/><rect x="269.3515625" y="219" width="142.075927734375" height="22" fill="black" rx="2"/><rect x="141.796875" y="255" width="115.89985656738281" height="22" fill="black" rx="2"/><rect x="137.09375" y="274.5" width="125.8125" height="19" fill="black" rx="2"/><rect x="430.234375" y="255" width="120.3839111328125" height="22" fill="black" rx="2"/><rect x="427.96875" y="274.5" width="125.10980224609375" height="19" fill="black" rx="2"/><rect x="213.8515625" y="302" width="251.77569580078125" height="19" fill="black" rx="2"/><rect x="281.1484375" y="331" width="117.93185424804688" height="22" fill="black" rx="2"/><rect x="136.125" y="367" width="127.0418701171875" height="22" fill="black" rx="2"/><rect x="126.796875" y="386.5" width="146.2337646484375" height="19" fill="black" rx="2"/><rect x="417.0703125" y="367" width="146.08685302734375" height="22" fill="black" rx="2"/><rect x="416.15625" y="386.5" width="148.80377197265625" height="19" fill="black" rx="2"/><rect x="211.1328125" y="414" width="257.2236328125" height="19" fill="black" rx="2"/><rect x="267.9765625" y="443" width="143.81787109375" height="22" fill="black" rx="2"/><rect x="64.515625" y="477" width="94.46591186523438" height="22" fill="black" rx="2"/><rect x="56.171875" y="496.5" width="112.13986206054688" height="19" fill="black" rx="2"/><rect x="220.828125" y="477" width="92.64495849609375" height="22" fill="black" rx="2"/><rect x="195.8984375" y="496.5" width="143.6318359375" height="19" fill="black" rx="2"/><rect x="370.125" y="477" width="103.03887939453125" height="22" fill="black" rx="2"/><rect x="358.9609375" y="496.5" width="126.04586791992188" height="19" fill="black" rx="2"/><rect x="524.625" y="477" width="104.046875" height="22" fill="black" rx="2"/><rect x="513.9453125" y="496.5" width="125.94384765625" height="19" fill="black" rx="2"/><rect x="238.2109375" y="545" width="203.86782836914062" height="22" fill="black" rx="2"/><rect x="257.8515625" y="564.5" width="164.1337890625" height="19" fill="black" rx="2"/><rect x="218.59375" y="592" width="242.28961181640625" height="19" fill="black" rx="2"/><rect x="241.6484375" y="639" width="196.29681396484375" height="22" fill="black" rx="2"/><rect x="274.390625" y="658.5" width="132.22586059570312" height="19" fill="black" rx="2"/><rect x="231.9296875" y="686" width="215.61968994140625" height="19" fill="black" rx="2"/><rect x="250.921875" y="733" width="178.755859375" height="22" fill="black" rx="2"/><rect x="227.1328125" y="752.5" width="225.73968505859375" height="19" fill="black" rx="2"/><rect x="246.453125" y="780" width="187.5777587890625" height="19" fill="black" rx="2"/><rect x="210.59375" y="827" width="259.3397216796875" height="22" fill="black" rx="2"/><rect x="231.7265625" y="846.5" width="217.51171875" height="19" fill="black" rx="2"/><rect x="196.3984375" y="874" width="286.6835632324219" height="19" fill="black" rx="2"/><rect x="275.7265625" y="903" width="128.9208984375" height="22" fill="black" rx="2"/><rect x="97.8515625" y="939" width="174.9578857421875" height="22" fill="black" rx="2"/><rect x="83.53125" y="958.5" width="202.76174926757812" height="19" fill="black" rx="2"/><rect x="393.828125" y="939" width="202.34375" height="22" fill="black" rx="2"/><rect x="419.5546875" y="958.5" width="150.93182373046875" height="19" fill="black" rx="2"/><rect x="187.625" y="1033" width="304.76373291015625" height="22" fill="black" rx="2"/><rect x="220.734375" y="1052.5" width="238.45965576171875" height="19" fill="black" rx="2"/><rect x="182.7109375" y="1128.5" width="314.7335205078125" height="19" fill="black" rx="2"/></mask></defs>


<a href="notes/ft_A-Plantwide-Industrial-Process-Control-Problem.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="180" y="20" width="320" height="56" rx="8" stroke-width="0.5" style="fill:rgb(250, 236, 231);stroke:rgb(153, 60, 29);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="340" y="42" text-anchor="middle" dominant-baseline="central" style="fill:rgb(113, 43, 19);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Downs &amp; Vogel (1993)</text>
  <text x="340" y="60" text-anchor="middle" dominant-baseline="central" style="fill:rgb(153, 60, 29);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">problema_supervisao — o TEP força a pergunta</text>
</g>
</a>

<line x1="340" y1="76" x2="340" y2="100" marker-end="url(#arrow)" mask="url(#imagine-text-gaps-ul1xh6)" style="fill:none;stroke:rgb(115, 114, 108);color:rgb(0, 0, 0);stroke-width:1.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
<text x="340" y="92" text-anchor="middle" style="fill:rgb(165, 163, 156);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:auto">quem decide como a planta opera?</text>


<text x="340" y="118" text-anchor="middle" dominant-baseline="central" style="fill:rgb(210, 207, 198);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">analogia_fundante</text>
<a href="notes/ft_Cloud-Native-Computing-A-Survey-from-the-Perspective-of-Services_Shuiguang_et_al.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="60" y="132" width="280" height="56" rx="8" stroke-width="0.5" style="fill:rgb(238, 237, 254);stroke:rgb(83, 74, 183);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="200" y="154" text-anchor="middle" dominant-baseline="central" style="fill:rgb(60, 52, 137);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Shuiguang et al.</text>
  <text x="200" y="172" text-anchor="middle" dominant-baseline="central" style="fill:rgb(83, 74, 183);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">survey cloud-native</text>
</g>
</a>
<a href="notes/ft_Borg-Omega-and-Kubernetes.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="350" y="132" width="280" height="56" rx="8" stroke-width="0.5" style="fill:rgb(238, 237, 254);stroke:rgb(83, 74, 183);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="490" y="154" text-anchor="middle" dominant-baseline="central" style="fill:rgb(60, 52, 137);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Burns et al. (2016)</text>
  <text x="490" y="172" text-anchor="middle" dominant-baseline="central" style="fill:rgb(83, 74, 183);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">Borg, Omega, Kubernetes</text>
</g>
</a>

<line x1="340" y1="188" x2="340" y2="212" marker-end="url(#arrow)" mask="url(#imagine-text-gaps-ul1xh6)" style="fill:none;stroke:rgb(115, 114, 108);color:rgb(0, 0, 0);stroke-width:1.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
<text x="340" y="204" text-anchor="middle" style="fill:rgb(165, 163, 156);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:auto">a comunidade já fez algo mais ousado?</text>


<text x="340" y="230" text-anchor="middle" dominant-baseline="central" style="fill:rgb(210, 207, 198);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">precedente_ousado</text>
<a href="notes/ft_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="60" y="244" width="280" height="56" rx="8" stroke-width="0.5" style="fill:rgb(238, 237, 254);stroke:rgb(83, 74, 183);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="200" y="266" text-anchor="middle" dominant-baseline="central" style="fill:rgb(60, 52, 137);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Johansson et al.</text>
  <text x="200" y="284" text-anchor="middle" dominant-baseline="central" style="fill:rgb(83, 74, 183);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">K8s orquestra VDCN</text>
</g>
</a>
<a href="notes/ft_Design-of-an-IoT-PLC_Mellado_Nunez.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="350" y="244" width="280" height="56" rx="8" stroke-width="0.5" style="fill:rgb(238, 237, 254);stroke:rgb(83, 74, 183);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="490" y="266" text-anchor="middle" dominant-baseline="central" style="fill:rgb(60, 52, 137);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Mellado &amp; Núñez</text>
  <text x="490" y="284" text-anchor="middle" dominant-baseline="central" style="fill:rgb(83, 74, 183);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">IoT-PLC cloud-native</text>
</g>
</a>

<line x1="340" y1="300" x2="340" y2="324" marker-end="url(#arrow)" mask="url(#imagine-text-gaps-ul1xh6)" style="fill:none;stroke:rgb(115, 114, 108);color:rgb(0, 0, 0);stroke-width:1.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
<text x="340" y="316" text-anchor="middle" style="fill:rgb(165, 163, 156);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:auto">é viável — mas o que o supervisor observa?</text>


<text x="340" y="342" text-anchor="middle" dominant-baseline="central" style="fill:rgb(210, 207, 198);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">espirito_politica</text>
<a href="notes/ft_Control-Structure-Desing-for-Complete-Chemical-Plants.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="60" y="356" width="280" height="56" rx="8" stroke-width="0.5" style="fill:rgb(225, 245, 238);stroke:rgb(15, 110, 86);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="200" y="378" text-anchor="middle" dominant-baseline="central" style="fill:rgb(8, 80, 65);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Skogestad (2004)</text>
  <text x="200" y="396" text-anchor="middle" dominant-baseline="central" style="fill:rgb(15, 110, 86);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">control structure design</text>
</g>
</a>
<a href="notes/ft_Plantwide-Control-A-Review-and-a-new-Design-Procedure.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="350" y="356" width="280" height="56" rx="8" stroke-width="0.5" style="fill:rgb(225, 245, 238);stroke:rgb(15, 110, 86);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="490" y="378" text-anchor="middle" dominant-baseline="central" style="fill:rgb(8, 80, 65);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Larsson &amp; Skogestad</text>
  <text x="490" y="396" text-anchor="middle" dominant-baseline="central" style="fill:rgb(15, 110, 86);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">plantwide control review</text>
</g>
</a>

<line x1="340" y1="412" x2="340" y2="436" marker-end="url(#arrow)" mask="url(#imagine-text-gaps-ul1xh6)" style="fill:none;stroke:rgb(115, 114, 108);color:rgb(0, 0, 0);stroke-width:1.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
<text x="340" y="428" text-anchor="middle" style="fill:rgb(165, 163, 156);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:auto">como saber se a planta está fora da política?</text>


<text x="340" y="454" text-anchor="middle" dominant-baseline="central" style="fill:rgb(210, 207, 198);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">tecnica_diagnostico</text>
<a href="notes/ft_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="40" y="468" width="145" height="56" rx="8" stroke-width="0.5" style="fill:rgb(225, 245, 238);stroke:rgb(15, 110, 86);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="112" y="488" text-anchor="middle" dominant-baseline="central" style="fill:rgb(8, 80, 65);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Viñuela et al.</text>
  <text x="112" y="506" text-anchor="middle" dominant-baseline="central" style="fill:rgb(15, 110, 86);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">malha controlada?</text>
</g>
</a>
<a href="notes/ft_Assessment-of-Control-Loop-Performance.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="195" y="468" width="145" height="56" rx="8" stroke-width="0.5" style="fill:rgb(225, 245, 238);stroke:rgb(15, 110, 86);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="267" y="488" text-anchor="middle" dominant-baseline="central" style="fill:rgb(8, 80, 65);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Harris (1989)</text>
  <text x="267" y="506" text-anchor="middle" dominant-baseline="central" style="fill:rgb(15, 110, 86);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">benchmark de variância</text>
</g>
</a>
<a href="notes/ft_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="350" y="468" width="145" height="56" rx="8" stroke-width="0.5" style="fill:rgb(225, 245, 238);stroke:rgb(15, 110, 86);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="422" y="488" text-anchor="middle" dominant-baseline="central" style="fill:rgb(8, 80, 65);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Tilaro et al. (a)</text>
  <text x="422" y="506" text-anchor="middle" dominant-baseline="central" style="fill:rgb(15, 110, 86);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">oscilação observável</text>
</g>
</a>
<a href="notes/ft_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="505" y="468" width="145" height="56" rx="8" stroke-width="0.5" style="fill:rgb(225, 245, 238);stroke:rgb(15, 110, 86);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="577" y="488" text-anchor="middle" dominant-baseline="central" style="fill:rgb(8, 80, 65);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Tilaro et al. (b)</text>
  <text x="577" y="506" text-anchor="middle" dominant-baseline="central" style="fill:rgb(15, 110, 86);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">clusters de sensores</text>
</g>
</a>
<a href="notes/ft_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="195" y="534" width="290" height="56" rx="8" stroke-width="0.5" style="fill:rgb(225, 245, 238);stroke:rgb(15, 110, 86);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="340" y="556" text-anchor="middle" dominant-baseline="central" style="fill:rgb(8, 80, 65);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Lessmeier et al. (+ IC própria)</text>
  <text x="340" y="574" text-anchor="middle" dominant-baseline="central" style="fill:rgb(15, 110, 86);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">telemetria online de avarias</text>
</g>
</a>

<line x1="340" y1="590" x2="340" y2="614" marker-end="url(#arrow)" mask="url(#imagine-text-gaps-ul1xh6)" style="fill:none;stroke:rgb(115, 114, 108);color:rgb(0, 0, 0);stroke-width:1.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
<text x="340" y="606" text-anchor="middle" style="fill:rgb(165, 163, 156);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:auto">e como abstrair o PLC num objeto virtual?</text>


<a href="notes/ft_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="180" y="628" width="320" height="56" rx="8" stroke-width="0.5" style="fill:rgb(250, 238, 218);stroke:rgb(133, 79, 11);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="340" y="650" text-anchor="middle" dominant-baseline="central" style="fill:rgb(99, 56, 6);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Gayet &amp; Barillère — UNICOS</text>
  <text x="340" y="668" text-anchor="middle" dominant-baseline="central" style="fill:rgb(133, 79, 11);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">plataforma_abstracao</text>
</g>
</a>

<line x1="340" y1="684" x2="340" y2="708" marker-end="url(#arrow)" mask="url(#imagine-text-gaps-ul1xh6)" style="fill:none;stroke:rgb(115, 114, 108);color:rgb(0, 0, 0);stroke-width:1.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
<text x="340" y="700" text-anchor="middle" style="fill:rgb(165, 163, 156);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:auto">tudo isso aponta para qual conceito?</text>


<a href="notes/ft_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="160" y="722" width="360" height="56" rx="8" stroke-width="0.5" style="fill:rgb(250, 236, 231);stroke:rgb(153, 60, 29);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="340" y="744" text-anchor="middle" dominant-baseline="central" style="fill:rgb(113, 43, 19);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Hehenberger et al. — CPS</text>
  <text x="340" y="762" text-anchor="middle" dominant-baseline="central" style="fill:rgb(153, 60, 29);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">conceito_cps — o que estou propondo</text>
</g>
</a>

<line x1="340" y1="778" x2="340" y2="802" marker-end="url(#arrow)" mask="url(#imagine-text-gaps-ul1xh6)" style="fill:none;stroke:rgb(115, 114, 108);color:rgb(0, 0, 0);stroke-width:1.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
<text x="340" y="794" text-anchor="middle" style="fill:rgb(165, 163, 156);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:auto">mas o que eu de fato entreguei?</text>


<a href="notes/ft_DigitalTwin-Mechatronic-Futures_Hehenberger_Bradley.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="160" y="816" width="360" height="56" rx="8" stroke-width="0.5" style="fill:rgb(241, 239, 232);stroke:rgb(95, 94, 90);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="340" y="838" text-anchor="middle" dominant-baseline="central" style="fill:rgb(68, 68, 65);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Hehenberger &amp; Bradley — Digital Twin</text>
  <text x="340" y="856" text-anchor="middle" dominant-baseline="central" style="fill:rgb(95, 94, 90);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">limite_honesto — não é gêmeo digital</text>
</g>
</a>

<line x1="340" y1="872" x2="340" y2="896" marker-end="url(#arrow)" mask="url(#imagine-text-gaps-ul1xh6)" style="fill:none;stroke:rgb(115, 114, 108);color:rgb(0, 0, 0);stroke-width:1.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
<text x="340" y="888" text-anchor="middle" style="fill:rgb(165, 163, 156);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:auto">como formalizar as fronteiras entre subsistemas?</text>


<text x="340" y="914" text-anchor="middle" dominant-baseline="central" style="fill:rgb(210, 207, 198);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">integracao_formal</text>
<a href="notes/ft_OPC-UA-System-Architecture_Mahnke_Leitner_Damm.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="40" y="928" width="290" height="56" rx="8" stroke-width="0.5" style="fill:rgb(230, 241, 251);stroke:rgb(24, 95, 165);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="185" y="950" text-anchor="middle" dominant-baseline="central" style="fill:rgb(12, 68, 124);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">Mahnke, Leitner &amp; Damm</text>
  <text x="185" y="968" text-anchor="middle" dominant-baseline="central" style="fill:rgb(24, 95, 165);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">OPC-UA — System Arch., Services</text>
</g>
</a>
<a href="notes/ft_IEC_62541-1.md" target="_top" style="cursor:pointer">
<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="350" y="928" width="290" height="56" rx="8" stroke-width="0.5" style="fill:rgb(230, 241, 251);stroke:rgb(24, 95, 165);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="495" y="950" text-anchor="middle" dominant-baseline="central" style="fill:rgb(12, 68, 124);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">IEC 62541 (1,3,8) · IEC 62264-1</text>
  <text x="495" y="968" text-anchor="middle" dominant-baseline="central" style="fill:rgb(24, 95, 165);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">OPC-UA · modelo Purdue</text>
</g>
</a>

<line x1="340" y1="984" x2="340" y2="1008" marker-end="url(#arrow)" style="fill:none;stroke:rgb(115, 114, 108);color:rgb(0, 0, 0);stroke-width:1.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>


<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="100" y="1022" width="480" height="56" rx="8" stroke-width="0.5" style="fill:rgb(250, 236, 231);stroke:rgb(153, 60, 29);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="340" y="1044" text-anchor="middle" dominant-baseline="central" style="fill:rgb(113, 43, 19);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:14px;font-weight:500;text-anchor:middle;dominant-baseline:central">TEP modernizado: Fortran → serviço em Rust</text>
  <text x="340" y="1062" text-anchor="middle" dominant-baseline="central" style="fill:rgb(153, 60, 29);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">substrato verificável da proposta de CPS</text>
</g>

<line x1="340" y1="1078" x2="340" y2="1102" marker-end="url(#arrow)" style="fill:none;stroke:rgb(115, 114, 108);color:rgb(0, 0, 0);stroke-width:1.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>

<g style="fill:rgb(0, 0, 0);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto">
  <rect x="140" y="1116" width="400" height="44" rx="8" stroke-width="0.5" style="fill:rgb(241, 239, 232);stroke:rgb(95, 94, 90);color:rgb(0, 0, 0);stroke-width:0.5px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:16px;font-weight:400;text-anchor:start;dominant-baseline:auto"/>
  <text x="340" y="1138" text-anchor="middle" dominant-baseline="central" style="fill:rgb(95, 94, 90);stroke:none;color:rgb(0, 0, 0);stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;opacity:1;font-family:&quot;Anthropic Sans&quot;, -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, sans-serif;font-size:12px;font-weight:400;text-anchor:middle;dominant-baseline:central">trabalho futuro: supervisor Kubernetes real + OPC-UA</text>
</g>

</svg>



## Inventário de Referências

### Artigos

| Título                                                                                     | Autores                                                              | Ano  | Periódico / Conferência                                 |
| ------------------------------------------------------------------------------------------ | -------------------------------------------------------------------- | ---- | ------------------------------------------------------- |
| A plant-wide industrial process control problem                                            | Downs, J.J.; Vogel, E.F.                                             | 1993 | Computers & Chemical Engineering, v.17, n.3             |
| An expert knowledge based methodology for online detection of signal oscillations          | Tilaro, F.; Bradu, B.; Gonzalez-Berges, M.; Roshchin, M.             | 2017 | CIVEMSA 2017                                            |
| Assessment of control loop performance                                                     | Harris, T.J.                                                         | 1989 | The Canadian Journal of Chemical Engineering, v.67, n.5 |
| Automatic PID performance monitoring applied to LHC cryogenics                             | Bradu, B.; Blanco Viñuela, E.; Marti, R.; Tilaro, F.                 | 2018 | ICALEPCS 2017 (proc. 2018)                              |
| Borg, Omega, and Kubernetes                                                                | Burns, B.; Grant, B.; Oppenheimer, D.; Brewer, E.; Wilkes, J.        | 2016 | ACM Queue, v.14                                         |
| Cloud-Native Computing: A Survey from the Perspective of Services                          | Deng, S. et al.                                                      | 2023 | arXiv:2306.14402                                        |
| Condition monitoring of bearing damage in electromechanical drive systems                  | Lessmeier, C.; Kimotho, J.K.; Zimmer, D.; Sextro, W.                 | 2016 | PHME 2016                                               |
| Control structure design for complete chemical plants                                      | Skogestad, S.                                                        | 2004 | Computers & Chemical Engineering, v.28, n.1             |
| Design of an IoT-PLC: A containerized programmable logical controller for the Industry 4.0 | Mellado, J.; Núñez, F.                                               | 2022 | Journal of Industrial Information Integration, v.25     |
| Kubernetes orchestration of high availability distributed control systems                  | Johansson, B.; Rågberger, M.; Nolte, T.; Papadopoulos, A.V.          | 2022 | IEEE ICIT 2022                                          |
| Model learning algorithms for anomaly detection in CERN control systems                    | Tilaro, F.; Bradu, B.; Gonzalez-Berges, M.; Varela, F.; Roshchin, M. | 2018 | ICALEPCS 2017 (proc. 2018)                              |
| Plantwide control — a review and a new design procedure                                    | Larsson, T.; Skogestad, S.                                           | 2000 | Modeling, Identification and Control, v.21              |
| UNICOS — a framework to build industry-like control systems                                | Gayet; Barillère                                                     | —    | CERN internal                                           |

### Normas

| Norma       | Título                                                                 | Organização          | Edição         |
| ----------- | ---------------------------------------------------------------------- | -------------------- | -------------- |
| IEC 62541-1 | OPC Unified Architecture — Part 1: Overview and concepts               | IEC / OPC Foundation | 2025           |
| IEC 62541-3 | OPC Unified Architecture — Part 3: Address space model                 | IEC / OPC Foundation | 2025 (ed. 4.0) |
| IEC 62541-8 | OPC Unified Architecture — Part 8: Data access                         | IEC / OPC Foundation | 2025 (ed. 4.0) |
| IEC 62264-1 | Enterprise-Control System Integration — Part 1: Models and terminology | IEC                  | 2013 (ed. 2.0) |

### Livros / Capítulos

| Título                               | Autores                    | Ano  | Livro / Editora                                              |
| ------------------------------------ | -------------------------- | ---- | ------------------------------------------------------------ |
| Digital Twin — The Simulation Aspect | Boschert, S.; Rosen, R.    | 2016 | Mechatronic Futures (Hehenberger & Bradley, Eds.) — Springer |
| \[capítulo CPS\]                     | Hehenberger et al.         | 2016 | Mechatronic Futures (Hehenberger & Bradley, Eds.) — Springer |
| Introduction                         | Mahnke, W.; Leitner, S.-H. | 2009 | OPC Unified Architecture — Springer                          |
| Services                             | Mahnke, W.; Leitner, S.-H. | 2009 | OPC Unified Architecture — Springer                          |
| System Architecture                  | Mahnke, W.; Leitner, S.-H. | 2009 | OPC Unified Architecture — Springer                          |

**Resumo:** 13 artigos + 4 normas + 5 capítulos = **22 notas de fonte**

---

## Estrutura do referencial (`referencial/`)

```
referencial/
├── articles/           # PDFs de artigos vinculados via Annotator
├── bibTex/             # arquivos .bib de cada fonte
├── books/              # PDFs de livros
├── notes/
│   ├── .obsidian/      # vault Obsidian (plugins, graph, temas)
│   └── ft_*.md         # notas de fonte
├── standard/           # PDFs de normas
└── big_picture_tcc_tep.svg
```

O vault do Obsidian está em `referencial/notes/`. Abra essa pasta no Obsidian, não a raiz do repositório.

---

## O campo `tags` — papel de cada fonte no argumento

Cada nota de fonte (`ft_`) carrega no frontmatter um campo `tags` que indica **onde aquela fonte se encaixa no argumento da monografia**. Os valores são tags nativas do Obsidian — aparecem no painel de tags e colorem os nós no Graph View.

| Tag                    | Papel no argumento                                                            |
| ---------------------- | ----------------------------------------------------------------------------- |
| `problema_supervisao`  | Ponto de partida — o TEP obriga a perguntar como controlar uma planta inteira |
| `analogia_fundante`    | Cloud-native resolve o mesmo problema de orquestração em escala               |
| `precedente_ousado`    | Trabalhos que já usaram Kubernetes / containers em contexto industrial real   |
| `espirito_politica`    | Teoria de como estruturar decisões de controle numa planta completa           |
| `tecnica_diagnostico`  | Como detectar que a planta saiu da política — o olho do supervisor            |
| `plataforma_abstracao` | Frameworks que abstraem ativos físicos em objetos de software (ex: UNICOS)    |
| `conceito_cps`         | Fundamento conceitual do Cyber-Physical System — o que estou propondo         |
| `limite_honesto`       | O que de fato foi entregue, sem exagerar o alcance (≠ gêmeo digital)          |
| `integracao_formal`    | Normas e protocolos que formalizam as interfaces entre subsistemas            |

**Exemplo de frontmatter:**

```yaml
---
annotation-target: articles/art1_...pdf
titulo: A plant-wide industrial process control problem
autor: Downs, J.J.; Vogel, E.F.
ano: 1993
fonte: Computers & Chemical Engineering, v.17, n.3
tags: problema_supervisao
---
```

---

## Graph View — Grupos por Tag

Configure em **Settings → Graph view → Groups** com filtros no formato `tag:#<valor>`:

| Grupo                  | Filtro no Obsidian          | Cor sugerida |
| ---------------------- | --------------------------- | ------------ |
| `problema_supervisao`  | `tag:#problema_supervisao`  | Vermelho     |
| `analogia_fundante`    | `tag:#analogia_fundante`    | Roxo         |
| `precedente_ousado`    | `tag:#precedente_ousado`    | Roxo claro   |
| `espirito_politica`    | `tag:#espirito_politica`    | Verde        |
| `tecnica_diagnostico`  | `tag:#tecnica_diagnostico`  | Verde claro  |
| `plataforma_abstracao` | `tag:#plataforma_abstracao` | Laranja      |
| `conceito_cps`         | `tag:#conceito_cps`         | Vermelho     |
| `limite_honesto`       | `tag:#limite_honesto`       | Cinza        |
| `integracao_formal`    | `tag:#integracao_formal`    | Azul         |

---

## Protocolo de Tags de Insight

Dentro das notas de fonte, highlights individuais podem receber tags **no corpo da nota** no formato `TIPO-TEMA-POLARIDADE`. Essas tags vinculam fragmentos de conhecimento entre artigos diferentes — dois highlights de fontes distintas com a mesma tag formam uma aresta no grafo.

> Diferença importante: o campo `tags` no frontmatter classifica a **fonte como um todo**. As tags de insight no corpo classificam **fragmentos específicos**.

### Tipo

| Tipo        | Quando usar                                               |
| ----------- | --------------------------------------------------------- |
| `TRADEOFF`  | Melhorar X implica piorar Y — tensão entre dois objetivos |
| `LIMITE`    | Teto ou piso teórico que nenhuma solução consegue superar |
| `PARADOXO`  | Resultado contraria a intuição                            |
| `REQUISITO` | Condição necessária para outra coisa funcionar            |
| `MECANISMO` | Explica *por que* algo acontece — a causa, não o efeito   |
| `METRICA`   | Define uma forma de medir, avaliar ou comparar algo       |

### Tema

| Tema                    | Quando usar                                                           |
| ----------------------- | --------------------------------------------------------------------- |
| `CONTROLE_AUTOMATICO`   | Malhas PID, sintonia, resposta a distúrbios, estabilidade             |
| `SISTEMAS_DINAMICOS`    | Modelagem matemática, equações diferenciais, análise de comportamento |
| `SUPERVISAO`            | Camada acima dos loops — decisão, coordenação, metacontrole           |
| `DIAGNOSTICO`           | Detecção de falhas, sensores ruins, malhas degradadas                 |
| `INSTRUMENTACAO`        | Sensores, atuadores, condicionamento de sinal                         |
| `INTEGRACAO_INDUSTRIAL` | Interoperabilidade entre componentes de controle                      |
| `COMUNICACAO`           | Protocolos, latência, gRPC, OPC-UA, troca de dados                    |
| `MODELAGEM`             | Gêmeo digital, simulação, representação matemática da planta          |
| `CALCULO_NUMERICO`      | Métodos numéricos, precisão e estabilidade                            |
| `SOFTWARE`              | Arquitetura, frameworks, tooling                                      |
| `BENCHMARKING`          | Índices de desempenho, limites teóricos, comparação entre soluções    |

### Polaridade

| Polaridade | Quando usar                                           |
| ---------- | ----------------------------------------------------- |
| `POSITIVO` | Reforça ou justifica uma decisão do projeto           |
| `NEGATIVO` | Contradiz, limita ou critica uma decisão do projeto   |
| `NEUTRO`   | Relevante mas sem posição clara em relação ao projeto |

**Formato final:** `TIPO-TEMA-POLARIDADE` — ex: `TRADEOFF-CONTROLE_AUTOMATICO-NEGATIVO`

---

## Os Quatro Tipos de Nota

### 1. Nota de Fonte (`ft_`)

**Quando usar:** Sempre que estiver lendo um artigo, livro ou seção de norma. Vincula o PDF via Annotator.

**Convenção de nome:** `ft_<titulo-resumido>.md`

**Frontmatter obrigatório:**

```yaml
---
annotation-target: articles/<arquivo>.pdf
titulo: <título completo>
autor: <autores>
ano: <ano>
fonte: <periódico / editora / norma>
tags: <valor da tag>
---
```

---

### 2. Nota Atômica de Conceito (`nt_`)

**Quando usar:** Quando aprende um conceito novo — uma ideia, um método, uma definição. Uma nota por conceito.

**Convenção de nome:** `nt_<conceito>.md`

**Protocolo de escrita:**
1. `conceito` — nome do conceito em uma ou duas palavras
2. `origem` — nota `ft_` de onde veio (ex: `[[ft_Assessment-of-Control-Loop-Performance]]`)
3. `conecta-com` — outros conceitos relacionados, mesmo sem saber como ainda
4. `## O que é` — apenas uma frase direta
5. `## Como se conecta ao projeto` — onde isso aparece no TCC

---

### 3. Documentação do Projeto (`doc_`)

**Quando usar:** Para registrar decisões de arquitetura, descrições de componentes, resultados de experimentos.

**Convenção de nome:** `doc_<componente>_<assunto>.md`

**Protocolo de escrita:**
1. Preencha o frontmatter (componente, relates-to)
2. Seja objetivo — este é um registro técnico, não um diário
3. Sempre termine com `## Próximos passos` ou `## Problemas em aberto`

---

### 4. Brainstorming (`bs_`)

**Quando usar:** Quando uma ideia surge e você não sabe ainda onde ela se encaixa.

**Convenção de nome:** `bs_<tema>_<data>.md`

**Protocolo de escrita:**
1. Escreva sem filtro em `## Ideia bruta`
2. Depois tente responder: "Isso vai para qual capítulo da monografia?"
3. Se souber, linke o capítulo correspondente; se não, deixe `status: incubando`

---

## Infraestrutura Obsidian

Para instruções sobre setup de plugins, como usar o Annotator, e convenções do Obsidian, ver: **[`docs/doc_obsidian_setup.md`](docs/doc_obsidian_setup.md)**
