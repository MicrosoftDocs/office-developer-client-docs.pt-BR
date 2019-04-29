---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405588"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece um mecanismo para sincronizar email, em vez de usar a API de transporte. Essa interface é exposta em um objeto Store. Usando esta interface e [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), um provedor de transporte pode fornecer melhores mensagens de progresso e de erro do que aqueles que aparecem na caixa de diálogo enviar/receber no Microsoft Outlook.
  
A saída ainda está no repositório padrão. O Outlook continuará a usar as APIs de transporte para enviar emails, pois a mensagem de saída não pode estar no repositório externo.
  
|||
|:-----|:-----|
|Exposto por:  <br/> |Provedores de armazenamento e transporte  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Chamado por:  <br/> |Provedores de armazenamento e transporte  <br/> |
|Identificador de interface:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implementado por provedores de repositório de mensagens. Este método é chamado pelo Outlook 2010 e pelo Outlook 2013 para iniciar a sincronização.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

