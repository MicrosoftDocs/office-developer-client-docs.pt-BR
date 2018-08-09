---
title: Sobre constantes de moeda
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82253123
localization_priority: Normal
ms.assetid: d94c740f-29e1-1e7f-39f6-8aa215f3111d
description: Para formatar um número como uma moeda, utilize a função CY e passe uma constante opcional para especificar a moeda de que país/região será utilizada. As constantes de moeda podem ser especificadas como o número de identificação correspondente a um país/uma região ou como uma cadeia de caracteres (entre aspas duplas) correspondente a uma abreviatura de três caracteres ISO 4217.
ms.openlocfilehash: ce27cbcb03b4c41cce3cf08fbcd234678fcdc773
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771243"
---
# <a name="about-currency-constants"></a>Sobre constantes de moeda

Para formatar um número como uma moeda, utilize a função CY e passe uma constante opcional para especificar a moeda de que país/região será utilizada. As constantes de moeda podem ser especificadas como o número de identificação correspondente a um país/uma região ou como uma cadeia de caracteres (entre aspas duplas) correspondente a uma abreviatura de três caracteres ISO 4217.
  
Se você mostrar símbolos de moeda para moedas não-locais e o sistema não reconhecer o símbolo de uma determinada moeda, será exibido o símbolo de dólar ($).
  
## <a name="ids-and-abbreviations"></a>Identificações e abreviações

