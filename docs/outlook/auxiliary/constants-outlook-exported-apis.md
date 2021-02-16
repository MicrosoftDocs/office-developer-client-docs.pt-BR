---
title: Constantes (Outlook exportados APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Este tópico contém definições constantes para APIs que o Outlook exporta.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319870"
---
# <a name="constants-outlook-exported-apis"></a>Constantes (Outlook exportados APIs)

Este tópico contém definições constantes para APIs que o Outlook exporta.
  
## <a name="definitions-for-time-zone-support"></a>Definições para suporte a fuso horário

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>Definições para suporte a categoria

|**Constante**|**Definição**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>Identificadores de expedição diversos

Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to access the corresponding property or method, or listen to the corresponding event. 
  
|**Constante associada**|**Valor de dispid**|**Descrição**|**Interface aplicável**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |Usado para invocar a propriedade correspondente em um item para verificar se o item foi modificado, mas não foi salvo.  <br/> |Objetos no nível do item  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |Usado para invocar o método correspondente no explorer ou inspetor para especificar se a imagem de um contato deve ser exibida, com base em um determinado argumento.  <br/> |Explorer ou inspector  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Usado para manipular o evento da **função IDispatch::Invoke** que é ativas antes de uma operação de impressão.  <br/> |Application  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Usado para manipular o evento da **função IDispatch::Invoke** que é ativas quando o Outlook concluiu a leitura das propriedades do item.  <br/> |Objetos no nível do item  <br/> |
   
## <a name="see-also"></a>Confira também

- [APIs exportadas do Outlook](outlook-exported-apis.md)
- [Sobre APIs exportadas pelo Outlook](about-apis-exported-by-outlook.md)
- [Determinar se um item do Outlook foi modificado, mas não salvo (referência do Outlook auxiliar)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Especificar se deseja exibir a imagem de um contato no Outlook (referência auxiliar do Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [Eventos disponíveis e os dispids (Outlook exportados APIs)](available-events-and-their-dispids-outlook-exported-apis.md)

