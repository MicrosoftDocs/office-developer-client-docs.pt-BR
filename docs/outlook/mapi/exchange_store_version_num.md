---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bf60b12a6e4575d3504a112aa2b54fb8c4ae23c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287032"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Armazena informações de versão do Microsoft Exchange Server nas quais contas de um perfil do Microsoft Office Outlook estão conectadas.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a>Membros

 _wMajorVersion_
  
- Número de versão principal que geralmente é incrementado quando uma versão contém novos recursos e alterações consideráveis na funcionalidade.
    
 _wMinorVersion_
  
- Número de versão secundário que corresponde a um número de versão principal específico e que geralmente é incrementado quando uma versão contém novos recursos secundários ou correções significativas.
    
 _wBuild_
  
- Número de compilação principal que corresponde aos números de versão principal e secundária e que geralmente é incrementado em uma versão interna que contém novos recursos ou correções. Esse valor também é incrementado quando o lançamento é uma ramificação de código interno principal ou uma etapa, como um candidato de versão.
    
 _wMinorBuild_
  
- Número de compilação secundário que geralmente é incrementado em uma versão interna que contém novos recursos ou correções correspondentes a uma compilação principal específica que indica uma ramificação de código principal ou Marco.
    
## <a name="see-also"></a>Confira também



[Sobre as adições de MAPI](about-mapi-additions.md)
  
[Propriedade canônica PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

