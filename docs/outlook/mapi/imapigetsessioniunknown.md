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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436647"
---
# <a name="imapigetsession--iunknown"></a>IMAPIGetSession : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à sessão MAPI atual associada ao objeto de suporte. Os provedores mapi podem consultar seu objeto de suporte MAPI para esta interface. Para obter mais informações sobre objetos de suporte, consulte [Visão geral do objeto de suporte.](support-object-overview.md)
  
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

