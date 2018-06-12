---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 27db5f54f6a6feba77308a4a63fe4c16448550cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767478"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**Aplica-se a**: Outlook 
  
Obtém informações sobre o que pode suportar um repositório com base no seletor especificado.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Par�metros

 *mscapSelector* 
  
> [in] Seletor indicando quais recursos para retornar.
    
## <a name="return-value"></a>Valor retornado

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Suporte para home pages de pasta em um repositório não padrão. Isso pode ser retornado se **MSCAP_SEL_FOLDER** for especificado no *mscapSelector* . 
    
MSCAP_RES_ANNOTATION
  
> Se uma restrição contiver nenhum argumento inválido como propriedades inválidos, o repositório ignora os argumentos inválidos e processa somente os argumentos válidos. Isso pode ser retornado se **MSCAP_SEL_RESTRICTION** for especificado no *mscapSelector* . 
    
NULL
  
> O repositório não oferece suporte a qualquer recurso com base no seletor determinado.
    

