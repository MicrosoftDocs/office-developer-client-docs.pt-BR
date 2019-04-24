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
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286601"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que os servidores de formulário recebam notificações de visualizadores de formulários. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform. h  <br/> |
|Exposto por:  <br/> |Objetos de coletor de aviso de formulário  <br/> |
|Implementado por:  <br/> |Servidores de formulário  <br/> |
|Chamado por:  <br/> |Visualizadores de formulários  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Indica que uma alteração ocorreu no status do Visualizador de formulários.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Indica se o formulário pode manipular a classe de mensagem da próxima mensagem a ser exibida.  <br/> |
   
## <a name="remarks"></a>Comentários

Os servidores de formulário usam um objeto de coletor de aviso de formulário para implementar o **IMAPIFormAdviseSink** em vez de incluí-lo com o objeto Form. Portanto, os visualizadores de formulário devem esperar uma chamada com falha para o método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) de um formulário para obter um ponteiro para esta interface. 
  
Os servidores de formulário chamam o método [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) de um visualizador para registrar notificações. Um ponteiro para a implementação do **IMAPIFormAdviseSink** está incluído como um parâmetro. 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

