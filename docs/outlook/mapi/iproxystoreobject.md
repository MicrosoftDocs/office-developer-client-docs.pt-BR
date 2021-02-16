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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315516"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece um objeto de armazenamento IMAP (Internet Message Access Protocol) que foi deswrapped e que permite o acesso a itens no arquivo de Pastas Particulares (PST) sem invocar a sincronização e baixar os itens.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herdado de:  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Fornecido por:  <br/> |Provedor de armazenamento de mensagens  <br/> |
|Identificador de interface:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Obtém um ponteiro para um armazenamento IMAP não mapeado.  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
   
## <a name="remarks"></a>Comentários

Chame [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) no repositório de mensagens de origem para obter a interface **IProxyStoreObject.** Em seguida, **chame IProxyStoreObject::UnwrapNoRef** para obter o objeto de repositório não mapeado. Se **QueryInterface** retornar o erro **MAPI_E_INTERFACE_NOT_SUPPORTED**, o armazenamento não foi empacotado. 
  
Como **UnwrapNoRef** não incrementa a contagem de referência desse novo ponteiro para o objeto de armazenamento não mapeado, depois de chamar **UnwrapNoRef** com êxito, você deve chamar [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para manter a contagem de referência. 
  

