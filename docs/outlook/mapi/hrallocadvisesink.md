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
ms.openlocfilehash: d5cb43bfa3acd912e397644657223c177d6afb30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589319"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um objeto de coletor de eventos advise, recebe um contexto especificado por uma função de retorno de chamada seja disparado por uma notificação de evento e a implementação de chamada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parâmetros

 _lpfnCallback_
  
> [in] Ponteiro para uma função de retorno de chamada com base em protótipo [NOTIFCALLBACK](notifcallback.md) que MAPI é chamar quando ocorre um evento de notificação do recém-criado coletor de eventos de aviso. 
    
 _lpvContext_
  
> [in] Ponteiro para dados do chamador passado para a função de retorno de chamada quando chamadas de MAPI-lo. Os dados do chamador podem representar um endereço de significância para o cliente ou o provedor. Geralmente, para código C++, o parâmetro _lpvContext_ representa um ponteiro para o endereço de um objeto. 
    
 _lppAdviseSink_
  
> [out] Ponteiro para um ponteiro para um objeto de coletor de eventos advise.
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Para usar a função **HrAllocAdviseSink** , um aplicativo cliente ou um provedor de serviço cria um objeto para receber notificações, cria uma função de retorno de chamada de notificação com base no protótipo de função [NOTIFCALLBACK](notifcallback.md) que vai com esse objeto, e passa um ponteiro para o objeto na função **HrAllocAdviseSink** como o valor de _lpvContext_ . Isso realiza uma notificação; e como parte do processo de notificação, MAPI chama a função de retorno de chamada com o ponteiro de objeto, como o contexto. 
  
MAPI implementa seu mecanismo de notificação de forma assíncrona. Em C++, o retorno de chamada de notificação pode ser um método do objeto. Se o objeto gerar a notificação não estiver presente, o cliente ou solicitar a notificação de provedor deve manter uma contagem de referência separada para aquele objeto para o objeto coletor de eventos de aviso. 
  
> [!CAUTION]
> **HrAllocAdviseSink** deve ser usado com moderação; é mais segura para os clientes criar seus próprios PIAs advise. 
  

