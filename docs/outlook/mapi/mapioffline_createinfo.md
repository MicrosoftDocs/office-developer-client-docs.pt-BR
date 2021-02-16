---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429562"
---
# <a name="mapioffline_createinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa estrutura é usada com [HrCreateOfflineObj](hrcreateofflineobj.md).
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a>Members

 **ulSize**
  
> O tamanho da estrutura.
    
 **ulCreateFlags**
  
> Deve ser 0.
    
 **pwszProfileName**
  
> O nome do perfil.
    
 **ulCapabilities**
  
> Uma máscara de bits dos sinalizadores de funcionalidade a seguir.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |O objeto offline é capaz de ficar offline.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |O objeto offline é capaz de ficar online.  <br/> |
   
 **pGUID**
  
> Ponteiro para um GUID que é usado para identificar exclusivamente esse tipo de objeto offline de outros objetos offline. GUID_GlobalState se refere ao objeto offline global que os objetos podem usar como um objeto pai.
    
 **pInstance**
  
> Ponteiro para GUID que identifica exclusivamente esse objeto offline. Ele é usado para desambiguar esses objetos offline de outros objetos.
    
 **pParent**
  
> Ponteiro para objeto offline que é o pai deste objeto offline e cujas alterações esse objeto offline herdará.
    
 **pMAPISupport**
  
>  Identifica o objeto de suporte MAPI que usará esse objeto offline. Por exemplo, se esse objeto offline for usado para controlar o estado offline e online de um armazenamento, esse será o objeto de suporte aos armazenamentos. No entanto, se for um objeto offline para um objeto sem suporte, ele poderá ser NULL. 
    
 **pAggregateInfo**
  
> Um ponteiro para uma MAPIOFFLINE_AGGREGATEINFO estrutura. Para obter mais informações, [consulte MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).
    
 **pConnectInfo**
  
> Deve ser nulo.
    
## <a name="see-also"></a>Confira também



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

