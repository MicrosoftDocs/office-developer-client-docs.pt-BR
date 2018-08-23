---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ad3d9d12e1073610747b0ab078c6d65c09f8c7c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569138"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Libera um buffer de memória alocado com uma chamada para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) ou a função [MAPIAllocateMore](mapiallocatemore.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Parâmetros

 _lpBuffer_
  
> [in] Ponteiro para um buffer de memória alocada anteriormente. Se NULL é passada no parâmetro _lpBuffer_ , **MAPIFreeBuffer** não fará nada. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e a memória solicitada liberada. **MAPIFreeBuffer** também pode retornar S_OK em locais de liberação já ou se o bloco de memória não alocado com **MAPIAllocateBuffer** e **MAPIAllocateMore**.
    
## <a name="remarks"></a>Comentários

Normalmente, quando um aplicativo cliente ou um provedor de serviços chama [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md), as construções de sistema operacional no buffer de memória contíguos um uma ou mais estruturas complexas com vários níveis de ponteiros. Quando uma função MAPI ou o método cria um buffer com tal conteúdo, um cliente posteriormente pode liberar todas as estruturas contidas no buffer, passando para **MAPIFreeBuffer** o ponteiro para o buffer retornado pela função MAPI que criou o buffer. Para um provedor de serviço liberar um buffer de memória usando **MAPIFreeBuffer**, ele deve passar o ponteiro para esse buffer retornado com o objeto de suporte do provedor. 
  
A chamada para **MAPIFreeBuffer** para liberar um buffer específico deve ser feita assim que um cliente ou provedor for concluído usando esse buffer. Basta chamar o método de [IMAPISession::Logoff](imapisession-logoff.md) no final de uma sessão MAPI não libera automaticamente buffers de memória. 
  
Um provedor de cliente ou serviço deve operar no pressuposto de que o ponteiro transmitido _lpBuffer_ é inválido após um retorno bem-sucedido de **MAPIFreeBuffer**. Se o ponteiro indica um bloco de memória não alocado pelo sistema de mensagens por meio de **MAPIAllocateBuffer** ou **MAPIAllocateMore** ou um bloco de memória disponível, o comportamento do **MAPIFreeBuffer** é indefinido. 
  
> [!NOTE]
> Passar um ponteiro nulo para **MAPIFreeBuffer** torna o código de limpeza do aplicativo simples e menor porque **MAPIFreeBuffer** pode inicializar ponteiros para NULL e livre no código limpeza sem precisar testá-las pela primeira vez. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

