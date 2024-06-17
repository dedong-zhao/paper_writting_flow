## Research Paper Writing Flow
### Figure Processing
- Waveform: Print Window to eps file in Xcelium(A3, landscape, high cursor, blank padding before the first line) --> eps to pdf --> rotate and crop online --> reprint using Adobe for smaller size
- Design Layout: Innovus layout viewer --> WeChat screenshot --> add ruler in Visio --> output as pdf-->online crop
- Schemetic Figure: create in Visio --> output as pdf-->online crop
### Python Figure Setting
- Width
  - Single column: 3.5 ~ 4 inches
  - Double column: 7 ~ 8 inches
- Format
  ```
    plt.rcParams['font.family'] = 'Garamond'
    plt.rcParams['font.size'] = 10
    ax.spines['top'].set_visible(False)
    ax.spines['right'].set_visible(False)
    ax.grid(True, which='both', axis='y')
    plt.savefig('area.pdf', format='pdf', bbox_inches='tight', pad_inches=0)
  ```
### Writing Order
#### Implementation --> PPA analysis --> main content --> related works --> introduction --> abstract/conclusion/title

### Texmaker
#### Options --> Configure Texmaker --> Commands --> Bib(la)tex --> biber %
#### Options --> Configure Texmaker --> Quick Build
```
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```
#### Delete .bbl file geneated during compiling process
