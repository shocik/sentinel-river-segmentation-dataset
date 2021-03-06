# sentinel-river-segmentation-dataset

Zbiór zawiera 2961 kolorowych zdjęć satelitarnych rzek położonych w różnych strefach klimatycznych oraz odpowiadające im maski wskazujące piksele zbiorników wodnych. Wszystkie obrazy w bazie mają rozmiar 400x400 pikseli (zazwyczaj są one następnie skalowane podczas treningu, aby spełnić wymagania poszczególnych modeli). Obrazy użyte do budowy zbioru pochodzą z satelity Sentinel II. Zostały one pobrane z internetowej bazy Sentinel Hub EO Browser metodą półautomatyczną przy użyciu dodatku iMacros dla przeglądarki internetowej Firefox. Dodatek ten pozwala na automatyzację czynności wykonywanych w przeglądarce internetowej, dzięki czemu dane wielospektralne związane z zadanym widokiem EO Browser mogły zostać pobrane jednym kliknięciem myszy. Maski zbiorników wodnych zostały wygenerowane poprzez progowanie jednokanałowych obrazów z pasma bliskiej podczerwieni (pasmo 8A satelity Sentinel, ok. 864nm). Wartość progowa została wyznaczona automatycznie na podstawie analizy wygładzonego histogramu. Do budowy histogramu wykorzystano wartości pikseli z obrazów 8A, oddzielnie dla każdej rzeki. Jest to podyktowane faktem, że poszczególne rzeki występują w różnych typach klimatu i różnią się składem wody, co skutkuje różnicami w obrazach z pasma podczerwieni i optymalnych wartości progowych. Wygładzanie histogramów przeprowadzono za pomocą jednowymiarowej operacji konwolucji. Każdy histogram posiada pik dla niskich wartości jasności oraz drugi pik dla wysokich wartości jasności. Są one wykorzystywane w algorytmie, który znajduje wartość progową jako punkt o najmniejszej liczbie zliczeń pomiędzy tymi szczytami. Wykres przedstawia wygładzony histogram utworzony z obrazów pasma 8A dla części zbioru danych dotyczącej rzeki Wisły.

![histogram](https://i.postimg.cc/vBbFgYjw/obraz.png)

# Lista rzek:
- Dniepr,
- Dunaj,
- Garonna,
- Łaba,
- Ren,
- Jenisej,
- Loara,
- Missisipi,
- Nil,
- Ob,
- Pad,
- Pechora,
- Wisła,
- Wołga.
