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
ms.openlocfilehash: 90fe316bfd11d712f02187b6a569450b747a6409
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587926"
---
# <a name="imapigetsession--iunknown"></a>IMAPIGetSession : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à sessão MAPI atual associado ao objeto de suporte. Provedores MAPI pode consultar seu objeto de suporte de MAPI para esta interface. Para obter mais informações sobre objetos de suporte, consulte [Visão geral do objeto de suporte](support-object-overview.md).
  
|||
|:-----|:-----|
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIGetSession  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetMAPISession](imapigetsession-getmapisession.md) <br/> |Chamado para obter um ponteiro para a sessão MAPI atual.  <br/> |
   
## <a name="see-also"></a>Confira também



[GetMAPISession](imapigetsession-getmapisession.md)
  
[IMAPISupport](imapisupportiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)
  
[Visão geral de objetos de suporte](support-object-overview.md)

