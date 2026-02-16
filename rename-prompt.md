You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about.html",
    "context": {
      "title": "FERRON STEELS | ABOUT US",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "careers.html",
    "context": {
      "title": "",
      "first_heading": "CAREERS"
    }
  },
  {
    "path": "contactus.html",
    "context": {
      "title": "FERRON STEELS | CONTACT US",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/65831fd6f1f49993e1646660d8747450.css",
    "context": {
      "path": "css/65831fd6f1f49993e1646660d8747450.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/c280e70a6f4e43fa117c8e590b4022bc.css",
    "context": {
      "path": "css/c280e70a6f4e43fa117c8e590b4022bc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "gallery.html",
    "context": {
      "title": "FERRON STEELS | GALLERY",
      "first_heading": "GALLERY"
    }
  },
  {
    "path": "imgs/0795bc0c907a1c97bc5c706d76ab7097.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/1573a9a3c4c97d68071f467835d1ff24.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/1c5e7e796a8669961286a8e0819015c2.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/1f4bfd7077f4099e595117b0ba2de2ed.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/29fa2f1c7ea5e75d32a21ac6b752c6ee.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/312f62d03737afb3ae87618616cae4ec.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/4165557566a574aada88581aa4dd44b5.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/44e18a84c7c3741eecb229080af597d8.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/4b60e5abc4551e1fc1143c7700200746.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/68b6569bbfdebb341aca2e8daaf95cad.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6bf250e6215d060cbc368e54abf2a302.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6d5ed30e2c9546e2f8934d6293d16022.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6f35675ab4f12ff30f045dcc6d94e893.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/725b445dcaf461b294b337b2064bd70e.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/731645aa9ec9051c290244ba93700f27.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/7fa740273e8860b094534e653fa2aa24.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/821b01381c80d6e91053e26d0c4dcbcf.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/900c635bc6f6bc20576aab025c2dbc11.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/92108b5f4f93b0eadfc8f8254da2efba.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/959f8de188d95720c25dc39f1ada7107.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/960deedec8c16ee3affaf7112145b2c6.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/96ba794363147cbe431407e8b7d3e8eb.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/988e4a08a8edab27cc38f0dcad52d6b2.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/9f2d6e8fdcdb83536c4cae75cefae96e.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/ce34fb23f2d610235addbd7568a08373.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/d0aee3c907a79ebf344acf8b5e51b505.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/ed6c72cea307feb3a76bf62a52168b90.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/f1e64f2c55eb1d0fcb3f7c1858d93ab1.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/f84f178fd88138cbc44e4cc18369b1f4.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/fac3a9285694a45e1cb08c1c64c6b43b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/fae041b9b247e2235e381e364d3a2fa7.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "FERRON STEELS | Manufacturers of Ferron TMT Rebars",
      "first_heading": "FERRON STEELS"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "products.html",
    "context": {
      "title": "FERRON STEELS | PRODUCTS | FE-500 TMT, RE-BARS & BILLETS",
      "first_heading": "PRODUCTS"
    }
  },
  {
    "path": "quality.html",
    "context": {
      "title": "FERRON STEELS | QUALITY",
      "first_heading": "QUALITY"
    }
  },
  {
    "path": "why-us.html",
    "context": {
      "title": "FERRON STEELS | WHY US",
      "first_heading": "WHY US"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.