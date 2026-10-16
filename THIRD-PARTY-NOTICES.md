# Componenti e dati di terze parti

Questo documento identifica i componenti NuGet, le librerie JavaScript, le icone, i caratteri tipografici e i dati incorporati distribuiti con BlackHole Workspaces.
I collegamenti indicano i progetti ufficiali, i pacchetti usati e le relative licenze; restano validi i testi completi
forniti dai rispettivi autori. Va aggiornato quando cambiano le versioni dei pacchetti o le fonti dei dati.

## Componenti NuGet

### MailKit 4.18.1 e MimeKit 4.18.1

- Uso: invio SMTP delle email (recupero della password, inviti, messaggio di prova).
- Progetto: [MimeKit e MailKit](https://mimekit.net/).
- Pacchetti: [MailKit 4.18.1](https://www.nuget.org/packages/MailKit/4.18.1) e [MimeKit 4.18.1](https://www.nuget.org/packages/MimeKit/4.18.1).
- Licenza dichiarata dai pacchetti: [MIT](https://licenses.nuget.org/MIT).

### BouncyCastle.Cryptography 2.7.0

- Uso: dipendenza crittografica di MailKit e MimeKit.
- Progetto: [Bouncy Castle C#](https://www.bouncycastle.org/download/bouncy-castle-c/).
- Pacchetto: [BouncyCastle.Cryptography 2.7.0](https://www.nuget.org/packages/BouncyCastle.Cryptography/2.7.0).
- Licenza dichiarata dal pacchetto: [MIT](https://licenses.nuget.org/MIT).

### Microsoft.Data.Sqlite 10.0.13

- Uso: accesso al database SQLite.
- Progetto: [Entity Framework Core](https://github.com/dotnet/efcore).
- Pacchetti: [Microsoft.Data.Sqlite 10.0.13](https://www.nuget.org/packages/Microsoft.Data.Sqlite/10.0.13) e Microsoft.Data.Sqlite.Core 10.0.13.
- Licenza dichiarata dai pacchetti: [MIT](https://licenses.nuget.org/MIT).

### SQLitePCLRaw 2.1.13 e SQLite

- Uso: libreria nativa di SQLite (`e_sqlite3`) e relativo collegamento con .NET.
- Progetto: [SQLitePCL.raw](https://github.com/ericsink/SQLitePCL.raw) e [SQLite](https://www.sqlite.org/).
- Pacchetti: SQLitePCLRaw.bundle_e_sqlite3, SQLitePCLRaw.core, SQLitePCLRaw.lib.e_sqlite3 e SQLitePCLRaw.provider.e_sqlite3, versione 2.1.13.
- Licenza dichiarata dai pacchetti: [Apache-2.0](https://licenses.nuget.org/Apache-2.0). SQLite è di [pubblico dominio](https://www.sqlite.org/copyright.html).

### Microsoft.Extensions.Hosting.WindowsServices 10.0.0 e System.ServiceProcess.ServiceController 10.0.0

- Uso: esecuzione come servizio di Windows.
- Progetto: [Microsoft .NET Runtime](https://github.com/dotnet/runtime).
- Pacchetti: [Microsoft.Extensions.Hosting.WindowsServices 10.0.0](https://www.nuget.org/packages/Microsoft.Extensions.Hosting.WindowsServices/10.0.0) e [System.ServiceProcess.ServiceController 10.0.0](https://www.nuget.org/packages/System.ServiceProcess.ServiceController/10.0.0).
- Licenza dichiarata dai pacchetti: [MIT](https://licenses.nuget.org/MIT).

### TesseractOCR 5.5.2, Tesseract 5.5 e Leptonica 1.85.0

- Uso: riconoscimento del testo (OCR) dei PDF scansionati e delle immagini, PDF ricercabili.
- Progetto: [TesseractOCR](https://github.com/Sicos1977/TesseractOCR), © Charles Weld e Kees van Spelde, collegamento per
  .NET di [Tesseract](https://github.com/tesseract-ocr/tesseract), © Google e i contributori di Tesseract, che usa
  [Leptonica](http://www.leptonica.org/), © Dan S. Bloomberg.
- Pacchetto: [TesseractOCR 5.5.2](https://www.nuget.org/packages/TesseractOCR/5.5.2), con le librerie native per Windows
  x64 `x64\tesseract55.dll` e `x64\leptonica-1.85.0.dll` (compilate con Visual Studio 2022: servono le librerie di
  Microsoft Visual C++ 2015-2022 x64, presenti in Windows o installate con il loro pacchetto ufficiale).
- Licenza: [Apache-2.0](https://licenses.nuget.org/Apache-2.0) per TesseractOCR e Tesseract;
  [licenza di Leptonica](http://www.leptonica.org/about-the-license.html) (di tipo BSD a 2 clausole).

### Docnet.Core 2.6.0 e PDFium

- Uso: lettura del testo delle pagine dei PDF e disegno delle pagine scansionate da riconoscere; unione delle pagine
  nel PDF ricercabile.
- Progetto: [Docnet](https://github.com/GowenGit/docnet), © Modestas Petravicius, che usa
  [PDFium](https://pdfium.googlesource.com/pdfium/), © The PDFium Authors.
- Pacchetto: [Docnet.Core 2.6.0](https://www.nuget.org/packages/Docnet.Core/2.6.0), con la libreria nativa `pdfium.dll`.
- Licenza: [MIT](https://licenses.nuget.org/MIT) per Docnet; PDFium con licenza BSD a 3 clausole e, per alcune parti,
  Apache-2.0 e le altre licenze riportate nel file `LICENSE` distribuito con la libreria.

### .NET 10 e ASP.NET Core

- Uso: il pacchetto pubblicato (`Scripts\Publish.ps1`) è autonomo e contiene il runtime di .NET e ASP.NET Core.
- Progetto: [.NET](https://dotnet.microsoft.com/).
- Licenza: [MIT](https://github.com/dotnet/runtime/blob/main/LICENSE.TXT); i componenti di terze parti del runtime sono elencati nel suo file `THIRD-PARTY-NOTICES.TXT`.

## Librerie JavaScript dei documenti

Il visualizzatore e l'editor dei documenti (`wwwroot/assets/js/core/viewer.js`, `editor.js`, `docx-io.js`) usano le
librerie seguenti, distribuite in `wwwroot/assets/vendor` e caricate dal browser solo quando servono. Sono prese dai
pacchetti npm indicati tramite `https://cdn.jsdelivr.net/npm/` (SheetJS dal suo sito), senza modifiche salvo dove
indicato. Accanto a ogni libreria c'è il testo completo della sua licenza (`LICENSE…`).

| Libreria | Versione | Uso | Licenza | File |
|---|---|---|---|---|
| [PDF.js](https://mozilla.github.io/pdf.js/) (`pdfjs-dist`), © Mozilla Foundation | 6.3.289 | PDF | [Apache-2.0](https://github.com/mozilla/pdf.js/blob/master/LICENSE) | `pdfjs/` |
| [docx-preview](https://github.com/VolodymyrBaydalka/docxjs), © Volodymyr Baydalka | 0.4.1 | Word .docx nel visualizzatore | Apache-2.0 | `docx/docx-preview.min.js` |
| [JSZip](https://stuk.github.io/jszip/), © Stuart Knightley e altri | 3.10.2 | archivi dei file Office (per docx-preview) | MIT (scelta tra MIT e GPLv3) | `docx/jszip.min.js` |
| [SheetJS Community Edition](https://sheetjs.com/) (`xlsx`), © SheetJS LLC | 0.20.3 | Excel, ODS, CSV | Apache-2.0 | `sheetjs/xlsx.full.min.js` |
| [UTIF.js](https://github.com/photopea/UTIF.js), © Photopea | 3.1.0 | immagini TIFF | MIT | `utif/UTIF.js` |
| [three.js](https://threejs.org/), © three.js authors | 0.186.1 | modelli 3D e base del visualizzatore DXF | MIT | `three/` |
| [fflate](https://github.com/101arrowz/fflate), © Arjun Barrett (incluso in three.js) | 0.8.2 | modelli 3MF compressi | MIT | `three/addons/libs/fflate.module.js` |
| [dxf-viewer](https://github.com/vagran/dxf-viewer), © SIA SPH Engineering | 1.0.49 | disegni DXF | [MPL-2.0](https://www.mozilla.org/MPL/2.0/) | `dxf/dxf-viewer.mjs` |
| [earcut](https://github.com/mapbox/earcut), © Mapbox | 3.2.3 | riempimenti dei DXF (per dxf-viewer) | ISC | `dxf/earcut.mjs` |
| [loglevel](https://github.com/pimterry/loglevel), © Tim Perry | 1.9.2 | messaggi di dxf-viewer | MIT | `dxf/loglevel.mjs` |
| [opentype.js](https://opentype.js.org/), © Frederik De Bleser | 1.3.4 | testi dei DXF (per dxf-viewer) | MIT | `dxf/opentype.mjs` |
| [Quill](https://quilljs.com/), © Slab, Jason Chen, salesforce.com | 2.0.3 | editor di testo formattato (documenti Word e appunti) | BSD-3-Clause | `editor/quill.js`, `editor/quill.snow.css` |
| [docx](https://docx.js.org/), © Dolan Miu | 9.8.1 | scrittura dei file Word .docx | MIT | `editor/docx.iife.js` |
| [mammoth.js](https://github.com/mwilliamson/mammoth.js), © Michael Williamson | 1.13.0 | apertura dei file Word .docx nell'editor | BSD-2-Clause | `editor/mammoth.browser.min.js` |

Origine dei file (`J` = `https://cdn.jsdelivr.net/npm`):

- PDF.js: `J/pdfjs-dist@6.3.289/build/pdf.min.mjs`, `build/pdf.worker.min.mjs`, `wasm/jbig2.wasm`, `wasm/openjpeg.wasm`, `LICENSE`.
- docx-preview: `J/docx-preview@0.4.1/dist/docx-preview.min.js`; JSZip: `J/jszip@3.10.2/dist/jszip.min.js`.
- SheetJS: `https://cdn.sheetjs.com/xlsx-0.20.3/package/dist/xlsx.full.min.js` e `…/package/LICENSE`.
- UTIF.js: `J/utif@3.1.0/UTIF.js`.
- three.js: `J/three@0.186.1/build/three.module.min.js` e `three.core.min.js`, più `examples/jsm/controls/OrbitControls.js`,
  `loaders/STLLoader.js`, `OBJLoader.js`, `3MFLoader.js`, `GLTFLoader.js`, `libs/fflate.module.js`,
  `utils/BufferGeometryUtils.js`, `utils/SkeletonUtils.js`. **Modifica**: nei componenti aggiuntivi l'importazione
  `'three'` è stata sostituita dal percorso relativo di `three.module.min.js`, perché funzionino senza import map.
- dxf-viewer: `J/dxf-viewer@1.0.49/+esm` (modulo preparato da jsDelivr), con earcut, loglevel e opentype.js presi allo
  stesso modo (`J/earcut@3.2.3/+esm`, `J/loglevel@1.9.2/+esm`, `J/opentype.js@1.3.4/+esm`). **Modifica**: le
  importazioni tra questi moduli e verso three.js puntano ai file locali.
- Quill: `J/quill@2.0.3/dist/quill.js` e `dist/quill.snow.css`; docx: `J/docx@9.8.1/dist/index.iife.js` (salvato come
  `docx.iife.js`); mammoth.js: `J/mammoth@1.13.0/mammoth.browser.min.js`.

SHA-256 dei file:

```
F80490490320511E5DF18C580B9EDD6B5DB8058DCEEBAF6F161992E0A964B9E2  pdfjs/pdf.min.mjs
8AB0E5E30031B4A06ECFDDD5AE9562F0227F830EE7EC9ED1A968B134243D2386  pdfjs/pdf.worker.min.mjs
E6BEE67724A7B5436FE8162638E3708CFC8D52B6342DB69A49715E30FF27CFDC  pdfjs/wasm/jbig2.wasm
004A0E62DB930BA9FF2A22212F4554D0BB57A0635A8287CAF70F98117CEE14BA  pdfjs/wasm/openjpeg.wasm
C4A133C65A112799E35B143C572DFFF9E923A3BF39B5FD3B07A06AA0F8F530C2  docx/docx-preview.min.js
7F839B2D4688B845C105EBF5D2F9803075F91EA0FE72BDAAC176C3A04DD3D2C1  docx/jszip.min.js
CC015130AA8521E7F088F88898EBA949CCDCBFB38DF0BD129B44B7273C3A6F41  sheetjs/xlsx.full.min.js
E3E76115F49571E39624C3316A76B3C4C5B2C5CA518DFEC4B66A9F7AF8C6D059  utif/UTIF.js
B2447F4F2D97D635F791E929E3F77C6A6AF8A798D1561A04340A9348BC217A07  three/three.module.min.js
3B346151F65FFDFCA3E4C002BD58966B78C423087FB48A873F83200DE1BFFC48  three/three.core.min.js
52D1E03BA0BDC9FF258403A757EB3D3EBA3EBBB9C585E4A8BC2FABCEBC182F5A  three/addons/controls/OrbitControls.js
209A4412EB48CE609EDB4391992A792FFCC3983D30EE7E2B0B89A8C470F3CD8A  three/addons/libs/fflate.module.js
A7A14B9458100B4B0A85DC75AA5CA60D30D4D61E5B5D33CA17460C0AAEFF2BC5  three/addons/loaders/3MFLoader.js
C1ED6222A6C85424EF408CD48BC5A897C363CBFD74680A44D87B80047CD651F5  three/addons/loaders/GLTFLoader.js
FC74467DEC4F5D00582836C7EB564DA7D8B82AD8D8C2949EB0A62DD113796865  three/addons/loaders/OBJLoader.js
31FED8A78843A8F4A58F4FF4B816827232C7E7A0C6226C79BDBF2E792DA41522  three/addons/loaders/STLLoader.js
79296B36B2719BCC3129784E048495A6037768A96894E56AA926736A20F02589  three/addons/utils/BufferGeometryUtils.js
B9CE558A98772A46DC67816D27E629A9810E41D1FD968EB96BDBFC8DBFB959F2  three/addons/utils/SkeletonUtils.js
27D8EC943BD40524B74BADB9BF3F9C630A90D3606466229492A02E554A45EE51  dxf/dxf-viewer.mjs
7AD4FA63F29DBA2190749F32FFF6520596371FC362BC4F97937510526E5953AB  dxf/earcut.mjs
7EBA036A5A3D824093630C259E3632ADA21211CD787332BAE33E6E5BAC1634CE  dxf/loglevel.mjs
7B445C538047FB713A8EC0D2D558C79A31ADE5EFB10C71674BA3EB4C0F5C60D9  dxf/opentype.mjs
22AFDDE505C286165D1D4D4F9F02B505773458D0F770E9E24EE1897184C11C9E  editor/quill.js
1C7948CD13AA92FAC6390319BC1E5E461823DA171519D3A768DB56164F871636  editor/quill.snow.css
1A1C55AF6242BC9BC1D89CBA76F656E79E9B4B3C43228E17BEE8CDA0B9DFFAD1  editor/docx.iife.js
92914A3708CFDF1E62CB553D1856A7FEDAB21DA83D8EE82845DE2F897B368CAB  editor/mammoth.browser.min.js
```

LibreOffice non è incluso: se l'amministratore lo installa dalla piattaforma, il setup ufficiale viene scaricato da
`download.documentfoundation.org` (o caricato dall'amministratore) ed è distribuito da The Document Foundation con la
propria licenza ([MPL-2.0](https://www.libreoffice.org/about-us/licenses/)).

Neppure i convertitori dei disegni DWG sono inclusi; la piattaforma li esegue come programmi separati, senza collegarli
al proprio codice:

- [GNU LibreDWG](https://www.gnu.org/software/libredwg/), © Free Software Foundation, licenza
  [GPL-3.0-or-later](https://www.gnu.org/licenses/gpl-3.0.html). Se l'amministratore lo installa dalla piattaforma, viene
  scaricato il pacchetto ufficiale per Windows della versione 0.14 dalle release del progetto indicate da gnu.org
  (`https://github.com/LibreDWG/libredwg/releases/download/0.14/libredwg-0.14-win64.zip`), oppure lo carica
  l'amministratore; in entrambi i casi si accetta solo il file con SHA-256
  `1AD7E15344D20B3426C3435B078D82FB84B35062815946B2CCA9C5FC9810FEA8`, verificato con la firma GPG del manutentore
  (chiave `38A4 167B 0DB6 9E49 C5F7 216C B8C2 8866 AB27 A7A2`). Il pacchetto contiene la licenza e il codice sorgente si
  trova sugli stessi siti.
- [ODA File Converter](https://www.opendesign.com/guestfiles/oda_file_converter), programma gratuito della Open Design
  Alliance, con le condizioni dell'[ODA Community User Agreement](https://www.opendesign.com/agreements/2025/en/ODA%20Community%20User%20Agreement%2009-2025.pdf)
  (uso per le funzioni del programma, come la conversione dei file; niente rivendita né distribuzione). Non è
  distribuito con BlackHole Workspaces: se l'amministratore lo installa dalla piattaforma, il setup ufficiale per Windows
  viene scaricato dal sito della Open Design Alliance
  (`https://www.opendesign.com/guestfiles/get?filename=ODAFileConverter_QT6_vc16_amd64dll.msi`, che rimanda al file
  dell'ultima versione), oppure lo carica l'amministratore; in entrambi i casi si accetta solo un pacchetto *ODA File
  Converter* firmato dalla Open Design Alliance (Authenticode). Installato a mano, viene solo cercato nella cartella dei
  programmi.

## Assistente AI

Né il motore né i modelli dell'assistente AI sono inclusi nel programma: li installa e li scarica un amministratore da
*Impostazioni → Assistente AI* e la piattaforma esegue il motore come programma separato (`llama-server.exe`, in
ascolto solo su 127.0.0.1), senza collegarlo al proprio codice.

- **Motore**: [llama.cpp](https://github.com/ggml-org/llama.cpp), © The ggml authors, licenza
  [MIT](https://github.com/ggml-org/llama.cpp/blob/master/LICENSE). La piattaforma scarica dalle release del progetto su
  GitHub il pacchetto ufficiale per Windows (solo processore, x64) della versione stabile più recente: la versione
  stabile indica nel file `nightly-tag.txt` la build di cui usare i pacchetti (`llama-<build>-bin-win-cpu-x64.zip`) e si
  accetta solo il file con l'impronta SHA-256 che GitHub pubblica per quel pacchetto. In alternativa l'amministratore lo
  carica: se il nome indica la build e GitHub è raggiungibile, l'impronta deve essere quella pubblicata. Il pacchetto,
  che contiene la licenza, viene estratto in `tools\llamacpp`.
- **Modelli consigliati**: file GGUF di [Qwen3](https://huggingface.co/Qwen), © Alibaba Cloud (Qwen Team), licenza
  [Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0), che ne permette anche l'uso commerciale. Si scaricano da
  Hugging Face nella versione fissata del repository e si accettano solo con questa impronta SHA-256; vanno in `models\`:
  - [Qwen3 4B](https://huggingface.co/Qwen/Qwen3-4B-GGUF), `Qwen3-4B-Q4_K_M.gguf` (2.497.280.256 byte), commit
    `bc640142c66e1fdd12af0bd68f40445458f3869b`, SHA-256
    `7485FE6F11AF29433BC51CAB58009521F205840F5B4AE3A32FA7F92E8534FDF5`;
  - [Qwen3 8B](https://huggingface.co/Qwen/Qwen3-8B-GGUF), `Qwen3-8B-Q4_K_M.gguf` (5.027.783.488 byte), commit
    `7c41481f57cb95916b40956ab2f0b139b296d974`, SHA-256
    `D98CDCBD03E17CE47681435B5150E34C1417F50B5C0019DD560E4882C5745785`;
  - [Qwen3 1.7B](https://huggingface.co/Qwen/Qwen3-1.7B-GGUF), `Qwen3-1.7B-Q8_0.gguf` (1.834.426.016 byte), commit
    `90862c4b9d2787eaed51d12237eafdfe7c5f6077`, SHA-256
    `061B54DAADE076B5D3362DAC252678D17DA8C68F07560BE70818CACE6590CB1A`.

  Gli altri modelli GGUF che l'amministratore carica a mano hanno la propria licenza, da controllare prima dell'uso in
  azienda (alcuni, come Qwen2.5 3B, sono riservati alla ricerca e all'uso non commerciale).

## Riconoscimento del testo

I dati delle lingue non sono inclusi nel programma: li scarica un amministratore da *Impostazioni → Sistema* nella
cartella `tools\tessdata`, da GitHub, sempre negli stessi file fissati, che si accettano solo con questa dimensione e
questa impronta SHA-256:

- **Lingue e orientamento**: modelli «best» di [tessdata_best](https://github.com/tesseract-ocr/tessdata_best),
  © Google e i contributori di Tesseract, licenza [Apache-2.0](https://github.com/tesseract-ocr/tessdata_best/blob/main/LICENSE),
  commit `e12c65a915945e4c28e237a9b52bc4a8f39a0cec`:
  - `ita.traineddata` (8.863.635 byte), SHA-256 `8DF9C89176FB93F56BF4B2D4EDE04C01C1F31D4B7697FBD76CC336DF700F3F38`;
  - `eng.traineddata` (15.400.601 byte), SHA-256 `8280AED0782FE27257A68EA10FE7EF324CA0F8D85BD2FD145D1C2B560BCB66BA`;
  - `osd.traineddata` (10.562.727 byte), SHA-256 `9CF5D576FCC47564F11265841E5CA839001E7E6F38FF7F7AACF46D15A96B00FF`.
- **Font del testo invisibile nei PDF ricercabili**: `pdf.ttf` (572 byte) della versione 5.5.2 di
  [Tesseract](https://github.com/tesseract-ocr/tesseract/tree/5.5.2/tessdata), licenza Apache-2.0, SHA-256
  `C7845420925A23D88ED830A63957B8AF85A66A8DAF8D9FC90E843673B2EF1A59`.

## Libreria della radio

- Uso: suona nel mini player (`wwwroot/assets/js/core/radio.js`) le radio in formato HLS quando il browser non lo sa
  fare da solo; viene caricata solo in quel caso.
- Opera: [hls.js](https://github.com/video-dev/hls.js), versione 1.7.3, build «light» (`dist/hls.light.min.js`),
  © 2017 Dailymotion.
- Licenza: [Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0); il testo del pacchetto è
  `wwwroot/assets/vendor/hls/LICENSE`.
- Origine: il pacchetto npm `https://registry.npmjs.org/hls.js/-/hls.js-1.7.3.tgz` (integrità
  `sha512-MsPlx6yVW4Qv4C7mEVou4/gk/5cN2dVxOTnrNjPSmyH2f0Ln+/UkG10Ax1PE6OvrmTVPKgQYozTtBaPOuCzq7A==`), senza modifiche.
- File: `wwwroot/assets/vendor/hls/hls.light.min.js`, SHA-256
  `0251332C00A216A35D7D6919044D60DA82B78BEB3BD50AC6C662AE74A2F5474B`.

## Libreria delle mappe

- Uso: la mappa degli indirizzi nella scheda dei clienti e dei fornitori (`wwwroot/assets/js/core/map.js`), caricata solo
  quando serve.
- Opera: [Leaflet](https://leafletjs.com/), versione 1.9.4, © 2010-2023 Volodymyr Agafonkin, © 2010-2011 CloudMade.
- Licenza: [BSD-2-Clause](https://github.com/Leaflet/Leaflet/blob/main/LICENSE); il testo del pacchetto è
  `wwwroot/assets/vendor/leaflet/LICENSE`. Il collegamento a Leaflet resta nella riga dei riconoscimenti della mappa.
- Origine: il pacchetto npm `https://registry.npmjs.org/leaflet/-/leaflet-1.9.4.tgz` (integrità
  `sha512-nxS1ynzJOmOlHp+iL3FyWqK89GtNL8U8rvlMOsQdTTssxZwCXh8N2NB3GDQOL+YR3XnWyZAxwQixURb+FA74PA==`, verificata),
  scaricato il 5 ottobre 2026, senza modifiche.
- File in `wwwroot/assets/vendor/leaflet/` (dalla cartella `dist` del pacchetto), SHA-256:
  - `leaflet.js` `DB49D009C841F5CA34A888C96511AE936FD9F5533E90D8B2C4D57596F4E5641A`
  - `leaflet.css` `A7837102824184820DFA198D1EBCD109FF6D0FF9A2672A074B9A1B4D147D04C6`
  - `images/layers.png` `1DBBE9D028E292F36FCBA8F8B3A28D5E8932754FC2215B9AC69E4CDECF5107C6`
  - `images/layers-2x.png` `066DACA850D8FFBEF007AF00B06EAC0015728DEE279C51F3CB6C716DF7C42EDF`
  - `images/marker-icon.png` `574C3A5CCA85F4114085B6841596D62F00D7C892C7B03F28CBFA301DEB1DC437`
  - `images/marker-icon-2x.png` `00179C4C1EE830D3A108412AE0D294F55776CFEB085C60129A39AA6FC4AE2528`
  - `images/marker-shadow.png` `264F5C640339F042DD729062CFC04C17F8EA0F29882B538E3848ED8F10EDB4DA`

## Icone

Le icone a tratto dell'interfaccia (`wwwroot/assets/js/core/icons.js`) usano i tracciati di [Lucide](https://lucide.dev/),
distribuiti con [licenza ISC](https://github.com/lucide-icons/lucide/blob/main/LICENSE) (© Lucide Contributors; le icone
derivate da Feather sono © Cole Bemis, licenza MIT). Il logo del buco nero e le immagini della cartella `Assets` sono del
progetto.

### Material Design Icons

- Uso: «Icona e colore» delle schede (clienti, impianti e tipi, modelli delle schede tecniche, monitoraggio, mezzi e
  attrezzature, tipi delle password): catalogo e ricerca in `Services/IconCatalog.vb`, disegno in
  `wwwroot/assets/js/core/badge.js`.
- Opera: [Material Design Icons](https://pictogrammers.com/library/mdi/) 7.4.47, © Pictogrammers (pacchetto
  `@mdi/svg`); le icone dei marchi e quelle deprecate non sono incluse.
- Licenza: [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) per le icone (Pictogrammers Free License); il
  testo è `Assets/Icons/LICENSE-mdi.txt`.
- File: `Assets/Icons/mdi-v7.4.47.mui.gz` (863.689 byte, SHA-256
  `4cdf94eb19fffbe40e76f68ed33f4b1102ac11fd17aea316e5729f4a47d5cbc6`), incorporato nel programma: 7.188 icone con
  tracciati, categorie e alias, preparate dal progetto ModernFrameworkUI dello stesso autore di BlackHole Workspaces.
  Le traduzioni italiane per la ricerca e le raccolte sono del progetto.

### Icone del meteo

- Uso: icone animate (e ferme, per chi chiede di ridurre le animazioni) del meteo nell'area informativa della barra
  superiore (`wwwroot/assets/js/core/dayinfo.js`).
- Opera: [Free Animated SVG Weather Icons](https://www.amcharts.com/free-animated-svg-weather-icons/), versione 1.0.0,
  © amCharts.
- Licenza: [Creative Commons Attribuzione 4.0 Internazionale](https://creativecommons.org/licenses/by/4.0/) (uso
  commerciale consentito citando amCharts); il testo del pacchetto è `wwwroot/assets/vendor/weather/LICENSE.txt`. Il
  riconoscimento è anche nella guida utente, capitolo *Fonti e riconoscimenti*.
- Origine: `https://www.amcharts.com/dl/svg-weather-icons/`, che rimanda a
  `https://download.amcharts.com/1.0/amcharts_weather_icons_1.0.0.zip` (SHA-256
  `20B84CABD8402B2E418383B90A9A1382FC890DB5C90849A9141A2B63DA78E35E`), scaricato il 3 ottobre 2026.
- File: dalle cartelle `animated/` e `static/` del pacchetto, senza modifiche, `day`, `night`, `cloudy`,
  `cloudy-day-1…3`, `cloudy-night-1…3`, `rainy-1…7`, `snowy-1…6` e `thunder` (`.svg`), in `wwwroot/assets/vendor/weather/`.

## Fattura elettronica

- Schema XML della fattura elettronica, versione 1.2.2 (`Assets/FatturaPA/Schema_del_file_xml_FatturaPA_v1.2.2.xsd`),
  pubblicato da Agenzia delle Entrate / SOGEI su [www.fatturapa.gov.it](https://www.fatturapa.gov.it): specifica
  pubblica, inclusa senza modifiche per controllare le fatture prodotte.
- Schema della firma XML (`Assets/FatturaPA/xmldsig-core-schema.xsd`), W3C Recommendation «XML-Signature Syntax and
  Processing» del 12/02/2002, © W3C (W3C Software and Document License), richiamato dallo schema della fattura.

## Servizi esterni

Dati che la piattaforma chiede a servizi di terzi mentre funziona (non sono inclusi nel programma):

- **Previsioni del tempo** (area informativa, se è indicata una località con le coordinate):
  [MET Norway](https://www.met.no/en/free-meteorological-data), servizio Locationforecast 2.0
  (`api.met.no`), dati con licenza [Creative Commons Attribuzione 4.0](https://creativecommons.org/licenses/by/4.0/),
  gratuiti anche per uso commerciale secondo le [condizioni d'uso](https://api.met.no/doc/TermsOfService) del servizio
  (identificazione nello User-Agent, cache fino alla scadenza indicata). Il riconoscimento è nella guida utente, capitolo
  *Fonti e riconoscimenti*.
- **Nuove versioni**: le release della repo pubblica del programma su GitHub (`api.github.com`).
- **Ricerca degli indirizzi** (se un amministratore la attiva con la sua chiave): [Geoapify](https://www.geoapify.com/),
  Geocoding API (`api.geoapify.com/v1/geocode/search` e `/reverse`), piano gratuito: 3000 crediti al giorno, uso
  commerciale consentito secondo le [condizioni](https://www.geoapify.com/terms-and-conditions/), che chiedono la dicitura
  «Powered by Geoapify» e il riconoscimento di OpenStreetMap (entrambi nel riquadro dei risultati) e vietano di
  distribuire le richieste su più account per restare in un piano più basso: la piattaforma usa una sola chiave, conta
  le richieste del giorno e si ferma al tetto scelto. I dati degli indirizzi sono © [OpenStreetMap](https://www.openstreetmap.org/copyright)
  e dei suoi contributori, con licenza [ODbL](https://opendatacommons.org/licenses/odbl/); i risultati restano in memoria
  sul server per una settimana e quello scelto viene salvato nella riga indirizzo. Il server invia il testo cercato o le
  coordinate, mai altri dati.
- **Mappe** (mappa degli indirizzi dei clienti): i riquadri dei server di [OpenStreetMap](https://www.openstreetmap.org/)
  (`tile.openstreetmap.org`), gestiti da volontari della OpenStreetMap Foundation. I dati delle mappe sono ©
  [OpenStreetMap](https://www.openstreetmap.org/copyright) e dei suoi contributori, con licenza
  [ODbL](https://opendatacommons.org/licenses/odbl/); il riconoscimento «© OpenStreetMap» è sempre visibile sulla mappa.
  Secondo le [regole d'uso dei riquadri](https://operations.osmfoundation.org/policies/tiles/) li chiede il browser di
  chi guarda la mappa, solo per la zona mostrata (niente scaricamenti in blocco né mappe fuori linea), con la provenienza
  ridotta all'indirizzo del server (`referrerPolicy: strict-origin-when-cross-origin`) e la cache del browser. È un uso
  leggero, adatto a un'azienda; per un uso intenso le regole chiedono un fornitore di riquadri proprio.
- **Genere dai nomi** (se un amministratore lo attiva): [genderize.io](https://genderize.io/) di Demografix ApS. Il server
  invia solo il primo nome, con il paese Italia; secondo le [condizioni](https://genderize.io/legal/terms-and-conditions)
  le risposte si possono conservare (cosa incoraggiata per non ripetere le richieste: la piattaforma le tiene in
  `cache\genderize-names.json`) e secondo l'[informativa](https://genderize.io/legal/privacy-policy) i nomi ricevuti non
  vengono conservati né registrati; i server sono negli Stati Uniti. La piattaforma propone il genere solo come
  suggerimento modificabile, mai come dato verificato.
- **Radio** (mini player): il catalogo [radio-browser.info](https://www.radio-browser.info/), con API libera e gratuita,
  usabile anche in programmi non liberi. Il server chiede la ricerca tra le radio italiane e, a ogni ascolto,
  l'indirizzo aggiornato della stazione (`/json/url`, che conta l'ascolto come il catalogo chiede), su uno dei server
  indicati dal DNS di `all.api.radio-browser.info`, identificandosi nello User-Agent. I dati del catalogo non sono
  inclusi nel programma: l'elenco curato contiene solo gli identificativi delle stazioni e un indirizzo di riserva. Le
  trasmissioni appartengono alle emittenti e il browser le riceve direttamente da loro.
- **Assistente AI** (solo quando un amministratore installa il motore o scarica un modello): l'API delle release di
  llama.cpp su GitHub (`api.github.com/repos/ggml-org/llama.cpp`) e i suoi file, e i file dei modelli su Hugging Face
  (`huggingface.co`). Le domande all'assistente restano sul server; se l'amministratore sceglie un server compatibile
  OpenAI, domande e testi vanno a quel server.
- **Riconoscimento del testo** (solo quando un amministratore lo installa): i file dei dati delle lingue su
  `raw.githubusercontent.com` (repository `tesseract-ocr/tessdata_best` e `tesseract-ocr/tesseract`). I documenti e le
  immagini da leggere restano sul server.

## Caratteri tipografici

I caratteri che si possono scegliere al posto di quello di sistema (Profilo → Aspetto) sono distribuiti in
`wwwroot/assets/fonts`, una sottocartella per carattere. Sono i file variabili (asse del peso, stile normale, sottoinsiemi
`latin` e `latin-ext`, formato WOFF2) dei pacchetti [Fontsource](https://fontsource.org/), presi senza modifiche da
`https://cdn.jsdelivr.net/npm/`. Sono tutti concessi con la
[SIL Open Font License 1.1](https://openfontlicense.org/open-font-license-official-text/): il testo completo, con le note
di copyright, è il file `LICENSE.txt` di ogni sottocartella (il file `LICENSE` del pacchetto; per Source Sans 3 la nota
di copyright è solo nei file del carattere, come indicato sotto). Gli `@font-face` sono nel blocco «Caratteri» di
`wwwroot/assets/css/app.css`.

### Inter

- Pacchetto: [@fontsource-variable/inter 5.3.0](https://www.npmjs.com/package/@fontsource-variable/inter/v/5.3.0).
- Copyright: © 2016 The Inter Project Authors ([rsms/inter](https://github.com/rsms/inter)).
- Licenza: OFL-1.1 (`wwwroot/assets/fonts/inter/LICENSE.txt`).
- Origine: `https://cdn.jsdelivr.net/npm/@fontsource-variable/inter@5.3.0/files/`.
- File e SHA-256:
  - `inter-latin-wght-normal.woff2`: `3100E775E8616CD2611BEECFA23A4263D7037586789B43F035236A2E6FBD4C62`
  - `inter-latin-ext-wght-normal.woff2`: `34B9C504CAB7A73E37B746343A449132E56CF7B5481AF2CB81DC74DCFF25C956`

### Source Sans 3

- Pacchetto: [@fontsource-variable/source-sans-3 5.3.0](https://www.npmjs.com/package/@fontsource-variable/source-sans-3/v/5.3.0).
- Copyright: © 2023 Adobe (http://www.adobe.com/), con nome riservato «Source»
  ([adobe-fonts/source-sans](https://github.com/adobe-fonts/source-sans)). È la nota contenuta nei due file del carattere
  (versione 3.052); il file `LICENSE` del pacchetto, e quindi `LICENSE.txt`, come intestazione riporta soltanto «Google Inc.».
- Licenza: OFL-1.1 (`wwwroot/assets/fonts/source-sans-3/LICENSE.txt`).
- Origine: `https://cdn.jsdelivr.net/npm/@fontsource-variable/source-sans-3@5.3.0/files/`.
- File e SHA-256:
  - `source-sans-3-latin-wght-normal.woff2`: `7A19A7027E125257D310C6DBD78AE3A30B5EA1E3794D60B12BB28227A003BFDA`
  - `source-sans-3-latin-ext-wght-normal.woff2`: `A85A7459BDB3CDC1136751E151A506BAE653FC29ADA3CA86237477DF6F1B59E6`

### IBM Plex Sans

- Pacchetto: [@fontsource-variable/ibm-plex-sans 5.3.0](https://www.npmjs.com/package/@fontsource-variable/ibm-plex-sans/v/5.3.0).
- Copyright: © 2019 IBM Corp. ([IBM/plex](https://github.com/IBM/plex)).
- Licenza: OFL-1.1 (`wwwroot/assets/fonts/ibm-plex-sans/LICENSE.txt`).
- Origine: `https://cdn.jsdelivr.net/npm/@fontsource-variable/ibm-plex-sans@5.3.0/files/`.
- File e SHA-256:
  - `ibm-plex-sans-latin-wght-normal.woff2`: `E2291E842CF5AF167122A22881A740C7F2DDA7716F1E8CD76680264F4A859470`
  - `ibm-plex-sans-latin-ext-wght-normal.woff2`: `D160E20920AE4D6556518D352D3AF27A74E9B0DE3D8FE17B1C1044FC75AA2F81`
- Per i testi dei disegni DXF (opentype.js non legge il formato WOFF2) ci sono anche i file WOFF del peso normale, dal
  pacchetto [@fontsource/ibm-plex-sans 5.3.0](https://www.npmjs.com/package/@fontsource/ibm-plex-sans/v/5.3.0)
  (`https://cdn.jsdelivr.net/npm/@fontsource/ibm-plex-sans@5.3.0/files/`), stessa licenza:
  - `ibm-plex-sans-latin-400-normal.woff`: `828907BFD14855C880789878BD2B38FFD284A6C27C8B80F6069900F70DAE3901`
  - `ibm-plex-sans-latin-ext-400-normal.woff`: `85DB75B89E3C0BEE23EA75EDE70C73024F62516CCDB6BE55EB0C5C7A7866433A`

### Nunito Sans

- Pacchetto: [@fontsource-variable/nunito-sans 5.3.0](https://www.npmjs.com/package/@fontsource-variable/nunito-sans/v/5.3.0).
- Copyright: © 2016 The Nunito Sans Project Authors ([Fonthausen/NunitoSans](https://github.com/Fonthausen/NunitoSans)).
- Licenza: OFL-1.1 (`wwwroot/assets/fonts/nunito-sans/LICENSE.txt`).
- Origine: `https://cdn.jsdelivr.net/npm/@fontsource-variable/nunito-sans@5.3.0/files/`.
- File e SHA-256:
  - `nunito-sans-latin-wght-normal.woff2`: `29E3890496844A9EA81975C52771C587C872B4EB317026422D1995B88D21B57D`
  - `nunito-sans-latin-ext-wght-normal.woff2`: `C648EE5BFDA70D44B9FB628F4114D1CC4F984D050CBB4881052237EDE3638A2E`

### Atkinson Hyperlegible Next

- Pacchetto: [@fontsource-variable/atkinson-hyperlegible-next 5.3.0](https://www.npmjs.com/package/@fontsource-variable/atkinson-hyperlegible-next/v/5.3.0).
- Copyright: © 2020-2024 The Atkinson Hyperlegible Next Project Authors
  ([googlefonts/atkinson-hyperlegible-next](https://github.com/googlefonts/atkinson-hyperlegible-next)).
- Licenza: OFL-1.1 (`wwwroot/assets/fonts/atkinson-hyperlegible-next/LICENSE.txt`).
- Origine: `https://cdn.jsdelivr.net/npm/@fontsource-variable/atkinson-hyperlegible-next@5.3.0/files/`.
- File e SHA-256:
  - `atkinson-hyperlegible-next-latin-wght-normal.woff2`: `18B2A1A39A2FA298B0BA5390ACA68462669826C90925656F1C1F6796E0E1BBAF`
  - `atkinson-hyperlegible-next-latin-ext-wght-normal.woff2`: `7DAE0C6C66AF1AEC82E096186AEB1F0E6FA36AB8061ED65422F2B7DAF4DD93F3`

### Lora

- Pacchetto: [@fontsource-variable/lora 5.3.0](https://www.npmjs.com/package/@fontsource-variable/lora/v/5.3.0).
- Copyright: © 2011 The Lora Project Authors ([cyrealtype/Lora-Cyrillic](https://github.com/cyrealtype/Lora-Cyrillic)),
  con nome riservato «Lora».
- Licenza: OFL-1.1 (`wwwroot/assets/fonts/lora/LICENSE.txt`).
- Origine: `https://cdn.jsdelivr.net/npm/@fontsource-variable/lora@5.3.0/files/`.
- File e SHA-256:
  - `lora-latin-wght-normal.woff2`: `DDB8C66035104E233FC024669183AAD3738B6DAA16DEEE2EBB1241BD0F98ACE1`
  - `lora-latin-ext-wght-normal.woff2`: `2A2D9C22C9863086A23F5013FEDE1428585321812B25F2662542C39D02967C5E`

## Produttori dei dispositivi di rete

`Assets/Oui/ieee-oui.txt.gz` (il produttore di un dispositivo dal suo indirizzo MAC, nello scanner della rete locale)
contiene i prefissi e i nomi delle organizzazioni dei registri pubblici dell'IEEE Registration Authority: MA-L (OUI a 24
bit), MA-M (28 bit) e MA-S (36 bit), consultabili gratuitamente su https://standards.ieee.org/products-programs/regauth/.
È generato da `Scripts/Build-Oui.py` dal file «manuf» che il progetto Wireshark compila da quei registri
(https://www.wireshark.org/download/automated/data/manuf). I dati sono forniti così come sono, senza garanzie di
accuratezza o aggiornamento; l'amministratore può scaricare i registri aggiornati dall'IEEE dalla piattaforma.

## Dati geografici

`wwwroot/assets/data/geo-it.json` (comuni italiani con codice catastale e CAP, località e frazioni, comuni soppressi, stati
esteri) è generato da `Scripts/Build-GeoData.py` unendo e riorganizzando le fonti che seguono. I dati sono forniti così
come sono, senza garanzie di accuratezza, completezza o aggiornamento: in particolare per i CAP non esiste una fonte
ufficiale aperta.

### ISTAT

- Dati: elenco dei comuni italiani (denominazione, sigla della provincia, codice catastale) e variazioni amministrative
  e territoriali dal 1991 (fusioni e cambi di nome).
- Fonte: [Istituto nazionale di statistica](https://www.istat.it/classificazione/codici-dei-comuni-delle-province-e-delle-regioni/).
- File sorgente: `https://www.istat.it/storage/codici-unita-amministrative/Elenco-comuni-italiani.csv` e
  `https://www.istat.it/storage/codici-unita-amministrative/Variazioni-amministrative-e-territoriali-dal-1991.zip`,
  scaricati il 1º ottobre 2026.
- Licenza: [Creative Commons Attribuzione 4.0 Internazionale](https://creativecommons.org/licenses/by/4.0/deed.it).
  I dati sono stati modificati: selezione dei campi e unione con le altre fonti.

### GeoNames

- Dati: codici postali italiani di comuni, frazioni e località.
- Fonte: [GeoNames](https://www.geonames.org/).
- File sorgente: `https://download.geonames.org/export/zip/IT.zip`, nella copia del 26 luglio 2026 incorporata anche nel
  programma BlackHole per Windows (SHA-256 `CFA48D8C0123154D5DB326FCC938AA0253CACEE26D69530FC8728F9352F23EFA`).
- Licenza: [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/).
  I dati sono stati modificati: nomi uniformati, voci abbreviate scartate, unione con le altre fonti.

### Wikidata

- Dati: codici postali dei comuni (proprietà P281), agganciati per codice catastale (proprietà P806).
- Fonte: [Wikidata](https://www.wikidata.org/), interrogata il 1º ottobre 2026.
- Licenza: [Creative Commons CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/deed.it).

### python-codicefiscale

- Dati: archivio storico dei comuni (da ANPR, Anagrafe nazionale della popolazione residente) e stati esteri con il
  relativo codice catastale, usati per i comuni soppressi o rinominati e per il codice fiscale di chi è nato all'estero.
- Progetto: [python-codicefiscale](https://github.com/fabiocaccamo/python-codicefiscale) di Fabio Caccamo, file della
  cartella `src/codicefiscale/data` scaricati il 1º ottobre 2026.
- Licenza: [MIT](https://github.com/fabiocaccamo/python-codicefiscale/blob/main/LICENSE.txt), © 2017-present Fabio Caccamo.

## Installazione

Il programma di installazione (`Setup\BlackHoleWorkspaces.iss`) è creato con [Inno Setup](https://jrsoftware.org/isinfo.php),
© 1997-2026 Jordan Russell, parti © 2000-2026 Martijn Laan ([licenza](https://jrsoftware.org/files/is/license.txt)).
