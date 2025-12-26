# SF-Detector

An efficient and accurate method for detecting steady flows in network traffic.

## Abstract

Steady flows refer to packet flows whose packet arrival rates remain relatively steady across multiple consecutive time windows. SF-Detector separates the filtering and recording functions of packet flows, enabling efficient detection and reporting of steady flows.

## Key Features

- **Triple-counting Bloom Filter**: Filters out non-continuous flows across three consecutive time windows
- **Hash-table-based Record Table**: Precisely tracks and verifies potentially steady flows
- **Extreme Value-based Stability Check**: Avoids complex variance calculations by comparing max/min frequencies
- **Steady-count Replacement Mechanism**: Efficiently handles memory overflow

## Performance

- Precision: up to 95%
- Recall: nearly 100%
- Throughput: 40 MIPS

## Project Structure

```
.
├── main.tex                                    # LaTeX source file
├── The framework of the SF-Detector.png        # Framework figure
├── Non-continuous flow filter structure.png   # Filter structure figure
├── Data Structure of the Steady flow Record Table.png  # Record table figure
├── 图(a).png                                   # Parameter k experiment
├── 图(b).png                                   # Parameter β experiment
├── 图(c).png                                   # Parameter Γ experiment
└── README.md
```

## Compilation

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## Datasets

- CAIDA2020 / CAIDA2022: https://www.caida.org/catalog/datasets/passive_dataset
- MAWI: https://mawi.wide.ad.jp/mawi/

## License

MIT License
