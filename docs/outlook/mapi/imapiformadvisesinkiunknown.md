---
title: IMAPIFormAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fd2575d401aa8a39d6f3b2cd08377b587b430ef1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767009"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Permite que os servidores de formulário receber notificações de visualizadores de formulário. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Expostos pelo:  <br/> |Objetos de coletor de eventos de aviso de formulário  <br/> |
|Implementada por:  <br/> |Servidores de formulário  <br/> |
|Chamado pelo:  <br/> |Visualizadores de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Indica que ocorreu uma alteração no status do Visualizador do formulário.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Indica se o formulário pode lidar com a classe de mensagem da próxima mensagem para exibir.  <br/> |
   
## <a name="remarks"></a>Comentários

Uso de servidores de formulário um formulário avise o objeto coletor de eventos para implementar **IMAPIFormAdviseSink** em vez de incluí-lo com seu objeto form. Portanto, os visualizadores de formulário devem esperar que uma chamada com Falha ao método de [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) de um formulário para obter um ponteiro para esta interface. 
  
Servidores de formulário chame o método de [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) do visualizador para registrar para notificações. Um ponteiro para sua implementação **IMAPIFormAdviseSink** é incluído como um parâmetro. 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

