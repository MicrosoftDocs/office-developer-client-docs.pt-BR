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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433721"
---
# <a name="exchange_store_version_num"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Armazena informações de versão para o Microsoft Exchange Server que contas em um perfil do Microsoft Office Outlook estão conectadas.
  
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
  
- Número da versão principal que geralmente é incrementado quando uma versão contém novos recursos significativos e alterações na funcionalidade.
    
 _wMinorVersion_
  
- Número de versão secundária que corresponde a um número de versão principal específico e que geralmente é incrementado quando uma versão contém pequenos recursos novos ou correções significativas.
    
 _wBuild_
  
- Número de com build principal que corresponde a números de versão principais e secundárias específicos e que geralmente é incrementado em uma versão interna que contém novos recursos ou correções. Esse valor também é incrementado quando a versão é uma ramificação de código interna importante ou um marco, como um candidato de versão.
    
 _wMinorBuild_
  
- Número de com build secundário que geralmente é incrementado em uma versão interna que contém novos recursos ou correções correspondentes a uma com build principal específica que denota uma ramificação ou etapa de código principal.
    
## <a name="see-also"></a>Confira também



[Sobre as adições de MAPI](about-mapi-additions.md)
  
[Propriedade canônica PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

