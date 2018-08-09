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
ms.openlocfilehash: fb7a8ea39d6e7b1d7df1560658ceb67a79d39d92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767299"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Oferece um mecanismo para sincronização de email em vez de usar a API de transporte. Esta interface é exposto em um objeto de repositório. Usando essa interface e [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), um provedor de transporte pode oferecer melhor progresso e mensagens de erro do que aqueles que aparecem na caixa de diálogo Enviar/receber no Microsoft Outlook.
  
A caixa de saída é ainda no armazenamento padrão. Outlook continuará usem as APIs de transporte para enviar emails, porque a mensagem de saída não pode ser no armazenamento externo.
  
|||
|:-----|:-----|
|Expostos pelo:  <br/> |Provedores de armazenamento e de transporte  <br/> |
|Implementada por:  <br/> |Outlook  <br/> |
|Chamado pelo:  <br/> |Provedores de armazenamento e de transporte  <br/> |
|Identificador de interface:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implementado por provedores de armazenamento de mensagem. Esse método é chamado pelo Outlook 2010 e o Outlook 2013 para iniciar a sincronização.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

