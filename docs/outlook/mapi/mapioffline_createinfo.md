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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357124"
---
# <a name="mapiofflinecreateinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa estrutura é usada com o [HrCreateOfflineObj](hrcreateofflineobj.md).
  
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
  
> Uma máscara de bits dos seguintes sinalizadores de recurso.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |O objeto offline é capaz de ficar offline.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |O objeto offline é capaz de entrar online.  <br/> |
   
 **pGUID**
  
> Ponteiro para um GUID que é usado para identificar exclusivamente esse tipo de objeto offline de outros objetos offline. GUID_GlobalState refere-se ao objeto offline global que os objetos podem usar como um objeto pai.
    
 **pInstance**
  
> Ponteiro para o GUID que identifica exclusivamente este objeto offline. Ela é usada para desambiguar esses objetos offline de outros objetos.
    
 **pParent**
  
> Ponteiro para objeto offline que é o pai deste objeto offline e cujas alterações esse objeto offline herdará.
    
 **pMAPISupport**
  
>  Identifica o objeto de suporte MAPI que usará este objeto offline. Por exemplo, se este objeto offline é usado para controlar o estado offline e online de um repositório, este é o objeto de suporte de armazenamento. No enTanto, se este for um objeto offline para um objeto sem nenhum objeto support, ele poderá ser nulo. 
    
 **pAggregateInfo**
  
> Um ponteiro para uma estrutura MAPIOFFLINE_AGGREGATEINFO. Para obter mais informações, consulte [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).
    
 **pConnectInfo**
  
> Deve ser nulo.
    
## <a name="see-also"></a>Confira também



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

