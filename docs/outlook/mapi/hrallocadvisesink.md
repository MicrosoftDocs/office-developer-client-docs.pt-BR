---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428897"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um objeto sink de aviso, dado um contexto especificado pela implementação da chamada e uma função de retorno de chamada a ser disparada por uma notificação de evento. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parâmetros

 _lpfnCallback_
  
> [in] Ponteiro para uma função de retorno de chamada com base no protótipo [NOTIFCALLBACK](notifcallback.md) que MAPI deve chamar quando um evento de notificação ocorre para o evento de aviso recém-criado. 
    
 _lpvContext_
  
> [in] Ponteiro para dados do chamador passados para a função de retorno de chamada quando MAPI o chama. Os dados do chamador podem representar um endereço significativo para o cliente ou provedor. Normalmente, para código C++, o parâmetro  _lpvContext_ representa um ponteiro para o endereço de um objeto. 
    
 _lppAdviseSink_
  
> [out] Ponteiro para um ponteiro para um objeto de evento de aconselhá-lo.
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Para usar a função **HrAllocAdviseSink,** um aplicativo cliente ou provedor de serviços cria um objeto para receber notificações, cria uma função de retorno de chamada de notificação com base no protótipo da função [NOTIFCALLBACK](notifcallback.md) que vai com esse objeto e passa um ponteiro para o objeto na função **HrAllocAdviseSink** como o valor _lpvContext._ Fazer isso executa uma notificação; e como parte do processo de notificação, MAPI chama a função de retorno de chamada com o ponteiro do objeto como o contexto. 
  
O MAPI implementa seu mecanismo de notificação de forma assíncrona. Em C++, o retorno de chamada de notificação pode ser um método de objeto. Se o objeto que está gerando a notificação não estiver presente, o cliente ou provedor que está solicitando a notificação deve manter uma contagem de referência separada para esse objeto para o sink de aviso do objeto. 
  
> [!CAUTION]
> **HrAllocAdviseSink** deve ser usado com moderação; é mais seguro para os clientes criarem seus próprios aconselhá-los. 
  

