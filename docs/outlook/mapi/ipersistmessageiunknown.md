---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309601"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que os visualizadores de formulário manipular o armazenamento de um formulário e fazer a transição entre os vários estados.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform.h  <br/> |
|Exposto por:  <br/> |Persistir objetos de mensagem  <br/> |
|Implementado por:  <br/> |Objetos de formulário  <br/> |
|Chamado por:  <br/> |Visualizadores de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IPersistMessage  <br/> |
|Tipo de ponteiro:  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior no objeto form.  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Retorna um identificador que representa o servidor de formulário que pode gerenciar o formulário.  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Verifica o formulário em busca de alterações feitas desde o último salvar.  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |Inicializa uma nova mensagem.  <br/> |
|[Load](ipersistmessage-load.md) <br/> |Carrega o formulário para uma mensagem especificada.  <br/> |
|[Save](ipersistmessage-save.md) <br/> |Salva um formulário revisado de volta à mensagem a partir da qual ele foi carregado ou criado.  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Notifica o formulário de que uma operação de salvar foi concluída.  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Faz com que o formulário libere sua mensagem atual.  <br/> |
   
## <a name="remarks"></a>Comentários

Todos os formulários são necessários para implementar a interface **IPersistMessage.** 
  
 **IPersistMessage** funciona da mesma forma que a interface [IPersistStorage OLE.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) Para obter mais informações, consulte os **métodos IPersistStorage.** 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

