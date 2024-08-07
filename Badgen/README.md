# Badgen

The original [badgen](https://github.com/badgen/badgen/tree/master) rewritten for OpenAF.

## Usage

To use, install the badgen opack:

````
opack install badgen
````

and load it in your code:

````javascript
var r = require("badgen.js")
r.badgen({ ... })
r.fromSVG(...)
````

## Examples

### Including in HTML

````javascript
templify('<img src="{{{svg}}}">', { svg: r.fromSVG(r.badgen({
    label : "This is",
    status: "in HTML",
    color : "013220"
})) })
````

<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iOTkuNSIgaGVpZ2h0PSIyMCIgdmlld0JveD0iMCAwIDk5NSAyMDAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgcm9sZT0iaW1nIiBhcmlhLWxhYmVsPSJUaGlzIGlzOiBpbiBIVE1MIj48dGl0bGU+VGhpcyBpczogaW4gSFRNTDwvdGl0bGU+PGxpbmVhckdyYWRpZW50IGlkPSJhIiB4Mj0iMCIgeTI9IjEwMCUiPjxzdG9wIG9mZnNldD0iMCIgc3RvcC1vcGFjaXR5PSIuMSIgc3RvcC1jb2xvcj0iI0VFRSIvPjxzdG9wIG9mZnNldD0iMSIgc3RvcC1vcGFjaXR5PSIuMSIvPjwvbGluZWFyR3JhZGllbnQ+PG1hc2sgaWQ9Im0iPjxyZWN0IHdpZHRoPSI5OTUiIGhlaWdodD0iMjAwIiByeD0iMzAiIGZpbGw9IiNGRkYiLz48L21hc2s+PGcgbWFzaz0idXJsKCNtKSI+PHJlY3Qgd2lkdGg9IjQ1MSIgaGVpZ2h0PSIyMDAiIGZpbGw9IiM1NTUiLz48cmVjdCB3aWR0aD0iNTQ0IiBoZWlnaHQ9IjIwMCIgZmlsbD0iIzAxMzIyMCIgeD0iNDUxIi8+PHJlY3Qgd2lkdGg9Ijk5NSIgaGVpZ2h0PSIyMDAiIGZpbGw9InVybCgjYSkiLz48L2c+PGcgYXJpYS1oaWRkZW49InRydWUiIGZpbGw9IiNmZmYiIHRleHQtYW5jaG9yPSJzdGFydCIgZm9udC1mYW1pbHk9IlZlcmRhbmEsRGVqYVZ1IFNhbnMsc2Fucy1zZXJpZiIgZm9udC1zaXplPSIxMTAiPjx0ZXh0IHg9IjYwIiB5PSIxNDgiIHRleHRMZW5ndGg9IjM1MSIgZmlsbD0iIzAwMCIgb3BhY2l0eT0iMC4yNSI+VGhpcyBpczwvdGV4dD48dGV4dCB4PSI1MCIgeT0iMTM4IiB0ZXh0TGVuZ3RoPSIzNTEiPlRoaXMgaXM8L3RleHQ+PHRleHQgeD0iNTA2IiB5PSIxNDgiIHRleHRMZW5ndGg9IjQ0NCIgZmlsbD0iIzAwMCIgb3BhY2l0eT0iMC4yNSI+aW4gSFRNTDwvdGV4dD48dGV4dCB4PSI0OTYiIHk9IjEzOCIgdGV4dExlbmd0aD0iNDQ0Ij5pbiBIVE1MPC90ZXh0PjwvZz48L3N2Zz4=">

### Simple badge

````javascript
io.writeFileString("badgen.svg", r.badgen({ 
    label: "Label", 
    status: "some issues", 
    color: 'yellow' 
}))
````

<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTE2LjgiIGhlaWdodD0iMjAiIHZpZXdCb3g9IjAgMCAxMTY4IDIwMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiByb2xlPSJpbWciIGFyaWEtbGFiZWw9IkxhYmVsOiBzb21lIGlzc3VlcyI+PHRpdGxlPkxhYmVsOiBzb21lIGlzc3VlczwvdGl0bGU+PGxpbmVhckdyYWRpZW50IGlkPSJhIiB4Mj0iMCIgeTI9IjEwMCUiPjxzdG9wIG9mZnNldD0iMCIgc3RvcC1vcGFjaXR5PSIuMSIgc3RvcC1jb2xvcj0iI0VFRSIvPjxzdG9wIG9mZnNldD0iMSIgc3RvcC1vcGFjaXR5PSIuMSIvPjwvbGluZWFyR3JhZGllbnQ+PG1hc2sgaWQ9Im0iPjxyZWN0IHdpZHRoPSIxMTY4IiBoZWlnaHQ9IjIwMCIgcng9IjMwIiBmaWxsPSIjRkZGIi8+PC9tYXNrPjxnIG1hc2s9InVybCgjbSkiPjxyZWN0IHdpZHRoPSIzOTIiIGhlaWdodD0iMjAwIiBmaWxsPSIjNTU1Ii8+PHJlY3Qgd2lkdGg9Ijc3NiIgaGVpZ2h0PSIyMDAiIGZpbGw9IiNEQjEiIHg9IjM5MiIvPjxyZWN0IHdpZHRoPSIxMTY4IiBoZWlnaHQ9IjIwMCIgZmlsbD0idXJsKCNhKSIvPjwvZz48ZyBhcmlhLWhpZGRlbj0idHJ1ZSIgZmlsbD0iI2ZmZiIgdGV4dC1hbmNob3I9InN0YXJ0IiBmb250LWZhbWlseT0iVmVyZGFuYSxEZWphVnUgU2FucyxzYW5zLXNlcmlmIiBmb250LXNpemU9IjExMCI+PHRleHQgeD0iNjAiIHk9IjE0OCIgdGV4dExlbmd0aD0iMjkyIiBmaWxsPSIjMDAwIiBvcGFjaXR5PSIwLjI1Ij5MYWJlbDwvdGV4dD48dGV4dCB4PSI1MCIgeT0iMTM4IiB0ZXh0TGVuZ3RoPSIyOTIiPkxhYmVsPC90ZXh0Pjx0ZXh0IHg9IjQ0NyIgeT0iMTQ4IiB0ZXh0TGVuZ3RoPSI2NzYiIGZpbGw9IiMwMDAiIG9wYWNpdHk9IjAuMjUiPnNvbWUgaXNzdWVzPC90ZXh0Pjx0ZXh0IHg9IjQzNyIgeT0iMTM4IiB0ZXh0TGVuZ3RoPSI2NzYiPnNvbWUgaXNzdWVzPC90ZXh0PjwvZz48L3N2Zz4=">

### With grey nAttrMon icon

````javascript
io.writeFileString("badgen.svg", r.badgen({ 
    label: "Label", 
    status: "it's okay", 
    color: 'green', 
    icon: r.fromSVG("svgs/nattrmon_grey.svg") 
}))
````

<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTE2LjQiIGhlaWdodD0iMjAiIHZpZXdCb3g9IjAgMCAxMTY0IDIwMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluayYjeDNEOyZxdW90O2h0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsmcXVvdDsgcm9sZT0iaW1nIiBhcmlhLWxhYmVsPSJMYWJlbDogaXQmYW1wO2Fwb3M7cyBva2F5Ij48dGl0bGU+TGFiZWw6IGl0JmFwb3M7cyBva2F5PC90aXRsZT48bGluZWFyR3JhZGllbnQgaWQ9ImEiIHgyPSIwIiB5Mj0iMTAwJSI+PHN0b3Agb2Zmc2V0PSIwIiBzdG9wLW9wYWNpdHk9Ii4xIiBzdG9wLWNvbG9yPSIjRUVFIi8+PHN0b3Agb2Zmc2V0PSIxIiBzdG9wLW9wYWNpdHk9Ii4xIi8+PC9saW5lYXJHcmFkaWVudD48bWFzayBpZD0ibSI+PHJlY3Qgd2lkdGg9IjExNjQiIGhlaWdodD0iMjAwIiByeD0iMzAiIGZpbGw9IiNGRkYiLz48L21hc2s+PGcgbWFzaz0idXJsKCNtKSI+PHJlY3Qgd2lkdGg9IjYwMiIgaGVpZ2h0PSIyMDAiIGZpbGw9IiM1NTUiLz48cmVjdCB3aWR0aD0iNTYyIiBoZWlnaHQ9IjIwMCIgZmlsbD0iIzNDMSIgeD0iNjAyIi8+PHJlY3Qgd2lkdGg9IjExNjQiIGhlaWdodD0iMjAwIiBmaWxsPSJ1cmwoI2EpIi8+PC9nPjxnIGFyaWEtaGlkZGVuPSJ0cnVlIiBmaWxsPSIjZmZmIiB0ZXh0LWFuY2hvcj0ic3RhcnQiIGZvbnQtZmFtaWx5PSJWZXJkYW5hLERlamFWdSBTYW5zLHNhbnMtc2VyaWYiIGZvbnQtc2l6ZT0iMTEwIj48dGV4dCB4PSIyNzAiIHk9IjE0OCIgdGV4dExlbmd0aD0iMjkyIiBmaWxsPSIjMDAwIiBvcGFjaXR5PSIwLjI1Ij5MYWJlbDwvdGV4dD48dGV4dCB4PSIyNjAiIHk9IjEzOCIgdGV4dExlbmd0aD0iMjkyIj5MYWJlbDwvdGV4dD48dGV4dCB4PSI2NTciIHk9IjE0OCIgdGV4dExlbmd0aD0iNDYyIiBmaWxsPSIjMDAwIiBvcGFjaXR5PSIwLjI1Ij5pdCZhcG9zO3Mgb2theTwvdGV4dD48dGV4dCB4PSI2NDciIHk9IjEzOCIgdGV4dExlbmd0aD0iNDYyIj5pdCZhcG9zO3Mgb2theTwvdGV4dD48L2c+PGltYWdlIHg9IjMwIiB5PSIxMCIgd2lkdGg9IjE4MCIgaGVpZ2h0PSIxODIiIHhsaW5rOmhyZWY9ImRhdGE6aW1hZ2Uvc3ZnK3htbDtiYXNlNjQsUEQ5NGJXd2dkbVZ5YzJsdmJqMGlNUzR3SWlCbGJtTnZaR2x1WnowaWRYUm1MVGdpUHo0S1BITjJaeUIzYVdSMGFEMGlNakFpSUdobGFXZG9kRDBpTWpBaUlIaHRiRzV6UFNKb2RIUndPaTh2ZDNkM0xuY3pMbTl5Wnk4eU1EQXdMM04yWnlJK0NpQWdJQ0E4Wno0S0lDQWdJQ0FnSUNBOGNHRjBhQ0JtYVd4c1BTSWpPVFU1UkVFMUlnb2dJQ0FnSUNBZ0lDQWdJQ0JrUFNKTklERTFMalV5TlNBeUxqTTVNaUJESURFMUxqQTBOQ0F5TGpFNU5TQXhOQzQxTXprZ01pNHdPVFVnTVRRdU1ESTFJREl1TURrMUlFTWdNVEl1TkRFNElESXVNRGsxSURFd0xqazROeUF6TGpBMU5pQXhNQzR6TnpZZ05DNDFOREVnUXlBeE1DNHlNemNnTkM0NE56a2dNVEF1TXprNUlEVXVNalkySURFd0xqY3pOeUExTGpRd05TQk1JREV6TGpFeE1TQTJMak00TVNCRElERXlMall5TWlBMkxqSTBNaUF4TWk0eE1EZ2dOaTR4TmpJZ01URXVOVGMySURZdU1UWXlJRU1nT0M0ME5qWWdOaTR4TmpJZ05TNDVNelVnT0M0Mk9USWdOUzQ1TXpVZ01URXVPREF5SUVNZ05TNDVNelVnTVRRdU9URXhJRGd1TkRZMklERTNMalEwSURFeExqVTNOaUF4Tnk0ME5DQkRJREV6TGpJNU5pQXhOeTQwTkNBeE5DNDRNemdnTVRZdU5qWXpJREUxTGpnM01pQXhOUzQwTkRNZ1F5QXhOUzQ0T1RVZ01UVXVOREl6SURFMUxqa3lOQ0F4TlM0ME1UTWdNVFV1T1RRMUlERTFMak00T1NCRElERTFMams0SURFMUxqTTBPU0F4TlM0NU9UWWdNVFV1TXpBeUlERTJMakF5TVNBeE5TNHlOVGNnUXlBeE5pNDNOalFnTVRRdU16QXlJREUzTGpJeE5DQXhNeTR4TURNZ01UY3VNakUwSURFeExqZ3dNU0JESURFM0xqSXhOQ0E1TGpZNE1TQXhOaTR3TXpjZ055NDRNelFnTVRRdU16QTFJRFl1T0RjZ1RDQXhOaTQ0TURnZ055NDRPVGtnUXlBeE5pNDRPRGdnTnk0NU16SWdNVFl1T1RjMElEY3VPVFE1SURFM0xqQTFPU0EzTGprME9TQkRJREUzTGpFME5pQTNMamswT1NBeE55NHlNeklnTnk0NU16SWdNVGN1TXpFMUlEY3VPRGs0SUVNZ01UY3VORGMzSURjdU9ESTVJREUzTGpZd05DQTNMamN3TVNBeE55NDJOekVnTnk0MU16a2dReUF4T0M0ME9UZ2dOUzQxTWpZZ01UY3VOVE0wSURNdU1qRTRJREUxTGpVeU5TQXlMak01TWlCYUlFMGdNVFV1T0RreElERXhMamd3TVNCRElERTFMamc1TVNBeE1pNDFPRGNnTVRVdU5qYzNJREV6TGpNeUlERTFMak13T1NBeE15NDVOVFVnVENBeE15NDBOU0F4TWk0ek16TWdReUF4TXk0NE56SWdNVEV1TXpFMElERXpMall6TVNBeE1DNHdPVGNnTVRJdU56VXhJRGt1TXpNM0lFTWdNVEl1TWpjeUlEZ3VPVEl6SURFeExqWTJNaUE0TGpZNU5pQXhNUzR3TXlBNExqWTVOaUJESURFd0xqSTJNeUE0TGpZNU5pQTVMalV6TnlBNUxqQXlPU0E1TGpBek5TQTVMall3T0NCRElEZ3VNRGczSURFd0xqY3dOaUE0TGpJd09TQXhNaTR6TnpNZ09TNHpNRGNnTVRNdU16SXhJRU1nT1M0M09EVWdNVE11TnpNMUlERXdMak01TlNBeE15NDVOak1nTVRFdU1ESTNJREV6TGprMk15QkRJREV4TGpZeU5DQXhNeTQ1TmpNZ01USXVNVGt5SURFekxqYzFOaUF4TWk0Mk5UTWdNVE11TXprMElFd2dNVFF1TkRjNElERTBMams0TlNCRElERXpMamN4TVNBeE5TNDJPRGNnTVRJdU5qa3pJREUyTGpFeE55QXhNUzQxTnpVZ01UWXVNVEUzSUVNZ09TNHhPVFFnTVRZdU1URTNJRGN1TWpVM0lERTBMakU0SURjdU1qVTNJREV4TGpnd01pQkRJRGN1TWpVM0lEa3VOREl5SURrdU1UazFJRGN1TkRnMklERXhMalUzTlNBM0xqUTROaUJESURFekxqazFOU0EzTGpRNE5TQXhOUzQ0T1RFZ09TNDBNakVnTVRVdU9Ea3hJREV4TGpnd01TQmFJRTBnTVRJdU1ESXhJREV5TGpFNE5TQkRJREV4TGpVMk5pQXhNaTQzTVRJZ01UQXVOams1SURFeUxqYzNOeUF4TUM0eE56TWdNVEl1TXpFNUlFTWdPUzQyTWpZZ01URXVPRFEzSURrdU5UWTFJREV4TGpBeE9DQXhNQzR3TXpjZ01UQXVORGN6SUVNZ01UQXVNamcySURFd0xqRTRNeUF4TUM0Mk5EZ2dNVEF1TURFNElERXhMakF6SURFd0xqQXhPQ0JESURFeExqTTBOQ0F4TUM0d01UZ2dNVEV1TmpRNUlERXdMakV6TVNBeE1TNDRPRFlnTVRBdU16TTNJRU1nTVRJdU5ETXpJREV3TGpneElERXlMalE1TkNBeE1TNDJNemtnTVRJdU1ESXhJREV5TGpFNE5TQmFJRTBnTVRZdU5qSXlJRFl1TXpreUlFd2dNVEV1T1RNZ05DNDBOalFnUXlBeE1pNDJNVElnTXk0MU5TQXhNeTQ1TVRRZ015NHhOaUF4TlM0d01qRWdNeTQyTVRZZ1F5QXhOaTR4TkRZZ05DNHdOemdnTVRZdU56YzNJRFV1TWpNNElERTJMall5TWlBMkxqTTVNaUJhSWdvZ0lDQWdJQ0FnSUNBZ0lDQnpkSGxzWlQwaUlpQXZQZ29nSUNBZ1BDOW5QZ284TDNOMlp6ND0iLz48L3N2Zz4=">

### With orange nAttrMon icon

````javascript
io.writeFileString("badgen.svg", r.badgen({ 
    label: "Label", 
    status: "it's okay", 
    color: 'green', 
    icon: r.fromSVG("svgs/nattrmon.svg") 
}))
````

<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTE2LjQiIGhlaWdodD0iMjAiIHZpZXdCb3g9IjAgMCAxMTY0IDIwMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluayYjeDNEOyZxdW90O2h0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsmcXVvdDsgcm9sZT0iaW1nIiBhcmlhLWxhYmVsPSJMYWJlbDogaXQmYW1wO2Fwb3M7cyBva2F5Ij48dGl0bGU+TGFiZWw6IGl0JmFwb3M7cyBva2F5PC90aXRsZT48bGluZWFyR3JhZGllbnQgaWQ9ImEiIHgyPSIwIiB5Mj0iMTAwJSI+PHN0b3Agb2Zmc2V0PSIwIiBzdG9wLW9wYWNpdHk9Ii4xIiBzdG9wLWNvbG9yPSIjRUVFIi8+PHN0b3Agb2Zmc2V0PSIxIiBzdG9wLW9wYWNpdHk9Ii4xIi8+PC9saW5lYXJHcmFkaWVudD48bWFzayBpZD0ibSI+PHJlY3Qgd2lkdGg9IjExNjQiIGhlaWdodD0iMjAwIiByeD0iMzAiIGZpbGw9IiNGRkYiLz48L21hc2s+PGcgbWFzaz0idXJsKCNtKSI+PHJlY3Qgd2lkdGg9IjYwMiIgaGVpZ2h0PSIyMDAiIGZpbGw9IiM1NTUiLz48cmVjdCB3aWR0aD0iNTYyIiBoZWlnaHQ9IjIwMCIgZmlsbD0iIzNDMSIgeD0iNjAyIi8+PHJlY3Qgd2lkdGg9IjExNjQiIGhlaWdodD0iMjAwIiBmaWxsPSJ1cmwoI2EpIi8+PC9nPjxnIGFyaWEtaGlkZGVuPSJ0cnVlIiBmaWxsPSIjZmZmIiB0ZXh0LWFuY2hvcj0ic3RhcnQiIGZvbnQtZmFtaWx5PSJWZXJkYW5hLERlamFWdSBTYW5zLHNhbnMtc2VyaWYiIGZvbnQtc2l6ZT0iMTEwIj48dGV4dCB4PSIyNzAiIHk9IjE0OCIgdGV4dExlbmd0aD0iMjkyIiBmaWxsPSIjMDAwIiBvcGFjaXR5PSIwLjI1Ij5MYWJlbDwvdGV4dD48dGV4dCB4PSIyNjAiIHk9IjEzOCIgdGV4dExlbmd0aD0iMjkyIj5MYWJlbDwvdGV4dD48dGV4dCB4PSI2NTciIHk9IjE0OCIgdGV4dExlbmd0aD0iNDYyIiBmaWxsPSIjMDAwIiBvcGFjaXR5PSIwLjI1Ij5pdCZhcG9zO3Mgb2theTwvdGV4dD48dGV4dCB4PSI2NDciIHk9IjEzOCIgdGV4dExlbmd0aD0iNDYyIj5pdCZhcG9zO3Mgb2theTwvdGV4dD48L2c+PGltYWdlIHg9IjMwIiB5PSIxMCIgd2lkdGg9IjE4MCIgaGVpZ2h0PSIxODIiIHhsaW5rOmhyZWY9ImRhdGE6aW1hZ2Uvc3ZnK3htbDtiYXNlNjQsUEQ5NGJXd2dkbVZ5YzJsdmJqMGlNUzR3SWlCbGJtTnZaR2x1WnowaWRYUm1MVGdpUHo0S1BITjJaeUIzYVdSMGFEMGlNakFpSUdobGFXZG9kRDBpTWpBaUlIaHRiRzV6UFNKb2RIUndPaTh2ZDNkM0xuY3pMbTl5Wnk4eU1EQXdMM04yWnlJK0NpQWdJQ0E4Wno0S0lDQWdJQ0FnSUNBOGNHRjBhQ0JtYVd4c1BTSWpaR1UzT0RNNUlnb2dJQ0FnSUNBZ0lDQWdJQ0JrUFNKTklERTFMalV5TlNBeUxqTTVNaUJESURFMUxqQTBOQ0F5TGpFNU5TQXhOQzQxTXprZ01pNHdPVFVnTVRRdU1ESTFJREl1TURrMUlFTWdNVEl1TkRFNElESXVNRGsxSURFd0xqazROeUF6TGpBMU5pQXhNQzR6TnpZZ05DNDFOREVnUXlBeE1DNHlNemNnTkM0NE56a2dNVEF1TXprNUlEVXVNalkySURFd0xqY3pOeUExTGpRd05TQk1JREV6TGpFeE1TQTJMak00TVNCRElERXlMall5TWlBMkxqSTBNaUF4TWk0eE1EZ2dOaTR4TmpJZ01URXVOVGMySURZdU1UWXlJRU1nT0M0ME5qWWdOaTR4TmpJZ05TNDVNelVnT0M0Mk9USWdOUzQ1TXpVZ01URXVPREF5SUVNZ05TNDVNelVnTVRRdU9URXhJRGd1TkRZMklERTNMalEwSURFeExqVTNOaUF4Tnk0ME5DQkRJREV6TGpJNU5pQXhOeTQwTkNBeE5DNDRNemdnTVRZdU5qWXpJREUxTGpnM01pQXhOUzQwTkRNZ1F5QXhOUzQ0T1RVZ01UVXVOREl6SURFMUxqa3lOQ0F4TlM0ME1UTWdNVFV1T1RRMUlERTFMak00T1NCRElERTFMams0SURFMUxqTTBPU0F4TlM0NU9UWWdNVFV1TXpBeUlERTJMakF5TVNBeE5TNHlOVGNnUXlBeE5pNDNOalFnTVRRdU16QXlJREUzTGpJeE5DQXhNeTR4TURNZ01UY3VNakUwSURFeExqZ3dNU0JESURFM0xqSXhOQ0E1TGpZNE1TQXhOaTR3TXpjZ055NDRNelFnTVRRdU16QTFJRFl1T0RjZ1RDQXhOaTQ0TURnZ055NDRPVGtnUXlBeE5pNDRPRGdnTnk0NU16SWdNVFl1T1RjMElEY3VPVFE1SURFM0xqQTFPU0EzTGprME9TQkRJREUzTGpFME5pQTNMamswT1NBeE55NHlNeklnTnk0NU16SWdNVGN1TXpFMUlEY3VPRGs0SUVNZ01UY3VORGMzSURjdU9ESTVJREUzTGpZd05DQTNMamN3TVNBeE55NDJOekVnTnk0MU16a2dReUF4T0M0ME9UZ2dOUzQxTWpZZ01UY3VOVE0wSURNdU1qRTRJREUxTGpVeU5TQXlMak01TWlCYUlFMGdNVFV1T0RreElERXhMamd3TVNCRElERTFMamc1TVNBeE1pNDFPRGNnTVRVdU5qYzNJREV6TGpNeUlERTFMak13T1NBeE15NDVOVFVnVENBeE15NDBOU0F4TWk0ek16TWdReUF4TXk0NE56SWdNVEV1TXpFMElERXpMall6TVNBeE1DNHdPVGNnTVRJdU56VXhJRGt1TXpNM0lFTWdNVEl1TWpjeUlEZ3VPVEl6SURFeExqWTJNaUE0TGpZNU5pQXhNUzR3TXlBNExqWTVOaUJESURFd0xqSTJNeUE0TGpZNU5pQTVMalV6TnlBNUxqQXlPU0E1TGpBek5TQTVMall3T0NCRElEZ3VNRGczSURFd0xqY3dOaUE0TGpJd09TQXhNaTR6TnpNZ09TNHpNRGNnTVRNdU16SXhJRU1nT1M0M09EVWdNVE11TnpNMUlERXdMak01TlNBeE15NDVOak1nTVRFdU1ESTNJREV6TGprMk15QkRJREV4TGpZeU5DQXhNeTQ1TmpNZ01USXVNVGt5SURFekxqYzFOaUF4TWk0Mk5UTWdNVE11TXprMElFd2dNVFF1TkRjNElERTBMams0TlNCRElERXpMamN4TVNBeE5TNDJPRGNnTVRJdU5qa3pJREUyTGpFeE55QXhNUzQxTnpVZ01UWXVNVEUzSUVNZ09TNHhPVFFnTVRZdU1URTNJRGN1TWpVM0lERTBMakU0SURjdU1qVTNJREV4TGpnd01pQkRJRGN1TWpVM0lEa3VOREl5SURrdU1UazFJRGN1TkRnMklERXhMalUzTlNBM0xqUTROaUJESURFekxqazFOU0EzTGpRNE5TQXhOUzQ0T1RFZ09TNDBNakVnTVRVdU9Ea3hJREV4TGpnd01TQmFJRTBnTVRJdU1ESXhJREV5TGpFNE5TQkRJREV4TGpVMk5pQXhNaTQzTVRJZ01UQXVOams1SURFeUxqYzNOeUF4TUM0eE56TWdNVEl1TXpFNUlFTWdPUzQyTWpZZ01URXVPRFEzSURrdU5UWTFJREV4TGpBeE9DQXhNQzR3TXpjZ01UQXVORGN6SUVNZ01UQXVNamcySURFd0xqRTRNeUF4TUM0Mk5EZ2dNVEF1TURFNElERXhMakF6SURFd0xqQXhPQ0JESURFeExqTTBOQ0F4TUM0d01UZ2dNVEV1TmpRNUlERXdMakV6TVNBeE1TNDRPRFlnTVRBdU16TTNJRU1nTVRJdU5ETXpJREV3TGpneElERXlMalE1TkNBeE1TNDJNemtnTVRJdU1ESXhJREV5TGpFNE5TQmFJRTBnTVRZdU5qSXlJRFl1TXpreUlFd2dNVEV1T1RNZ05DNDBOalFnUXlBeE1pNDJNVElnTXk0MU5TQXhNeTQ1TVRRZ015NHhOaUF4TlM0d01qRWdNeTQyTVRZZ1F5QXhOaTR4TkRZZ05DNHdOemdnTVRZdU56YzNJRFV1TWpNNElERTJMall5TWlBMkxqTTVNaUJhSWdvZ0lDQWdJQ0FnSUNBZ0lDQnpkSGxzWlQwaUlpQXZQZ29nSUNBZ1BDOW5QZ284TDNOMlp6ND0iLz48L3N2Zz4=">