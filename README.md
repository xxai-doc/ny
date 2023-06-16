<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Ndibwino kuti muyike nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) poyamba, ndiyeno `direnv allow` mutalowa m'ndandanda ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) idzachitidwa pokhapokha mutalowa m'ndandanda).

Tanthauzo lake ndi: Kumasulira kwa Chitchaina kupita ku Japan, Korea, Chingerezi, kumasulira kwa Chingerezi kuzilankhulo zina zonse. Ngati mukufuna kungothandizira Chitchaina ndi Chingerezi, mutha kungolemba `zh: en` .

Tanthauzo lake ndi: Kumasulira kwa Chitchaina kupita ku Japan, Korea, Chingerezi, kumasulira kwa Chingerezi kuzilankhulo zina zonse. Ngati mukufuna kungothandizira Chitchaina ndi Chingerezi, mutha kungolemba `zh: en` .

* [kod komaliza](https://github.com/xxai-art/web)
* [Language mapaketi kwa malo lonse](https://github.com/xxai-art/web/tree/main/i18n)
* [Zinenero mapaketi a ma module olowera](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Zolemba za Zinenero Zambiri pa Webusaiti](https://github.com/xxai-doc)

Chiyankhulo chakumapeto kwa mapulogalamu ndi [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , chomwe chimawonjezera zinthu zina potengera kalembedwe ka khofi, onani [./coffee_plus.md](./coffee_plus.md) .

## Kupititsa patsogolo mawebusayiti ndi zolemba

Pangani mapulojekiti atatu otsatirawa

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Chokwanira ndi `.mdt` , mungagwiritse ntchito mawu ofanana ndi `<+ ./coffee_plus/import.js>` kutanthauza mafayilo akunja, ndi kupanga cholembapo ndi suffix `.md` .

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Kumasulira kwa Markdown sikumasulira ma code ndi maulalo, ndipo kusungitsa ziganizo zotanthauziridwa. Ngati zomasulirazo zasinthidwa koma zomasulirazo sizinasinthidwe, kubwerezanso sikudzachotsa zosinthidwazo.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  Mafayilo azilankhulo omasulira mawebusayiti opangidwa ndi `yaml` .

### Document Translation Automation Malangizo

Onani code repository [xxai-art/doc](https://github.com/xxai-art/doc)

Ndibwino kuti muyike nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) poyamba, ndiyeno `direnv allow` mutalowa m'ndandanda ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) idzachitidwa pokhapokha mutalowa m'ndandanda).

Pofuna kupewa ma code base omasuliridwa m'zilankhulo mazanamazana, ndidapanga ma code osiyana a chilankhulo chilichonse ndikupanga bungwe kuti lisunge ma code base.

Kukhazikitsa kusintha kwa chilengedwe `GITHUB_ACCESS_TOKEN` ndiyeno kuyendetsa [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) kudzangopanga posungira.

Inde, mutha kuyiyikanso mu code base.

Zomasulira zomasulira [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Script code imatanthauziridwa motere:

[bunx](https://bun.sh/docs/cli/bunx) ndi m'malo mwa npx, yomwe imakhala yachangu. Zachidziwikire, ngati mulibe bun, mutha kugwiritsa ntchito `npx` m'malo mwake.

`bunx mdt zh` renders `.mdt` mu chikwatu cha zh ngati `.md` , onani mafayilo awiri olumikizidwa pansipa

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` ndiye khodi yayikulu yomasulira (ngati muli ndi `nodejs` okha, koma `bun` ndi `direnv` sizinayikidwe, mutha kuyendetsanso `npx i18n` kumasulira).

Idzasiyanitsa [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , masinthidwe a `i18n.yml` mu chikalatachi ali motere:

```
en:
zh: ja ko en
```

Tanthauzo lake ndi: Kumasulira kwa Chitchaina kupita ku Japan, Korea, Chingerezi, kumasulira kwa Chingerezi kuzilankhulo zina zonse. Ngati mukufuna kungothandizira Chitchaina ndi Chingerezi, mutha kungolemba `zh: en` .

Chomaliza ndi [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , chomwe chimachotsa zomwe zili pakati pa mutu waukulu ndi mawu oyamba achilankhulo chilichonse `README.md` kuti alembe `README.md` . Khodiyo ndi yophweka kwambiri, mukhoza kuyang'ana nokha.

Google API imagwiritsidwa ntchito kumasulira kwaulere. Ngati simungathe kupeza Google, chonde konzani ndikukhazikitsa projekiti, monga:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Zomasulirazo zitulutsa kache yotanthauziridwa mu `.i18n` chikwatu, chonde yang'anani ndi `git status` ndikuwonjezera ku code repository kupewa kumasulira mobwerezabwereza.

Chonde thamangani `bunx i18n` nthawi iliyonse mukasintha zomasulira kuti musinthe posungira.

Ngati malemba oyambirira ndi kumasulira kusinthidwa nthawi yomweyo, cache idzasokonezeka, kotero ngati mukufuna kusintha, mukhoza kusintha chimodzi, ndiyeno muthamangitse `bunx i18n` kuti musinthe cache.
