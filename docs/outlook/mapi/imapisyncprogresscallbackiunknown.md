---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418334"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Passa o provedor de repositório como um campo na estrutura MAPISIB durante uma chamada para [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md). O provedor de repositório usa essa interface para fornecer comentários ao Microsoft Outlook sobre o status da sincronização.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> ||
|Exposto por:  <br/> |Outlook  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Chamado por:  <br/> |Provedores de repositório  <br/> |
|Identificador de interface:  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |O provedor de repositório chama periodicamente essa função para atualizar o status na caixa de diálogo enviar/receber.  <br/> |
|[Erro](imapisyncprogresscallback-error.md) <br/> |Se forem encontrados erros durante a sincronização, o provedor de repositório chamará essa função para fornecer detalhes que são exibidos na caixa de diálogo enviar/receber.  <br/> |
|[Feito](imapisyncprogresscallback-done.md) <br/> |O provedor de repositório chama essa função para informar ao Outlook que a sincronização foi concluída.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISync : IUnknown](imapisynciunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

