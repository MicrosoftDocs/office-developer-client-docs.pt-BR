---
title: IMAPIGetSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIGetSession
api_type:
- COM
ms.assetid: d1b662e2-1516-46b2-ba94-4092d79b5a39
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0b861a11b6bc1d590225a0c99b20f8be38edfd2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321578"
---
# <a name="imapigetsession--iunknown"></a>IMAPIGetSession : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à sessão MAPI atual associada ao objeto support. Os provedores MAPI podem consultar o objeto de suporte MAPI para esta interface. Para obter mais informações sobre objetos de suporte, consulte [visão geral do objeto support](support-object-overview.md).
  
|||
|:-----|:-----|
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIGetSession  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetMAPISession](imapigetsession-getmapisession.md) <br/> |Chamado para obter um ponteiro para a sessão MAPI atual.  <br/> |
   
## <a name="see-also"></a>Confira também



[GetMAPISession](imapigetsession-getmapisession.md)
  
[IMAPISupport](imapisupportiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)
  
[Visão geral do objeto support](support-object-overview.md)

