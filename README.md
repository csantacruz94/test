## Indice

**[1. Introduzione](#introduzione)**

**[2. Vertical](#vertical)**

* [2.1 Crea Vertical](#crea-vertical)
* [2.2 Modifica Vertical](#modifica-vertical)
* [2.3 Elimina Vertical](#elimina-vertical)

**[3. Categoria](#categoria)**

* [3.1 Crea Categoria](#crea-categoria)
* [3.2 Modifica Categoria](#modifica-categoria)
* [3.3 Elimina Categoria](#elimina-categoria)

**[4. Esempio](#esempio)**

* [4.1 Crea Esempio](#crea-esempio)
* [4.2 Modifica Esempio](#modifica-esempio)
* [4.3 Elimina Esempio](#elimina-esempio)



# <a name="introduzione">1. Introduzione</a>

Questo documento riguarda le modifiche e creazione dei vertical.<br>
Sono descritte con maggiore dettaglio solo le proprietà del json più interessate ad essere modificate in futuro, sono le seguenti: showcase, categories, examples

# <a name="vertical">2. Vertical</a>
## <a name="crea-vertical">2.1 Crea Vertical</a>

Di seguito la struttura json completa di un vertical

```json
{
  "id": 1,
  "name": "GDO",
  "slug": "gdo",
  "route": "/gdo",
  "img_homepage": "assets/homepage/gdo_home_generale.jpg",
  "img_homepage_2x": "assets/homepage/gdo_home_generale_2x.jpg",
  "img_menu_desktop": "assets/menu/gdo_desktop.jpg",
  "img_menu_desktop_2x": "assets/menu/gdo_desktop_2x.jpg",
  "img_menu_mobile": "assets/menu/gdo_mobile.jpg",
  "img_menu_mobile_2x": "assets/menu/gdo_mobile_2x.jpg",
  "icon": {
    "name": "cart",
    "is_tall": false
  },
  "showcase": {
    "title": "GDO",
    "titleBig": "Alcuni dei nostri clienti",
    "description": "Grazie alla grande efficacia degli <strong>strumenti ad alte performance Ediscom</strong> e all’utilizzo di <strong>soluzioni multicanale</strong>, la nostra azienda è in grado di portare i propri partner al <strong>raggiungimento di risultati concreti.</strong> Tramite lo studio comportamentale del pubblico e un’adeguata comprensione delle sue esigenze, realizziamo contenuti in grado di <strong>rispondere in maniera rapida alle richieste</strong> della clientela. Saranno Account dedicati ad occuparsi in prima persona del successo del nostro partner, con <strong>assistenza e supporto costanti</strong>, lo accompagneranno nella realizzazione del proprio progetto di business, dalla creazione di una strategia alla valutazione delle performance ottenute. Infatti, mediante un’accurata analisi, siamo in grado di fornire alle aziende un adeguato <strong>monitoraggio e tracciamento delle prestazioni delle campagne</strong> e procedere, sulla base dei dati raccolti, <strong>all’ottimizzazione delle stesse.</strong>",
    "subtitle": "Hanno scelto Ediscom:",
    "clients": [
      {
        "description": "Selex",
        "logo": "selex.svg"
      }
    ]
  },
  "categories": [
    {
      "id": 1,
      "title": "ESEMPI GDO",
      "slug": "esempi",
      "iconName": "cart",
      "examples": [
        {
          "id": 1,
          "title": "DEM | Eventi e Ricorrenze",
          "slug": "dem_eventi_e_ricorrenze",
          "route": "/gdo/esempi/dem_eventi_e_ricorrenze",
          "iconName": "",
          "description": "Il <strong>Direct Email Marketing</strong> è una delle soluzioni per <strong>promuovere la propria attività, ottenere nuovi contatti qualificati, posizionare il brand sul mercato</strong> e <strong>migliorare l’<i>engagement</i> con il pubblico.</strong> Attraverso la creazione di DEM personalizzate, inviate ad <strong>anagrafiche segmentate</strong> e che rimandano a landing page ottimizzate, infatti, è possibile ad esempio impattare su <strong>enormi volumi di audience in target</strong> con il business del cliente.",
          "flusso": {
            "deviceIsDesktop": false,
            "mockups": [
              {
                "id": "dem_eventi_e_ricorrenze_step1",
                "name": "STEP 1",
                "description": "L’utente riceve la DEM informativa con codice sconto e, cliccando sulla call to action, viene reindirizzato su una landing page, pensata per essere cross device e ottimizzata dal punto di vista creativo.",
                "img": "assets/gdo/images/esempi/lp_dem_eventi_e_ricorrenze/01_DEM_coupon_sconto_natale_.jpg",
                "img_2x": "assets/gdo/images/esempi/lp_dem_eventi_e_ricorrenze/01_DEM_coupon_sconto_natale_2x_.jpg"
              },
              {
                "id": "dem_eventi_e_ricorrenze_step2",
                "name": "STEP 2",
                "description": "Una volta atterrato sulla landing page, l’utente riceve maggiori informazioni sulla promozione e viene invitato a partecipare alle iniziative del brand.",
                "img": "assets/gdo/images/esempi/lp_dem_eventi_e_ricorrenze/02_coupon_sconto_natale_.jpg",
                "img_2x": "assets/gdo/images/esempi/lp_dem_eventi_e_ricorrenze/02_coupon_sconto_natale_2x_.jpg"
              }
            ]
          },
          "video": {
            "id": "lp_dem_festivita-video",
            "src": "assets/gdo/video/esempi/dem_lp_festivita_.mp4",
            "poster": "assets/gdo/images/esempi/lp_dem_eventi_e_ricorrenze/video_poster.jpg",
            "deviceIsDesktop": false
          }
        }
      ]
    }
  ]
}
```
### Percorso

> Il file json da modificare si trova al percorso:
> 
> Porfolio-Sales/projects/portfolio/src/verticals.json

Questo file contiene un array di oggetti dove ogni oggetto corrisponde ad un vertical. Per proseguire con la creazione del vertical bisogna copiare la struttura esatta dell'oggetto esistente poi inserirlo in fondo all'array infine fare le modifiche delle varie proprietà esistenti.

> **Attenzione**
> 
> Durante la duplicazione dell'oggetto assicurarti di mettere in ordine crescente gli **id** dei vari oggetti vertical, eliminare o modificare le proprietà che contengo al loro interno altri dati:
> - showcase
> - categories

Struttura vertical

```json
{
  "id": 1,
  "name": "GDO",
  "slug": "gdo",
  "route": "/gdo",
  "img_homepage": "assets/homepage/gdo_home_generale.jpg",
  "img_homepage_2x": "assets/homepage/gdo_home_generale_2x.jpg",
  "img_menu_desktop": "assets/menu/gdo_desktop.jpg",
  "img_menu_desktop_2x": "assets/menu/gdo_desktop_2x.jpg",
  "img_menu_mobile": "assets/menu/gdo_mobile.jpg",
  "img_menu_mobile_2x": "assets/menu/gdo_mobile_2x.jpg",
  "icon": {
    "name": "cart",
    "is_tall": false
  },
  "showcase": { /* -------------- proprietà interessata ------------- */
    "title": "GDO",
    "titleBig": "Alcuni dei nostri clienti",
    "description": "",
    "subtitle": "Hanno scelto Ediscom:",
    "clients": [
      {
        "description": "Selex",
        "logo": "selex.svg"
      }
    ]
  },
  
  "categories": [  /* -------------- proprietà interessata ------------- */
    {
      "id": 1,
      "title": "ESEMPI GDO",
      "slug": "esempi",
      "iconName": "cart",
      "examples": []
    }
  ]
}
```
> **Attenzione**
>
> All'interno dello **showcase** fare attenzione alla proprietà **clients**.
> 
> All'interno di **categories** fare attenzione alla proprietà **examples** che contiene un array di oggetti che sono gli esempi di una determinata categoria. 


## <a name="modifica-vertical">2.2 Modifica Vertical</a>
### Percorso

> Il file json da modificare si trova al percorso:
>
> Porfolio-Sales/projects/portfolio/src/verticals.json

In questo file trova l'oggetto in questione e modifica la parte interessata.

## <a name="elimina-vertical">2.3 Elimina Vertical</a>
### Percorso

> Il file json da modificare si trova al percorso:
>
> Porfolio-Sales/projects/portfolio/src/verticals.json

In questo file trova l'oggetto in questione e eliminalo del tutto dall'array in cui si trova.
> **Attenzione**
>
> Durante l'eliminazione metti in ordine crescente la proprietà **id** dei vari oggetti vertical

ad esempio

```json
[
  {
    "id": 1,  /* ---------- ATTENZIONE -----------*/
    "name": "GDO",
    "slug": "gdo",
    "route": "/gdo",
    "img_homepage": "assets/homepage/gdo_home_generale.jpg",
    "img_homepage_2x": "assets/homepage/gdo_home_generale_2x.jpg",
    "img_menu_desktop": "assets/menu/gdo_desktop.jpg",
    "img_menu_desktop_2x": "assets/menu/gdo_desktop_2x.jpg",
    "img_menu_mobile": "assets/menu/gdo_mobile.jpg",
    "img_menu_mobile_2x": "assets/menu/gdo_mobile_2x.jpg",
    "icon": {
      "name": "cart",
      "is_tall": false
    },
    "showcase": {...},
    "categories": [...]
  },
  {
    "id": 2,  /* ---------- ATTENZIONE -----------*/
    "name": "GDO",
    "slug": "gdo",
    "route": "/gdo",
    "img_homepage": "assets/homepage/gdo_home_generale.jpg",
    "img_homepage_2x": "assets/homepage/gdo_home_generale_2x.jpg",
    "img_menu_desktop": "assets/menu/gdo_desktop.jpg",
    "img_menu_desktop_2x": "assets/menu/gdo_desktop_2x.jpg",
    "img_menu_mobile": "assets/menu/gdo_mobile.jpg",
    "img_menu_mobile_2x": "assets/menu/gdo_mobile_2x.jpg",
    "icon": {
      "name": "cart",
      "is_tall": false
    },
    "showcase": {...},
    "categories": [...]
  },
  {
    "id": 3,  /* ---------- ATTENZIONE -----------*/
    "name": "GDO",
    "slug": "gdo",
    "route": "/gdo",
    "img_homepage": "assets/homepage/gdo_home_generale.jpg",
    "img_homepage_2x": "assets/homepage/gdo_home_generale_2x.jpg",
    "img_menu_desktop": "assets/menu/gdo_desktop.jpg",
    "img_menu_desktop_2x": "assets/menu/gdo_desktop_2x.jpg",
    "img_menu_mobile": "assets/menu/gdo_mobile.jpg",
    "img_menu_mobile_2x": "assets/menu/gdo_mobile_2x.jpg",
    "icon": {
      "name": "cart",
      "is_tall": false
    },
    "showcase": {...},
    "categories": [...]
  }
]
```

# <a name="categoria">3. Categoria</a>
## <a name="crea-categoria">3.1 Crea Categoria</a>
### Percorso

> Il file json da modificare si trova al percorso:
>
> Porfolio-Sales/projects/portfolio/src/verticals.json

In questo file recati nella proprietà **categories**

```json
{
  "id": 1,
  "name": "GDO",
  "slug": "gdo",
  "route": "/gdo",
  "img_homepage": "assets/homepage/gdo_home_generale.jpg",
  "img_homepage_2x": "assets/homepage/gdo_home_generale_2x.jpg",
  "img_menu_desktop": "assets/menu/gdo_desktop.jpg",
  "img_menu_desktop_2x": "assets/menu/gdo_desktop_2x.jpg",
  "img_menu_mobile": "assets/menu/gdo_mobile.jpg",
  "img_menu_mobile_2x": "assets/menu/gdo_mobile_2x.jpg",
  "icon": {
    "name": "cart",
    "is_tall": false
  },
  "showcase": {
    "title": "GDO",
    "titleBig": "Alcuni dei nostri clienti",
    "description": "",
    "subtitle": "Hanno scelto Ediscom:",
    "clients": [
      {
        "description": "Selex",
        "logo": "selex.svg"
      }
    ]
  },
  "categories": [ /* ----- proprietà interessata ------*/
    {
      "id": 1,
      "title": "ESEMPI GDO",
      "slug": "esempi",
      "iconName": "cart",
      "examples": []
    }
  ]
}
```
**categories** è un array di oggetti quindi per creare un'altra categoria all'interno del vertical basta duplicare l'oggetto e inserirlo in fondo all'array.

ad esempio la nuova struttura subito dopo la duplicazione sarà così:
```json
{
  "id": 1,
  "name": "GDO",
  "slug": "gdo",
  "route": "/gdo",
  "img_homepage": "assets/homepage/gdo_home_generale.jpg",
  "img_homepage_2x": "assets/homepage/gdo_home_generale_2x.jpg",
  "img_menu_desktop": "assets/menu/gdo_desktop.jpg",
  "img_menu_desktop_2x": "assets/menu/gdo_desktop_2x.jpg",
  "img_menu_mobile": "assets/menu/gdo_mobile.jpg",
  "img_menu_mobile_2x": "assets/menu/gdo_mobile_2x.jpg",
  "icon": {
    "name": "cart",
    "is_tall": false
  },
  "showcase": {
    "title": "GDO",
    "titleBig": "Alcuni dei nostri clienti",
    "description": "",
    "subtitle": "Hanno scelto Ediscom:",
    "clients": [
      {
        "description": "Selex",
        "logo": "selex.svg"
      }
    ]
  },
  "categories": [ /* ----- proprietà interessata ------*/
    {
      "id": 1,
      "title": "ESEMPI GDO",
      "slug": "esempi",
      "iconName": "cart",
      "examples": []
    },
    {
      "id": 2,  /* ----- nuova categoria ------*/
      "title": "ESEMPI GDO",
      "slug": "esempi",
      "iconName": "cart",
      "examples": []
    },
    {
      "id": 2, /* ----- nuova categoria ------*/
      "title": "ESEMPI GDO",
      "slug": "esempi",
      "iconName": "cart",
      "examples": []
    }
  ]
}
```

> **Attenzione**
>
> Durante la creazione di nuove categorie metti in ordine crescente la proprietà **id** dei vari oggetti categoria e modifica o elimina i dati all'interno della proprietà **examples**

## <a name="modifica-categoria">3.2 Modifica Categoria</a>
### Percorso

> Il file json da modificare si trova al percorso:
>
> Porfolio-Sales/projects/portfolio/src/verticals.json

In questo file recati nella proprietà **categories** trova l'oggetto in questione e modifica la parte interessata. 

## <a name="elimina-categoria">3.3 Elimina Categoria</a>
### Percorso

> Il file json da modificare si trova al percorso:
>
> Porfolio-Sales/projects/portfolio/src/verticals.json

In questo file recati nella proprietà **categories** trova l'oggetto in questione e elimina dall'array in cui si trova.

> **Attenzione**
>
> Durante l'eliminazione metti in ordine crescente la proprietà **id** dei vari oggetti categoria

# <a name="esempio">4 Esempio</a>
## <a name="crea-esempio">4.1 Crea Esempio</a>
### Percorso

> Il file json da modificare si trova al percorso:
>
> Porfolio-Sales/projects/portfolio/src/verticals.json

In questo file recati nella proprietà **categories** e subito dopo su **examples**

```json
{
  "id": 1,
  "name": "GDO",
  "slug": "gdo",
  "route": "/gdo",
  "img_homepage": "assets/homepage/gdo_home_generale.jpg",
  "img_homepage_2x": "assets/homepage/gdo_home_generale_2x.jpg",
  "img_menu_desktop": "assets/menu/gdo_desktop.jpg",
  "img_menu_desktop_2x": "assets/menu/gdo_desktop_2x.jpg",
  "img_menu_mobile": "assets/menu/gdo_mobile.jpg",
  "img_menu_mobile_2x": "assets/menu/gdo_mobile_2x.jpg",
  "icon": {
    "name": "cart",
    "is_tall": false
  },
  "showcase": {
    "title": "GDO",
    "titleBig": "Alcuni dei nostri clienti",
    "description": "",
    "subtitle": "Hanno scelto Ediscom:",
    "clients": [
      {
        "description": "Selex",
        "logo": "selex.svg"
      }
    ]
  },
  "categories": [ 
    {
      "id": 1,
      "title": "ESEMPI GDO",
      "slug": "esempi",
      "iconName": "cart",
      "examples": [ /* ----- proprietà interessata ------*/
        {
          "id": 1,
          "title": "DEM | Eventi e Ricorrenze",
          "slug": "dem_eventi_e_ricorrenze",
          "route": "/gdo/esempi/dem_eventi_e_ricorrenze",
          "iconName": "",
          "description": "Il <strong>Direct Email Marketing</strong> è una delle soluzioni per <strong>promuovere la propria attività, ottenere nuovi contatti qualificati, posizionare il brand sul mercato</strong> e <strong>migliorare l’<i>engagement</i> con il pubblico.</strong> Attraverso la creazione di DEM personalizzate, inviate ad <strong>anagrafiche segmentate</strong> e che rimandano a landing page ottimizzate, infatti, è possibile ad esempio impattare su <strong>enormi volumi di audience in target</strong> con il business del cliente.",
          "flusso": {
            "deviceIsDesktop": false,
            "mockups": []
          },
          "video": {
            "id": "lp_dem_festivita-video",
            "src": "assets/gdo/video/esempi/dem_lp_festivita_.mp4",
            "poster": "assets/gdo/images/esempi/lp_dem_eventi_e_ricorrenze/video_poster.jpg",
            "deviceIsDesktop": false
          }
        }
      ]
    }
  ]
}
```
**examples** è un array di oggetti dove per creare un altrao esempio basta duplicare l'oggetto e inserirlo in fondo all'array.

Dopo la creazione la nuova struttura sarà così ad esempio:

```json
{
  "id": 1,
  "name": "GDO",
  "slug": "gdo",
  "route": "/gdo",
  "img_homepage": "assets/homepage/gdo_home_generale.jpg",
  "img_homepage_2x": "assets/homepage/gdo_home_generale_2x.jpg",
  "img_menu_desktop": "assets/menu/gdo_desktop.jpg",
  "img_menu_desktop_2x": "assets/menu/gdo_desktop_2x.jpg",
  "img_menu_mobile": "assets/menu/gdo_mobile.jpg",
  "img_menu_mobile_2x": "assets/menu/gdo_mobile_2x.jpg",
  "icon": {
    "name": "cart",
    "is_tall": false
  },
  "showcase": {
    "title": "GDO",
    "titleBig": "Alcuni dei nostri clienti",
    "description": "",
    "subtitle": "Hanno scelto Ediscom:",
    "clients": [
      {
        "description": "Selex",
        "logo": "selex.svg"
      }
    ]
  },
  "categories": [ 
    {
      "id": 1,
      "title": "ESEMPI GDO",
      "slug": "esempi",
      "iconName": "cart",
      "examples": [ /* ----- proprietà interessata ------*/
        {
          "id": 1,
          "title": "DEM | Eventi e Ricorrenze",
          "slug": "dem_eventi_e_ricorrenze",
          "route": "/gdo/esempi/dem_eventi_e_ricorrenze",
          "iconName": "",
          "description": "Il <strong>Direct Email Marketing</strong> è una delle soluzioni per <strong>promuovere la propria attività, ottenere nuovi contatti qualificati, posizionare il brand sul mercato</strong> e <strong>migliorare l’<i>engagement</i> con il pubblico.</strong> Attraverso la creazione di DEM personalizzate, inviate ad <strong>anagrafiche segmentate</strong> e che rimandano a landing page ottimizzate, infatti, è possibile ad esempio impattare su <strong>enormi volumi di audience in target</strong> con il business del cliente.",
          "flusso": {
            "deviceIsDesktop": false,
            "mockups": []
          },
          "video": {
            "id": "lp_dem_festivita-video",
            "src": "assets/gdo/video/esempi/dem_lp_festivita_.mp4",
            "poster": "assets/gdo/images/esempi/lp_dem_eventi_e_ricorrenze/video_poster.jpg",
            "deviceIsDesktop": false
          }
        },
        {
          "id": 2, /* ----- nuovo oggetto esempio ------*/
          "title": "DEM | Eventi e Ricorrenze",
          "slug": "dem_eventi_e_ricorrenze",
          "route": "/gdo/esempi/dem_eventi_e_ricorrenze",
          "iconName": "",
          "description": "Il <strong>Direct Email Marketing</strong> è una delle soluzioni per <strong>promuovere la propria attività, ottenere nuovi contatti qualificati, posizionare il brand sul mercato</strong> e <strong>migliorare l’<i>engagement</i> con il pubblico.</strong> Attraverso la creazione di DEM personalizzate, inviate ad <strong>anagrafiche segmentate</strong> e che rimandano a landing page ottimizzate, infatti, è possibile ad esempio impattare su <strong>enormi volumi di audience in target</strong> con il business del cliente.",
          "flusso": {
            "deviceIsDesktop": false,
            "mockups": []
          },
          "video": {
            "id": "lp_dem_festivita-video",
            "src": "assets/gdo/video/esempi/dem_lp_festivita_.mp4",
            "poster": "assets/gdo/images/esempi/lp_dem_eventi_e_ricorrenze/video_poster.jpg",
            "deviceIsDesktop": false
          }
        }
      ]
    }
  ]
}
```

> **Attenzione**
>
> Durante la creazione di nuovi esempi metti in ordine crescente la proprietà **id** dei vari oggetti esempi e modifica o elimina le proprietà al suo interno.

## <a name="modifica-esempio">4.2 Modifica Esempio</a>
### Percorso

> Il file json da modificare si trova al percorso:
>
> Porfolio-Sales/projects/portfolio/src/verticals.json

In questo file recati nella proprietà **categories** e subito dopo su **examples** e modifica l'oggetto interessato

## <a name="elimina-esempio">4.3 Elimina Esempio</a>
### Percorso

> Il file json da modificare si trova al percorso:
>
> Porfolio-Sales/projects/portfolio/src/verticals.json

In questo file recati nella proprietà **categories** -> **examples** trova l'oggetto in questione e elimina dall'array in cui si trova.

> **Attenzione**
>
> Durante l'eliminazione metti in ordine crescente la proprietà **id** dei vari oggetti esempio
