# Gluaiseacht shimplí gan teorainneacha

Is féidir leat an mhuc a bhogadh leis na heochracha `wasd`.  Bogann sí
go réidh, ach is í an fhadhb atá ann ná gur féidir leat í a bhogadh go
hiomlán den scáileán.

## Míniú ar an gcód

Socraíonn script na muice suíomh tosaigh na muice.  Ansin, ritheann sé
i lúb gan stad, ag seiceáil an bhfuil na heochracha `w`, `a`, `s` nó
`d` brúite, agus ag bogadh beagán (tríd an gcomhordanáid _x_ nó _y_ a
athrú) má tá siad brúite. Socraítear méid na gluaiseachta leis an
athróg `speed`. Tá sé úsáideach an uimhir sin a choinneáil in athróg,
cé nach n-athraíonn sí, mar go mbíonn sé níos éasca an cód a
choigeartú agus a léamh dá bharr.


# Gluaiseacht shimplí, ag fanacht ar an scáileán

Is féidir leat an bhó a bhogadh leis na saigheadeochracha. Ní féidir
leat í a bhogadh den scáileán.

## Míniú ar an gcód

Tá an cód an-chosúil le cód na muice. Seo iad na codanna nua:

* Tá athróg againn darb ainm `x_limit` chun a shonrú cé chomh fada ar
  chlé agus ar dheis is féidir leis an mbó bogadh.  Sa lúb, ní
  cheadaímid gluaiseacht ar dheis ach amháin má tá comhordanáid _x_ na
  bó níos lú ná `x_limit`.  Ní cheadaímid gluaiseacht ar chlé ach
  amháin má tá comhordanáid _x_ na bó níos mó ná `-x_limit` (luach
  diúltach `x_limit`).

* Tá athróg againn darb ainm `y_limit` a dhéanann an obair chéanna
  maidir le gluaiseacht suas agus síos.


# Gluaiseacht le táimhe

Is féidir leat an gabhar a bhogadh leis na heochracha `ijkl`. Tógann
sé beagán ama air luas a mhéadú nó a laghdú.

## Míniú ar an gcód

Is é cód an ghabhair an ceann is casta. Coinnímid súil ar _treoluas_
an ghabhair sna treonna clé/deas agus suas/síos. Tá treoluas
an-chosúil le luas, ach cuimsíonn treoluas an treo ina bhfuil an
gabhar ag bogadh freisin.

Ní bhogann brú na heochrach `i` an gabhar suas go díreach. Ina ionad
sin, méadaíonn sé `y_velocity` de réir luach na hathróige `accel` suas
go teorainn áirithe.  Ar an gcaoi chéanna, laghdaíonn brú na heochrach
`k` `y_velocity`. Mura bhfuil `i` ná `k` brúite, athraíonn an treoluas
i dtreo nialais.

Déanaimid an rud céanna maidir le gluaiseacht ar chlé agus ar dheis,
tríd an athróg `x_velocity` a choigeartú.  Ansin, athraímid an
chomhordanáid _x_ de réir `x_velocity` agus an chomhordanáid _y_ de
réir `y_velocity`, ach cinntímid nach dtéann an gabhar thar na
teorainneacha atá leagtha síos dó.

Úsáidimid feidhmeanna `min()` agus `max()` Python lena chinntiú nach
n-éiríonn luachanna an dá athróg treoluais rómhór agus nach mbogann an
gabhar den scáileán.


# Buíochas

Gabhaimid buíochas le húsáideoir Pexels
[DamirK.](https://www.pexels.com/@damir/) as an ngrianghraf (atá
bearrtha agus coigeartaithe againn), agus le
[FreePixel.art](https://freepixel.art/) as na grafaicí ainmhithe.
