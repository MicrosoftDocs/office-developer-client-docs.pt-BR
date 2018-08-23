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
ms.openlocfilehash: ffac4328401b8afbc07eb650ea6c08da5f9c51b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594492"
---
# <a name="mapiofflinecreateinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
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
  
> Ela deve ser 0.
    
 **pwszProfileName**
  
> O nome do perfil.
    
 **ulCapabilities**
  
> Uma máscara de bits dos seguintes sinalizadores de recurso.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |O objeto offline é capaz de entrar no modo offline.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |O objeto offline é capaz de modo online.  <br/> |
   
 **pGUID**
  
> Ponteiro para um GUID que é usado para identificar exclusivamente esse tipo de objeto offline a partir de outros objetos offline. GUID_GlobalState refere-se ao objeto offline global que objetos podem usar como um objeto pai.
    
 **pInstance**
  
> Ponteiro para GUID que identifica exclusivamente esse objeto offline. Ele é usado para eliminar a ambiguidade este objetos offline dentre outros objetos.
    
 **pParent**
  
> Ponteiro para o objeto offline que é o pai deste objeto offline e cujas alterações herdarão esse objeto offline.
    
 **pMAPISupport**
  
>  Identifica o objeto de suporte MAPI que que usará esse objeto offline. Por exemplo, se esse objeto offline é usado para rastrear um repositório offline e estado online, em seguida, isso é os repositórios de suportam ao objeto. No entanto, caso se trate de um objeto offline para um objeto com nenhum objeto de suporte, ela pode ser NULL. 
    
 **pAggregateInfo**
  
> Um ponteiro para uma estrutura MAPIOFFLINE_AGGREGATEINFO. Para obter mais informações, consulte [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).
    
 **pConnectInfo**
  
> Deve ser nula.
    
## <a name="see-also"></a>Confira também



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

