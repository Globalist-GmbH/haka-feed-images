#  Feed-Bilder (weisser Hintergrund)

Geflattete Packshots fuer das Google Merchant Center.

**Warum:** Die Shop-Bilder sind transparente PNGs. Google rendert Transparenz bei
hellen Produkten teils vor Schwarz (Merchant-Hilfe), und die Flaeche unter
dem Alphakanal kippt beim Herunterskalieren von Weiss auf Schwarz. Fuer den Feed
braucht es deshalb ein zweites Bildset ohne Alphakanal. Website, Newsletter und
Print behalten unveraendert die transparenten PNGs.

**Inhalt:** `img/<datei>_w.jpg` - JPG, echtes Weiss (255,255,255), kein Alpha,
max. 1600 px. `manifest.json` mappt die Original-URL auf die Datei.

Erzeugt von `clients/haka/scripts/flatten-feed-images.py`, eingespielt per
Supplemental-Datenquelle "Image Overrides" () mit
`clients/haka/scripts/push-supplemental-images.cjs`.
