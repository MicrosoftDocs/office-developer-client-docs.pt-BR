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
ms.openlocfilehash: 62fb2b069a50408713eea741cf837c421a749fcd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767633"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Permite que os visualizadores de formulário lidar com o armazenamento de um formulário e fazer a transição entre os diversos estados.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Expostos pelo:  <br/> |Objetos de mensagem de persistência  <br/> |
|Implementada por:  <br/> |Objetos de formulário  <br/> |
|Chamado pelo:  <br/> |Visualizadores de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IPersistMessage  <br/> |
|Tipo de ponteiro:  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior no objeto form.  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Retorna um identificador que representa o servidor de formulário que pode gerenciar o formulário.  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Verifica o formulário para que as alterações feitas desde o último salvamento.  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |Inicializa uma nova mensagem.  <br/> |
|[Load](ipersistmessage-load.md) <br/> |Carrega o formulário para uma mensagem especificada.  <br/> |
|[Save](ipersistmessage-save.md) <br/> |Salva um formulário revisado na mensagem do qual ele foi carregado ou criado.  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Notifica o formulário que uma gravação operação foi concluída.  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Faz com que o formulário liberar a sua mensagem atual.  <br/> |
   
## <a name="remarks"></a>Comentários

Todas as formas são necessários para implementar a interface **IPersistMessage** . 
  
 **IPersistMessage** funciona de modo semelhante à interface OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . Para obter mais informações, consulte os métodos de **IPersistStorage** . 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

