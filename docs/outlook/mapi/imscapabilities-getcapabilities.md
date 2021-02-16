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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409255"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém informações sobre o que um armazenamento pode suportar com base no seletor especificado.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Parâmetros

 *mscapSelector* 
  
> [in] Seletor indicando quais recursos retornar.
    
## <a name="return-value"></a>Valor de retorno

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Suporte para homepages de pasta em um armazenamento não padrão. Isso pode ser retornado **se MSCAP_SEL_FOLDER** especificado em  *mscapSelector*  . 
    
MSCAP_RES_ANNOTATION
  
> Se uma restrição contiver argumentos inválidos, como propriedades inválidas, o armazenamento ignorará os argumentos inválidos e processa apenas os argumentos válidos. Isso pode ser retornado **se MSCAP_SEL_RESTRICTION** especificado em  *mscapSelector*  . 
    
NULL
  
> O armazenamento não dá suporte a nenhum recurso com base no seletor determinado.
    

