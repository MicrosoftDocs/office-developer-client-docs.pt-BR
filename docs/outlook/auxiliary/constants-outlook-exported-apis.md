---
title: Constantes (Outlook exportados APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Este tópico contém definições constantes para APIs que exporta do Outlook.
ms.openlocfilehash: 8b7a9d70b2fc5d26c52a8729797221a44526360c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564462"
---
# <a name="constants-outlook-exported-apis"></a>Constantes (Outlook exportados APIs)

Este tópico contém definições constantes para APIs que exporta do Outlook.
  
## <a name="definitions-for-time-zone-support"></a>Definições para suporte de fuso horário

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>Definições para suporte de categoria

|**Constante**|**Definição**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>Identificadores de expedição Miscellaneous

Outlook expõe os seguintes identificadores de expedição (dispids) para que os desenvolvedores podem usar [IDispatch:: Invoke](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) para acessar o método ou a propriedade correspondente ou ouvir o evento correspondente. 
  
|**Constante associada**|**Valor DISPID**|**Descrição**|**Interface aplicável**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |Usado para chamar a propriedade correspondente em um item para verificar se o item foi modificado, mas não foi salvo.  <br/> |Objetos de nível de item  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |Usado para chamar o método correspondente no explorer ou inspector para especificar se deseja exibir a imagem de um contato, com base em um determinado argumento.  <br/> |Explorer ou inspector  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Usado para manipular o evento a partir da função **IDispatch:: Invoke** que é acionado antes de uma operação de impressão.  <br/> |Aplicativo  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Usado para manipular o evento a partir da função **IDispatch:: Invoke** que é acionado quando o Outlook concluiu a ler as propriedades do item.  <br/> |Objetos de nível de item  <br/> |
   
## <a name="see-also"></a>Confira também

- [APIs exportadas do Outlook](outlook-exported-apis.md)
- [Sobre APIs exportadas pelo Outlook](about-apis-exported-by-outlook.md)
- [Determinar se um item do Outlook foi modificado, mas não salvo (referência auxiliar do Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Especifique se deseja exibir a imagem de um contato no Outlook (referência auxiliar do Outlook)](https://msdn.microsoft.com/en-us/library/office/gg262879.aspx)
- [Eventos disponíveis e os dispids (Outlook exportados APIs)](available-events-and-their-dispids-outlook-exported-apis.md)

