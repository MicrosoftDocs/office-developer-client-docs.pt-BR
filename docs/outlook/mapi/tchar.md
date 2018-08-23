---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 357ace3267f22d751a20a12c96f108ee2f8ae1e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595199"
---
# <a name="tchar"></a>TCHAR

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma cadeia de caracteres Win32 que pode ser usada para descrever as cadeias de caracteres ANSI, Unicode ou DBCS. Para plataformas ANSI e DBCS, TCHAR é definida da seguinte maneira:
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a>Comentários

Plataformas de Unicode, TCHAR é definido como o tipo WCHAR um sinônimo. 
  
Clientes MAPI podem usar o tipo de dados TCHAR para representar uma cadeia de caracteres de tipo de WCHAR ou char. Certifique-se definir o UNICODE constante simbólico e limitar a plataforma quando for solicitado. MAPI irá interpretar as informações de plataforma e internamente traduzir TCHAR para a cadeia de caracteres apropriada. O tipo de propriedade MAPI, PT_TSTRING, funciona como o tipo de dados TCHAR. Quando a plataforma oferece suporte a Unicode, propriedades do tipo PT_TSTRING recebem o tipo PT_UNICODE em tempo de compilação. Quando a plataforma não oferece suporte a Unicode, essas propriedades recebem o tipo PT_STRING8.
  
Para obter mais informações sobre essa funcionalidade, consulte [Conjuntos de caracteres](mapi-character-sets.md) e a [Lista de tipos de propriedade](property-types.md). 
  
## <a name="see-also"></a>Confira também



[Tipos de dados MAPI](mapi-data-types.md)

