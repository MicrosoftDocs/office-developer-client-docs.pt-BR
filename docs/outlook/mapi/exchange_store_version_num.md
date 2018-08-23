---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 152afd68bea44f3485b2cc566f3f0d2768590704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594471"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Armazena informações de versão do Microsoft Exchange Server conectados a contas em um perfil do Microsoft Office Outlook.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a>Members

 _wMajorVersion_
  
- Número da versão principal que geralmente é incrementado quando uma versão contém alterações e novos recursos significativos em termos de funcionalidade.
    
 _wMinorVersion_
  
- Número de versão secundária que corresponde a um número específico de versão principal e que geralmente é incrementado quando uma versão contém secundárias novos recursos ou correções significativas.
    
 _wBuild_
  
- Número de compilação principais que corresponde aos números de versão principal e secundária específica e que geralmente é incrementado uma versão interna que contém os novos recursos ou correções. Esse valor também é incrementado quando a versão é uma ramificação principais de código interno ou etapa, como uma versão release candidate.
    
 _wMinorBuild_
  
- Número de compilação secundária que geralmente é incrementado uma versão interna que contém novos recursos ou corrige correspondente a uma compilação principal específica que denota uma filial principais de código ou etapa do projeto.
    
## <a name="see-also"></a>Confira também



[Sobre as adições de MAPI](about-mapi-additions.md)
  
[Propriedade canônica PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

