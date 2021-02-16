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
  
Fornece um mecanismo para sincronizar emails em vez de usar a API de Transporte. Essa interface é exposta em um objeto store. Usando essa interface e [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), um provedor de transporte pode fornecer mensagens de erro e progresso melhores do que aquelas que aparecem na caixa de diálogo Enviar/Receber no Microsoft Outlook.
  
A caixa de saída ainda está no armazenamento padrão. O Outlook continuará a usar as APIs de Transporte para enviar emails porque a mensagem de saída não pode estar no armazenamento externo.
  
|||
|:-----|:-----|
|Exposto por:  <br/> |Provedores de transporte e loja  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Chamado por:  <br/> |Provedores de Transporte e Loja  <br/> |
|Identificador de interface:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implementado pelos provedores de armazenamento de mensagens. Esse método é chamado pelo Outlook 2010 e pelo Outlook 2013 para iniciar a sincronização.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

