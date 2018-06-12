---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: f6566f567c228b6416a64dbd58653561bb592e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767663"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**Aplica-se a**: Outlook 
  
Fornece um objeto de repositório IMAP Internet Message Access Protocol () que foi desfeita e que permite o acesso aos itens no arquivo de pastas particulares (. PST) sem sincronização de invocação e baixando os itens.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herdado de:  <br/> |[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Fornecido por:  <br/> |Provedor de armazenamento de mensagem  <br/> |
|Identificador de interface:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Obtém um ponteiro para um repositório IMAP desfeito.  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
   
## <a name="remarks"></a>Coment�rios

Chame [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) no armazenamento da mensagem de origem para obter a interface **IProxyStoreObject** . Em seguida, chame **IProxyStoreObject::UnwrapNoRef** para obter o objeto store desfeita. Se **QueryInterface** retornará o erro **MAPI_E_INTERFACE_NOT_SUPPORTED**, em seguida, o repositório não foi quebrado. 
  
Porque **UnwrapNoRef** não incrementa a contagem de referência para este novo ponteiro para o objeto de repositório desfeita, após chamar o **UnwrapNoRef**com êxito, você deve chamar [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) para manter a contagem de referência. 
  