|**ID DO**|**Abbreviation**|**Moeda**|
|:-----|:-----|:-----|
| 0  <br/> | SYS  <br/> | Utiliza configurações de sistema  <br/> |
| 1  <br/> | XXX  <br/> | Formata como um número  <br/> |
| 2 - 9  <br/> | Reservado  <br/> |
| 10  <br/> | EUR  <br/> | Euro  <br/> |
| 11  <br/> | USD  <br/> | Dólar americano  <br/> |
| 12  <br/> | ATS  <br/> | Xelim austríaco  <br/> |
| 13  <br/> | AUD  <br/> | Dólar australiano  <br/> |
| 14  <br/> | BEF  <br/> | Franco belga  <br/> |
| 15  <br/> | CAD  <br/> | Dólar canadense  <br/> |
| 16  <br/> | CHF  <br/> | Franco suíço  <br/> |
| 17  <br/> | CNY  <br/> | Yuan chinês  <br/> |
| 18  <br/> | DEM  <br/> | Marco alemão  <br/> |
| 19  <br/> | DKK  <br/> | Coroa dinamarquesa  <br/> |
| 20  <br/> | ESP  <br/> | Peseta espanhola  <br/> |
| 21  <br/> | FIM  <br/> | Marco finlandês  <br/> |
| 22  <br/> | FRF  <br/> | Franco francês  <br/> |
| 23  <br/> | GBP  <br/> | Libra esterlina britânica  <br/> |
| 24  <br/> | GRD  <br/> | Dracma grega  <br/> |
| 25  <br/> | HKD  <br/> | Dólar de Hong Kong R.A.E (Região Administrativa Especial)  <br/> |
| 26  <br/> | HUF  <br/> | Florim húngaro  <br/> |
| 27  <br/> | IDR  <br/> | Rúpia indonésia  <br/> |
| 28  <br/> | IEP  <br/> | Libra irlandesa  <br/> |
| 29  <br/> | ILS  <br/> | Shekel israelense  <br/> |
| 30  <br/> | ITL  <br/> | Lira italiana  <br/> |
| 31  <br/> | JPY  <br/> | Iene japonês  <br/> |
| 32  <br/> | KRW  <br/> | Won coreano  <br/> |
| 33  <br/> | LUF  <br/> | Franco luxemburguês  <br/> |
| 34  <br/> | MXN  <br/> | Peso mexicano  <br/> |
| 35  <br/> | MYR  <br/> | Ringgit malaio  <br/> |
| 36  <br/> | NLG  <br/> | Florim holandês  <br/> |
| 37  <br/> | NOK  <br/> | Coroa norueguesa  <br/> |
| 38  <br/> | NZD  <br/> | Dólar neozelandês  <br/> |
| 39  <br/> | PHP  <br/> | Peso filipino  <br/> |
| 40  <br/> | PLZ (uso histórico PLN.)  <br/> | Zloti Polonês  <br/> |
| 41  <br/> | PTE  <br/> | Escudo português  <br/> |
| 42  <br/> | ROL  <br/> | Leu romeno  <br/> |
| 43  <br/> | RUR (uso histórico RUB.)  <br/> | Rublo russo  <br/> |
| 44  <br/> | SEK  <br/> | Coroa sueca  <br/> |
| 45  <br/> | SGD  <br/> | Dólar de Cingapura  <br/> |
| 46  <br/> | THB  <br/> | Baht tailandês  <br/> |
| 47  <br/> | TWD  <br/> | Novo dólar de Taiwan  <br/> |
| 48  <br/> | XEU (uso histórico EUR.)  <br/> | Euro (antes de 1998)  <br/> |
| 49  <br/> | YUN (uso histórico YUM.)  <br/> | Dinar iugoslavo  <br/> |
| 50  <br/> | ZAR  <br/> | Rand sul-africano  <br/> |
| 51 - 55  <br/> | Reservado  <br/> |
| 56  <br/> | ARS  <br/> | Peso argentino  <br/> |
| 57  <br/> | BMD  <br/> | Dólar das Bermudas  <br/> |
| 58  <br/> | BOB  <br/> | Boliviano da Bolívia  <br/> |
| 59  <br/> | BRL  <br/> | Real brasileiro  <br/> |
| 60  <br/> | BSD  <br/> | Dólar das Bahamas  <br/> |
| 61  <br/> | CLP  <br/> | Peso chileno  <br/> |
| 62  <br/> | COP  <br/> | Peso colombiano  <br/> |
| 63  <br/> | CRC  <br/> | Colón da Costa Rica  <br/> |
| 64  <br/> | CZK  <br/> | Coroa tcheca  <br/> |
| 65  <br/> | DOP  <br/> | Peso dominicano  <br/> |
| 66  <br/> | ECS  <br/> | Sucre equatoriano  <br/> |
| 67  <br/> | EGP  <br/> | Libra egípcia  <br/> |
| 68  <br/> | HNL  <br/> | Lempira hondurenha  <br/> |
| 69  <br/> | INR  <br/> | Rúpia indiana  <br/> |
| 70  <br/> | JMD  <br/> | Dólar jamaicano  <br/> |
| 71  <br/> | JOD  <br/> | Dinar jordaniano  <br/> |
| 72  <br/> | KWD  <br/> | Dinar Kuwaitiano  <br/> |
| 73  <br/> | MOP  <br/> | Pataca de Macau  <br/> |
| 74  <br/> | NIO  <br/> | Córdova de ouro nicaraguense  <br/> |
| 75  <br/> | PAB  <br/> | Balboa panamenho  <br/> |
| 76  <br/> | PEN  <br/> | Novo Sol peruano  <br/> |
| 77  <br/> | PKR  <br/> | Rúpia paquistanesa  <br/> |
| 78  <br/> | PYG  <br/> | Guarani paraguaio  <br/> |
| 79  <br/> | SAR  <br/> | Rial saudita  <br/> |
| 80  <br/> | SIT  <br/> | Tolar esloveno  <br/> |
| 81  <br/> | SKK  <br/> | Coroa eslovaca  <br/> |
| 82  <br/> | SVC  <br/> | Colón salvadorenho  <br/> |
| 83  <br/> | TRY  <br/> | Nova Lira Turca  <br/> |
| 84  <br/> | TTD  <br/> | Dólar de Trinidad e Tobago  <br/> |
| 85  <br/> | UYU  <br/> | Peso uruguaio  <br/> |
| 86  <br/> | VEB  <br/> | Bolívar venezuelano  <br/> |
| 87  <br/> | VND  <br/> | Dong vietnamita  <br/> |
| 88  <br/> | BRL  <br/> | Real brasileiro  <br/> |
| 89  <br/> | PLN  <br/> | Zloti Polonês  <br/> |
| 90  <br/> | RUB  <br/> | Rublo russo  <br/> |
| 91  <br/> | YUM  <br/> | Dinar iugoslavo  <br/> |
| 92  <br/> | BYB (uso histórico BYR.)  <br/> | Rublo belarusso  <br/> |
| 93  <br/> | UAH  <br/> | Hryvinia ucraniana  <br/> |
| 94  <br/> | AFA  <br/> | Afegane (adicionado ao Visio 2002)  <br/> |
| 95  <br/> | ALL  <br/> | Lek (adicionado ao Visio 2002)  <br/> |
| 96  <br/> | DZD  <br/> | Dinar argelino (adicionado ao Visio 2002)  <br/> |
| 97  <br/> | ADP  <br/> | Peseta andorrana (adicionado ao Visio 2002)  <br/> |
| 98  <br/> | AOA  <br/> | Kwanza (adicionado ao Visio 2002)  <br/> |
| 99  <br/> | XCD  <br/> | Dólar do Caribe Oriental (adicionado ao Visio 2002)  <br/> |
| 100  <br/> | AMD  <br/> | Dracma armênio (adicionado ao Visio 2002)  <br/> |
| 101  <br/> | AWG  <br/> | Florim de Aruba (adicionado ao Visio 2002)  <br/> |
| 102  <br/> | AZM  <br/> | Manat azerbaidjano (adicionado ao Visio 2002)  <br/> |
| 103  <br/> | BHD  <br/> | Dinar bareinita (adicionado ao Visio 2002)  <br/> |
| 104  <br/> | BDT  <br/> | Taka (adicionado ao Visio 2002)  <br/> |
| 105  <br/> | BBD  <br/> | Dólar barbadiano (adicionado ao Visio 2002)  <br/> |
| 106  <br/> | BYR  <br/> | Rublo Belarusso (adicionado ao Visio 2002)  <br/> |
| 107  <br/> | BZD  <br/> | Dólar belizenho (adicionado ao Visio 2002)  <br/> |
| 108  <br/> | XOF  <br/> | Franco CFA BCEAO (adicionado ao Visio 2002)  <br/> |
| 109  <br/> | BTN  <br/> | Ngultrum (adicionado ao Visio 2002)  <br/> |
| 110  <br/> | BAM  <br/> | Marcos conversíveis (adicionado no Visio 2002)  <br/> |
| 111  <br/> | BWP  <br/> | Pula (adicionado ao Visio 2002)  <br/> |
| 112  <br/> | BND  <br/> | Dólar bruneano (adicionado ao Visio 2002)  <br/> |
| 113  <br/> | BGL (uso histórico BGN.)  <br/> | Lev  <br/> |
| 114  <br/> | BGN  <br/> | Lev búlgaro (adicionado ao Visio 2002)  <br/> |
| 115  <br/> | BIF  <br/> | Franco burundinês (adicionado ao Visio 2002)  <br/> |
| 116  <br/> | KHR  <br/> | Riel (adicionado ao Visio 2002)  <br/> |
| 117  <br/> | XAF  <br/> | Franco CFA BEAC (adicionado ao Visio 2002)  <br/> |
| 118  <br/> | CVE  <br/> | Escudo cabo-verdiano (adicionado ao Visio 2002)  <br/> |
| 119  <br/> | KYD  <br/> | Dólar das Ilhas Cayman (adicionado ao Visio 2002)  <br/> |
| 120  <br/> | KMF  <br/> | Franco comorense (adicionado ao Visio 2002)  <br/> |
| 121  <br/> | CDF  <br/> | Franco congolês (adicionado ao Visio 2002)  <br/> |
| 122  <br/> | HRK  <br/> | Kuna croata (adicionado ao Visio 2002)  <br/> |
| 123  <br/> | CUP  <br/> | Peso cubano (adicionado ao Visio 2002)  <br/> |
| 124  <br/> | CYP  <br/> | Libra cipriota (adicionado ao Visio 2002)  <br/> |
| 125  <br/> | DJF  <br/> | Franco jibutiano (adicionado ao Visio 2002)  <br/> |
| 126  <br/> | TPE  <br/> | Escudo timorense (adicionado ao Visio 2002)  <br/> |
| 127  <br/> | ERN  <br/> | Nakfa (adicionado ao Visio 2002)  <br/> |
| 128  <br/> | EEK  <br/> | Coroa (adicionado no Visio 2002)  <br/> |
| 129  <br/> | ETB  <br/> | Birr etíope (adicionado ao Visio 2002)  <br/> |
| 130  <br/> | FKP  <br/> | Libra das Ilhas Malvinas (Ilhas Falkland) (adicionado ao Visio 2002)  <br/> |
| 131  <br/> | FJD  <br/> | Dólar fijiano (adicionado ao Visio 2002)  <br/> |
| 132  <br/> | XPF  <br/> | Franco CFA (adicionado ao Visio 2002)  <br/> |
| 133  <br/> | GMD  <br/> | Dalasi (adicionado ao Visio 2002)  <br/> |
| 134  <br/> | GEL  <br/> | Lari (adicionado ao Visio 2002)  <br/> |
| 135  <br/> | GHC  <br/> | Cedi (adicionado ao Visio 2002)  <br/> |
| 136  <br/> | GIP  <br/> | Libra gibraltarina (adicionado ao Visio 2002)  <br/> |
| 137  <br/> | GTQ  <br/> | Quetzal (adicionado ao Visio 2002)  <br/> |
| 138  <br/> | GNF  <br/> | Franco guineano (adicionado ao Visio 2002)  <br/> |
| 139  <br/> | GWP  <br/> | Peso guineense (adicionado ao Visio 2002)  <br/> |
| 140  <br/> | GYD  <br/> | Dólar guianense (adicionado ao Visio 2002)  <br/> |
| 141  <br/> | HTG  <br/> | Gourde (adicionado ao Visio 2002)  <br/> |
| 142  <br/> | ISK  <br/> | Coroa islandesa (adicionado ao Visio 2002)  <br/> |
| 143  <br/> | IRR  <br/> | Rial iraniano (adicionado ao Visio 2002)  <br/> |
| 144  <br/> | IQD  <br/> | Dinar iraquiano (adicionado ao Visio 2002)  <br/> |
| 145  <br/> | KZT  <br/> | Tenge (adicionado ao Visio 2002)  <br/> |
| 146  <br/> | KES  <br/> | Xelim queniano (adicionado ao Visio 2002)  <br/> |
| 147  <br/> | KPW  <br/> | Won norte-coreano (adicionado ao Visio 2002)  <br/> |
| 148  <br/> | KGS  <br/> | Som (adicionado ao Visio 2002)  <br/> |
| 149  <br/> | LAK  <br/> | Kip (adicionado ao Visio 2002)  <br/> |
| 150  <br/> | NÍVEL (histórica. Usar EUR.)  <br/> | Lats letão (adicionado ao Visio 2002)  <br/> |
| 151  <br/> | LBP  <br/> | Libra libanesa (adicionado ao Visio 2002)  <br/> |
| 152  <br/> | LSL  <br/> | Loti (adicionado ao Visio 2002)  <br/> |
| 153  <br/> | LRD  <br/> | Dólar liberiano (adicionado ao Visio 2002)  <br/> |
| 154  <br/> | LYD  <br/> | Dinar líbio (adicionado ao Visio 2002)  <br/> |
| 155  <br/> | LTL  <br/> | Litus lituano (adicionado ao Visio 2002)  <br/> |
| 156  <br/> | MKD  <br/> | Dinar (adicionado ao Visio 2002)  <br/> |
| 157  <br/> | MGF (uso histórico MGA.)  <br/> | Franco de Madagascar (adicionado ao Visio 2002)  <br/> |
| 158  <br/> | MWK  <br/> | Cuacha Malauiana (adicionado ao Visio 2002)  <br/> |
| 159  <br/> | MVR  <br/> | Rúpia (adicionado ao Visio 2002)  <br/> |
| 160  <br/> | MTL  <br/> | Lira maltesa (adicionado ao Visio 2002)  <br/> |
| 161  <br/> | MRO  <br/> | Ouguiya (adicionado ao Visio 2002)  <br/> |
| 162  <br/> | MUR  <br/> | Rúpia mauriciana (adicionado ao Visio 2002)  <br/> |
| 163  <br/> | MDL  <br/> | Leu moldavo (adicionado ao Visio 2002)  <br/> |
| 164  <br/> | MNT  <br/> | Tugrik (adicionado ao Visio 2002)  <br/> |
| 165  <br/> | MAD  <br/> | Dirham marroquino (adicionado ao Visio 2002)  <br/> |
| 166  <br/> | MZM  <br/> | Metical (adicionado ao Visio 2002)  <br/> |
| 167  <br/> | MMK  <br/> | Kyat (adicionado ao Visio 2002)  <br/> |
| 168  <br/> | NAD  <br/> | Dólar namibiano (adicionado ao Visio 2002)  <br/> |
| 169  <br/> | NPR  <br/> | Rúpia nepalesa (adicionado ao Visio 2002)  <br/> |
| 170  <br/> | ANG  <br/> | Florim das Antilhas Holandesas (adicionado ao Visio 2002)  <br/> |
| 171  <br/> | NGN  <br/> | Naira (adicionado ao Visio 2002)  <br/> |
| 172  <br/> | OMR  <br/> | Rial omaniano (adicionado ao Visio 2002)  <br/> |
| 173  <br/> | PGK  <br/> | Kina (adicionado ao Visio 2002)  <br/> |
| 174  <br/> | QAR  <br/> | Rial catariano (adicionado ao Visio 2002)  <br/> |
| 175  <br/> | RWF  <br/> | Franco ruandês (adicionado ao Visio 2002)  <br/> |
| 176  <br/> | SHP  <br/> | Libra de Santa Helena (adicionado ao Visio 2002)  <br/> |
| 177  <br/> | WST  <br/> | Tala (adicionado ao Visio 2002)  <br/> |
| 178  <br/> | STD  <br/> | Dobra (adicionado ao Visio 2002)  <br/> |
| 179  <br/> | SCR  <br/> | Rúpia seichelense (adicionado ao Visio 2002)  <br/> |
| 180  <br/> | SLL  <br/> | Leone (adicionado ao Visio 2002)  <br/> |
| 181  <br/> | SBD  <br/> | Dólar das Ilhas Salomão (adicionado ao Visio 2002)  <br/> |
| 182  <br/> | SOS  <br/> | Xelim somali (adicionado ao Visio 2002)  <br/> |
| 183  <br/> | LKR  <br/> | Rúpia cingalesa (adicionado ao Visio 2002)  <br/> |
| 184  <br/> | SDD  <br/> | Dinar sudanês (adicionado ao Visio 2002)  <br/> |
| 185  <br/> | SRG  <br/> | Florim Surinamês (adicionado ao Visio 2002)  <br/> |
| 186  <br/> | SZL  <br/> | Lilangeni (adicionado ao Visio 2002)  <br/> |
| 187  <br/> | SYP  <br/> | Libra síria (adicionado ao Visio 2002)  <br/> |
| 188  <br/> | TJR (uso histórico TJS.)  <br/> | Rublo tadjique  <br/> |
| 189  <br/> | TJS  <br/> | Somoni tadjique (adicionado ao Visio 2002)  <br/> |
| 190  <br/> | TZS  <br/> | Xelim tanzaniano (adicionado ao Visio 2002)  <br/> |
| 191  <br/> | TOP  <br/> | Pa'anga (adicionado ao Visio 2002)  <br/> |
| 192  <br/> | TND  <br/> | Dinar tunisiano (adicionado ao Visio 2002)  <br/> |
| 193  <br/> | TMM  <br/> | Manat (adicionado ao Visio 2002)  <br/> |
| 194  <br/> | UGX  <br/> | Xelim ugandense (adicionado ao Visio 2002)  <br/> |
| 195  <br/> | AED  <br/> | Dirham dos Emirados Árabes Unidos (adicionado ao Visio 2002)  <br/> |
| 196  <br/> | UZS  <br/> | Sum usbeque (adicionado ao Visio 2002)  <br/> |
| 197  <br/> | VUV  <br/> | Vatu (adicionado ao Visio 2002)  <br/> |
| 198  <br/> | YER  <br/> | Rial iemenita (adicionado ao Visio 2002)  <br/> |
| 199  <br/> | ZMK  <br/> | Cuacha zambiana (adicionado ao Visio 2002)  <br/> |
| 200  <br/> | ZWD  <br/> | Dólar zimbabuense (adicionado ao Visio 2002)  <br/> |
|201  <br/> |VEF  <br/> |Bolívar forte venezuelano (adicionado ao Visio 2010)  <br/> |
|202  <br/> |MGA  <br/> |Ariary Malgaxe (adicionado ao Visio 2010)  <br/> |
|203  <br/> |RSD  <br/> |Dinar sérvio (adicionado ao Visio 2010)  <br/> |
|204  <br/> |CSD (uso histórico RSD.)  <br/> |Dinar sérvio (adicionado ao Visio 2010)  <br/> |
   

