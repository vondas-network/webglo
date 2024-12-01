<h3 align="center">
  <img height="60%" width="60%" src="https://github.com/cskonopka/WebGL-Ordinals/blob/main/webglo.png?raw=true"/>
</h3>

<p align="center"><em>decentralized video art on the Bitcoin blockchain</em></p>

# Overview
WebGL Ordinals is a project with the focus of hosting video art on the Bitcoin using the Ordinals protocol. Rendered using a web browser, an Ordinal version of glsl-canvas.js is used to render web graphics directly from the blockchain.

## Why is this important?

- OpenGL allows for high-fidelity graphics by working directly with the GPU. WebGL is the web version of OpenGL. If you’ve used a computer in the past 30 years, you’ve experienced OpenGL graphics. For example, Three.js is a user-friendly wrapper for WebGL.
- Empower others to push the limits of graphical possibilities on the Bitcoin blockchain.
- The size of a shader is small, which makes it great for inscribing. Technically, there is no size limitation to shaders that I know of.
- No external dependencies. HTML5 + Javascript is all you need.
- A HTML5 + WebGL website example inscription hasn’t happened yet.

# On-chain Files
| Inscription    | On-chain Content |
| -------- | ------- |
| glsl-canvas.js v0.2.8 | [link](https://ordinals.com/content/aeb29dfe6396589bd501f2be3478202a6ed75989cfc5ff49dd0d704b012c00eci0) |
| #11635450 | [link](https://ordinals.com/preview/5518d36079b3cc854dba0bd6497ec078fbaa996ebd53e908150c845d6a56a463i0) |
| #11637749 | [link](https://ordinals.com/preview/af030674ee65b6bd72e71b92ddb4edbeafbc47768e2e412b7ff2415097447a2ci0) |
| #11805310 | [link](https://ordinals.com/preview/5534cd7b566ba833e59ca5d5db3f15d97c2263992c031bb83c6383a1406892cai0) |
| #11875520 | [link](https://ordinals.com/preview/0d08c2461af5ddfe3cb7db121e02a802e34d890e2fab3a2fd13c19d4de1c555bi0) |
| #11875521 | [link](https://ordinals.com/preview/96fcddf6cc1bca7541fba5c3224e51219c982b3997a2d4be4f1eef35702f06adi0) |
| #11875522 | [link](https://ordinals.com/preview/b422d57f5dc33eb55d06e2679b46ba5a0dd1967907c6c3121a66934a4eaaffc1i0) |
| #11875523 | [link](https://ordinals.com/preview/eb25cd04c31abd750f7ee2e34f9def46ab969e38a490c5c7eab738d0c0fb1046i0) |
| #11875524 | [link](https://ordinals.com/preview/00dac7ca13b960240b84266837e1bc8f4bad619ed458b4306143638c9b26595fi0) |
| #11875525 | [link](https://ordinals.com/preview/3f838fb74263af62a32240844a5976ffdab0c4b182e5b4c1011111fd05f215e8i0) |
| #11875526 | [link](https://ordinals.com/preview/f0e8a5ec3af3d20328caee3ea71f8e5dee75ccb2ee9c1cb0e2ff93bd3be3bda0i0) |
| #12077747 | [link](https://ordinals.com/preview/948a98d723e268fd371381478cdaa4cfbd8a85e9c515ef49b2f9d6f1a95f2446i0) |
| #12077748 | [link](https://ordinals.com/preview/8fc62bc3f8835e32cdfcdeb1362411ab959f1649d1c55e6c284f3c5d6761d1dci0) |
| #12077749 | [link](https://ordinals.com/preview/e9311bca95daaa81f4081f890cf2bc9314576bf69b39f09ee88814e17c296de6i0) |
| #12077750 | [link](https://ordinals.com/preview/166e5b837b024fff451d09c2fa690054ac4d5fdf8dd5075529a30c64dd40fa3ai0) |
| #12077751 | [link](https://ordinals.com/preview/765dc276c6d8fd4e098cad5af409f79b5316230d59592af8c53f17df5ccd3481i0) |
| #12077752 | [link](https://ordinals.com/preview/137db8ca401499bdd142b51aa342531cc11638530ae3f09a15ae89526ebeb0a9i0) |
| #12077753 | [link](https://ordinals.com/preview/66c79249046140a133ed645eac800f6e6999edfc114b61d355a44b5916ff00f2i0) |
| #12077753 | [link](https://ordinals.com/preview/66c79249046140a133ed645eac800f6e6999edfc114b61d355a44b5916ff00f2i0) |
| #12077754 | [link](https://ordinals.com/preview/7f6af3ddd89c1ef94f3dd039d0febdabf8a32c3303fe9bb34d165ea96d89176ei0) |
| #12077755 | [link](https://ordinals.com/preview/5a7891cdf9795c896e633cb75e1e270385e52b7025316949b02d3312f8661c98i0) |
| #12102422 | [link](https://ordinals.com/preview/56cf52dd2bf2b97e21c5bf5c022360aa3fa93b72959143e54feb9aeed5dc76d8i0) |
| #12102423 | [link](https://ordinals.com/preview/9adee923231b5ed39a9c08d1bb5eb7e1ae575d42902f5264848a1e3246b8c598i0) |
| #12102424 | [link](https://ordinals.com/preview/2fbe24ceb06bc433d37321b47701644868cf877fda2d80923e0ed66a3c00a876i0) |
| #12102425 | [link](https://ordinals.com/preview/dda24ae020f4994f88d8274a64c8395acd1513cd7384dbd753e2a802d3864bf3i0) |
| #12102426 | [link](https://ordinals.com/preview/181bd2f56701a42053c816809ae62f77739982523ff5607ada0022799b91a6d9i0) |

# Tutorial

<h3 align="center">
  <img height="40%" width="40%" src="https://github.com/user-attachments/assets/b714c712-ca6c-4bd8-90ab-8fac983c3b95"/>
</h3>

## HTML5 Template
To start, I needed a working example which demonstrated how to run a WebGL example within a HTML5 file. The key was finding one that loads a _fragment shader_. Luckily, I found a working an [example](https://wolftype.github.io/200c/about/) from Pablo Colapinto that runs locally without any external dependencies. This example is pasted below.

``` html
<html>
<script type="text/javascript">

var GL;
var shaderId;
var vertexBuffer;
var indexBuffer;
var timer = 0;

function initWebGL(){
    // Get Canvas Element
    var canvas = document.getElementById("glcanvas");
    // Get A WebGL Context
    GL = canvas.getContext("webgl") || canvas.getContext("experimental-webgl");
    // Test for Success
    if (!GL) {
      alert("Unable to initialize WebGL. Your browser may not support it.");
    }
    // Set clear color to red, fully opaque
    GL.clearColor(1.0, 0.0, 0.0, 1.0);
    // Clear Screen
    GL.clear(GL.COLOR_BUFFER_BIT| GL.DEPTH_BUFFER_BIT);

    initShaderProgram();
    initBuffers();
}

function initShaderProgram(){

    //Create Program and Shaders
    shaderId = GL.createProgram();
    var vertId = GL.createShader(GL.VERTEX_SHADER);
    var fragId = GL.createShader(GL.FRAGMENT_SHADER);

    //Load Shader Source (source text are in scripts below)
    var vert = document.getElementById("vertScript").text;
    var frag = document.getElementById("fragScript").text;

    GL.shaderSource(vertId, vert);
    GL.shaderSource(fragId, frag);

    //Compile Shaders
    GL.compileShader(vertId);
    GL.compileShader(fragId);

    //Check Vertex Shader Compile Status
    if (!GL.getShaderParameter(vertId, GL.COMPILE_STATUS)) {  
        alert("Vertex Shader Compiler Error: " + GL.getShaderInfoLog(id));  
        GL.deleteShader(vertId);
        return null;  
    }

    //Check Fragment Shader Compile Status
    if (!GL.getShaderParameter(fragId, GL.COMPILE_STATUS)) {  
        alert("Fragment Shader Compiler Error: " + GL.getShaderInfoLog(id));  
        GL.deleteShader(fragId);
        return null;  
    }

    //Attach and Link Shaders
    GL.attachShader(shaderId, vertId);
    GL.attachShader(shaderId, fragId);
    GL.linkProgram(shaderId);

    //Check Shader Program Link Status
    if (!GL.getProgramParameter(shaderId, GL.LINK_STATUS)) {
      alert("Shader Linking Error: " + GL.getProgramInfoLog(shader));
    }     

}

function initBuffers(){

    //Some Vertex Data
    var vertices = new Float32Array( [
      -1.0, -1.0, 0.0,
      -1.0,  1.0, 0.0,
       1.0,  1.0, 0.0,
       1.0, -1.0, 0.0
    ]);
    //Create A Buffer
    vertexBuffer = GL.createBuffer();
    //Bind it to Array Buffer
    GL.bindBuffer(GL.ARRAY_BUFFER, vertexBuffer);
    //Allocate Space on GPU
    GL.bufferData(GL.ARRAY_BUFFER, vertices.byteLength, GL.STATIC_DRAW);
    //Copy Data Over, passing in offset
    GL.bufferSubData(GL.ARRAY_BUFFER, 0, vertices );

    //Some Index Data
    var indices = new Uint16Array([ 0,1,3,2 ]);
    //Create A Buffer
    indexBuffer = GL.createBuffer();
    //Bind it to Element Array Buffer
    GL.bindBuffer(GL.ELEMENT_ARRAY_BUFFER, indexBuffer);
    //Allocate Space on GPU
    GL.bufferData(GL.ELEMENT_ARRAY_BUFFER, indices.byteLength, GL.STATIC_DRAW);
    //Copy Data Over, passing in offset
    GL.bufferSubData(GL.ELEMENT_ARRAY_BUFFER, 0, indices );

}

//ANIMATION FUNCTION (to be passed a callback)  see also http://www.paulirish.com/2011/requestanimationframe-for-smart-animating/
window.requestAnimFrame = ( function() {
   
    //Find best option given current browser
    return  window.requestAnimationFrame || 
            window.webkitRequestAnimationFrame ||  
            window.mozRequestAnimationFrame || 
            window.oRequestAnimationFrame || 
            window.msRequestAnimationFrame ||
    
    // if none of the above, use non-native timeout method
    function(callback) {
      window.setTimeout(callback, 1000 / 60);
    };
  
  } ) (); 

function animationLoop(){
    // feedback loop requests new frame
    requestAnimFrame( animationLoop );
    // render function is defined below
    render(); 
}

function render(){
    timer+=.1;

    //Bind Shader
    GL.useProgram(shaderId);   
    //Update uniform variable on shader
    var uID = GL.getUniformLocation(shaderId, "uTime");
    GL.uniform1f(uID, timer);
    //Enable Position Attribute
    var attId = GL.getAttribLocation(shaderId, "position");
    GL.enableVertexAttribArray(attId);
    //Bind Vertex Buffer
    GL.bindBuffer(GL.ARRAY_BUFFER, vertexBuffer);
    ///Point to Attribute (loc, size, datatype, normalize, stride, offset)
    GL.vertexAttribPointer( attId, 3, GL.FLOAT, false, 0, 0);
    //Bind Index Buffer
    GL.bindBuffer(GL.ELEMENT_ARRAY_BUFFER, indexBuffer);
    //Draw!      --( mode, number_of_elements, data type, offset )
    GL.drawElements(GL.TRIANGLE_STRIP, 4, GL.UNSIGNED_SHORT, 0);
}

function start(){
    initWebGL();
    animationLoop();
}

</script>

<!-- VERTEX SHADER SOURCE -->
<script id="vertScript" type="text/glsl">

  #ifdef GL_ES
  precision lowp float;
  #endif

  attribute vec3 position; 

  void main(void) {
    gl_Position = vec4(position,1.0);
  }

</script>

<!-- FRAGMENT SHADER SOURCE -->

<script id="fragScript" type="text/glsl">
<!-- ADD GLSL SHADER CODE HERE -->
  #ifdef GL_ES
  precision lowp float;
  #endif

  #define PI 3.14159265359

  uniform float uTime;

  void main(void) {

    //divide pixel location by canvas width and height
    //to get values are now between 0.0 and 1.0
    vec2 st = gl_FragCoord.xy/vec2(640,480);
    //some fun functions for picking colors
    float r = sin(uTime+8.*PI*st.x);
    float g = fract( sin(3.*PI*st.y) );   
    float b = sin(uTime+PI*st.x*st.y);
    vec3 color = vec3(r,b,g);
    gl_FragColor = vec4(color,1.0);
  }
</script>

<body onload = start() >
<canvas id="glcanvas" width=640 height=480 style = "margin:auto; display:block"> 
 Oops, browser has no <code> canvas </code> tag support 
</canvas>
</body>

</html>
```

I look for the Fragment Shader section and removed the code from inside the _<script>_ tag. Below is what it should look like once you remove the code from the template.

``` html
...
<!-- FRAGMENT SHADER SOURCE -->
<script id="fragScript" type="text/glsl">
<!-- ADD GLSL SHADER CODE HERE -->
</script>
...
```

Then, I pasted my GLSL shader, or _Fragment Shader_, into the area where it says Add GLSL Shader Code here.

``` javascript
<!-- FRAGMENT SHADER SOURCE -->
<script id="fragScript" type="text/glsl">
<!-- ADD GLSL SHADER CODE HERE -->
    #ifdef GL_ES
    precision mediump float;
    #endif
    
    #define PI 3.14159265359
    
    uniform vec2 uResolution;
    uniform vec2 uMouse;
    uniform float uTime;
    
    float plot(vec2 st, float pct){
      return  smoothstep( pct-0.02, pct, st.y) -
              smoothstep( pct, pct+0.02, st.y);
    }
    
    void main() {
        vec2 st = gl_FragCoord.xy/vec2(640,480);
        st -= 0.5; 
        st *= 12.0;
        float pct2 = 0.0;
        pct2 = distance(st,vec2(0.5));
    
        float y3 = sin(cos((st.y)*(0.10)))-sin(st.x+st.y*02.2);
        float y = smoothstep(1.2-(sin(((y3)))*(cos(st.y/-9.2))),0.5,st.x) - smoothstep(0.5,0.1,(st.x*0.2))+(sin(st.x-(uTime*.0412)));
        float y2 = smoothstep(04.91,02.5,st.y+st.x) - smoothstep(0.481,0.918,st.y);
        vec3 colorA = vec3(y*y2)-(y3-(0.14))*(sin(st.x-(uTime*.02412)));
        colorA = (1.0)*colorA*vec3(.020+(sin(((y3+y)))+(cos(pct2*-0.2))),0.120,(0.10+(sin(y3))));
    
        float y4 = cos(cos((st.x)*(0.13)*sin(0.23)));
        float y5 = smoothstep(0.2,0.25,0.3) - smoothstep(0.25,0.31,(st.y*0.12));
        float y6 = smoothstep(0.9+(st.x*0.012),0.1915,st.y+cos(st.y)) - smoothstep(0.641,0.8191,(st.x+st.y)*0.2);
        vec3 colorB = vec3(y4+y5)-(y3*(0.913))*(sin(st.x+(uTime*.031592)));
        colorB = (1.0)*colorB*vec3(.920,0.95030,(0.20-y6))*(sin(st.y-(uTime*.032412)));
    
        vec2 bl = step(vec2(0.5),st);
        float pct = bl.x * bl.y;
        vec3 colorMix = vec3(0.0);
        colorMix = mix(colorA*0.432, colorB+0.3892, 0.983*(sin(((y6+y2)))*(cos(pct2/-2.2))));
    
        gl_FragColor = vec4(colorMix,1.0);
    }
</script>
```

Save the file as a new _index.html_. Check to see if the shader rasters correctly.

<h3 align="center">
  <img height="50%" width="50%" src="https://github.com/user-attachments/assets/7ced5564-d09d-4e16-a7a5-c7d6577942cc"/>
</h3>

<h3 align="center">
  <img height="50%" width="50%" src="https://github.com/user-attachments/assets/6aa22574-788e-43c4-8fff-d26a3d1d4a8e"/>
</h3>


## Inscribing to the Bitcoin blockchain

We’ve tested it locally, and it runs as expected. Code is [here](https://gist.github.com/cskonopka/6f00d256ad42413ce6e3c28d8410aef0) if you are curious. It’s time to inscribe.

## Inscribing the HTML file
Go to [looksordinal](https://looksordinal.com/). It is a cost-effective site for self-custodial bulk inscriptions. The website looks like the image below.

<img height="60%" width="60%" src="https://miro.medium.com/v2/resize:fit:786/format:webp/1*gLEiaEzNXRz4a_0imbQFYg.png"/>

Add your _Ordinal address_ to the _Receiving Address_ section. Don’t forget that your Ordinal address is different than your BTC recipient address.

![1_c5bwlsi6n0Pz912brWPGGA copy](https://miro.medium.com/v2/resize:fit:786/format:webp/1*FfQR-ZWPv9X8WK8ULjMulw.png)

Choose the file you would like to inscribe. Here, it’s _index.html_.

![1_c5bwlsi6n0Pz912brWPGGA copy](https://miro.medium.com/v2/resize:fit:828/format:webp/1*0Eg3VhdVsUUPo4FD4-NV3g.png)

Select the _freerate_. I’d suggest _Mid_ because if you choose _Min_, you risk waiting a long time for the inscription to complete. Don’t forget to tip your dev!

![1_c5bwlsi6n0Pz912brWPGGA copy](https://miro.medium.com/v2/resize:fit:786/format:webp/1*PrZAhiOAoThTGevLkH1kPg.png)

Click _Estimate Fees_ to see the cost of the inscription. Then the press the _inscribe_ button.

![1_c5bwlsi6n0Pz912brWPGGA copy](https://miro.medium.com/v2/resize:fit:786/format:webp/1*V0HFcKhZbPuYiPgV2XckNg.png)

The page will transition to the payment process. Scan the QR code with your preferred Bitcoin app and send the payment to the address provided.

![1_c5bwlsi6n0Pz912brWPGGA copy](https://miro.medium.com/v2/resize:fit:786/format:webp/1*088ZxCOGHyV_1zWvuaTrmQ.png)

Once the payment is received, the inscription process begins. Click the transaction link.

![1_c5bwlsi6n0Pz912brWPGGA copy](https://miro.medium.com/v2/resize:fit:786/format:webp/1*CdJzyJaNmLAGjjVoNKor0Q.png)

Track the progress of your inscription by using [mempool.space](https://mempool.space/).

![1_c5bwlsi6n0Pz912brWPGGA copy](https://miro.medium.com/v2/resize:fit:786/format:webp/1*P_Sa3nR0pu83TvjPHPj3dg.png)

<h3 align="center">
  <img height="50%" width="50%" src="https://github.com/user-attachments/assets/46100658-8278-482d-ad15-f9864e435178"/>
</h3>

When it’s finished inscribing, check it out on Ordinals.

## Final thoughts
This is the first time a WebGL compatible HTML5 webpage has been inscribed to the Bitcoin blockchain. It is a massive moment for decentralized graphics and pushes the perception of how a blockchain can be used. It’s your turn, change the world.

# Glossary

Here is primer if you are unfamiliar with concepts mentioned above.

_Bitcoin Ordinals_: The new Ordinals protocol allows people who operate Bitcoin nodes to inscribe each sat with data, creating something called an Ordinal. That data inscribed on Bitcoin can include smart contracts, which in turn enables NFTs. In rough terms, Ordinals are NFTs you can mint directly onto the Bitcoin blockchain.

_WebGL_: WebGL is a JavaScript API for rendering interactive 2D and 3D graphics within any compatible web browser without the use of plug-ins. WebGL is fully integrated with other web standards, allowing GPU-accelerated usage of physics and image processing and effects as part of the web page canvas.

_GLSL Shaders_: Shaders use GLSL (OpenGL Shading Language), a special OpenGL Shading Language with syntax similar to C. GLSL is executed directly by the graphics pipeline. There are several kinds of shaders, but two are commonly used to create graphics on the web: Vertex Shaders and Fragment (Pixel) Shaders. Applications using OpenGL include computer games, virtual reality, augmented reality, 3D animation, CAD and other visual simulations.

_OpenGL_: OpenGL (Open Graphics Library) is a cross-language, multi-platform application programming interface (API) for rendering 2D and 3D vector graphics. The API is typically used to interact with a graphics processing unit (GPU), to achieve hardware-accelerated rendering.

# References
- [Ordinals protocol](https://github.com/casey/ord/blob/master/bip.mediawiki)
- [Bitcoin NFTs? Ordinals Inscriptions Explained (Finding, Buying, & More)](https://nftnow.com/guides/bitcoin-nfts-ordinals-inscriptions-explained-finding-buying-more/)
- [What are Bitcoin Ordinals?](https://www.bitstamp.net/learn/blockchain/what-are-bitcoin-ordinals/)
- [GLSL Shaders](https://developer.mozilla.org/en-US/docs/Games/Techniques/3D_on_the_web/GLSL_Shaders)
- [OpenGL](https://en.wikipedia.org/wiki/OpenGL)
- [What is WebGL?](https://www.youtube.com/watch?v=f-9LEoYYvE4)
- [What is a fragment shader?](https://thebookofshaders.com/01/)
- [Xverse wallet](https://www.xverse.app/)
- [What Are The Types Of Bitcoin Public Keys?](https://thebitcoinmanual.com/articles/types-btc-public-keys/)
