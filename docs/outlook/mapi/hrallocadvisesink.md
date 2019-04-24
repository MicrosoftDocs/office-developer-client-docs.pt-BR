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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348213"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um objeto de coletor de aviso, dado um contexto especificado pela implementação de chamada e uma função de retorno de chamada a ser disparada por uma notificação de evento. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
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
  
> no Ponteiro para uma função de retorno de chamada com base no protótipo [NOTIFCALLBACK](notifcallback.md) que o MAPI deve chamar quando ocorre um evento de notificação para o coletor de aviso recém-criado. 
    
 _lpvContext_
  
> no Ponteiro para dados do chamador passados para a função de retorno de chamada quando o MAPI o chama. Os dados do chamador podem representar um endereço de importância para o cliente ou provedor. Normalmente, para o código C++, o parâmetro _lpvContext_ representa um ponteiro para o endereço de um objeto. 
    
 _lppAdviseSink_
  
> bota Ponteiro para um ponteiro para um objeto de coletor de aviso.
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Para usar a função **HrAllocAdviseSink** , um aplicativo cliente ou provedor de serviços cria um objeto para receber notificações, cria uma função de retorno de chamada de notificação com base no protótipo da função [NOTIFCALLBACK](notifcallback.md) que acompanha esse objeto, e passa um ponteiro para o objeto na função **HrAllocAdviseSink** como o valor _lpvContext_ . Fazer isso executará uma notificação; e como parte do processo de notificação, MAPI chama a função de retorno de chamada com o ponteiro do objeto como o contexto. 
  
O MAPI implementa o mecanismo de notificação de forma assíncrona. No C++, o retorno de chamada de notificação pode ser um método de objeto. Se o objeto que gera a notificação não estiver presente, o cliente ou provedor que solicitar a notificação deverá manter uma contagem de referência separada para esse objeto para o coletor de aviso do objeto. 
  
> [!CAUTION]
> **HrAllocAdviseSink** deve ser usado com moderação; é mais seguro que os clientes criem seus próprios coletores de aviso. 
  

