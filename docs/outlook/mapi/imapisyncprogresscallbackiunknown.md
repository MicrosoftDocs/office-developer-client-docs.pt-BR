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
ms.openlocfilehash: 33d811af0fc9e06902750075ba39bfb6ca88903f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593708"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Passa o provedor de armazenamento como um campo na estrutura MAPISIB durante uma chamada para [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md). O provedor de armazenamento usa essa interface para fornecer comentários para o Microsoft Outlook sobre o status da sincronização.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> ||
|Expostos pelo:  <br/> |Outlook  <br/> |
|Implementada por:  <br/> |Outlook  <br/> |
|Chamado pelo:  <br/> |Provedores de armazenamento  <br/> |
|Identificador de interface:  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |O provedor de armazenamento periodicamente chama esta função para atualizar o status na caixa de diálogo Enviar/receber.  <br/> |
|[Erro](imapisyncprogresscallback-error.md) <br/> |Se forem encontrados erros durante a sincronização, o provedor de armazenamento chama esta função para fornecer detalhes que são exibidos na caixa de diálogo Enviar/receber.  <br/> |
|[Feito](imapisyncprogresscallback-done.md) <br/> |O provedor de armazenamento chama esta função para informe ao Outlook sincronização foi concluída.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISync : IUnknown](imapisynciunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

