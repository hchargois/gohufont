# Double-size, "HiDPI" versions

## Rationale

Some people asked me for a larger version of the font, specifically for higher-DPI screens.

I don't plan on designing new glyph shapes for higher resolutions. However, if all you want is a font that retains the same glyphs but double in size, it is possible to automatically scale the font so that each pixel in the 11-px (resp. 14-px) font is duplicated to occupy two pixels in width and two pixels in height of a then 22-px (resp. 28-px) large font.

I hacked together some lines of python to do just that. May work only depending on the phase of Moon.

I also throw in the output for 22-px and 28-px non-unicode bdfs. I opened them in gbdfed and they seem fine, but I didn't test them more that that, sorry.

## Usage

    # requires bdflib https://pypi.python.org/pypi/bdflib/
    python font_doubler.py < gohufont-11.bdf > gohufont-22.bdf

Works better with fingers crossed.
