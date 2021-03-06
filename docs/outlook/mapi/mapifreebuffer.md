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
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410550"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Libera um buffer de memória alocado com uma chamada para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [a função MAPIAllocateMore.](mapiallocatemore.md) 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Parâmetros

 _lpBuffer_
  
> [in] Ponteiro para um buffer de memória alocado anteriormente. Se NULL for passado no  _parâmetro lpBuffer,_ **MAPIFreeBuffer** não faz nada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e liberou a memória solicitada. **MAPIFreeBuffer** também pode retornar S_OK locais já liberados ou se o bloco de memória não estiver alocado com **MAPIAllocateBuffer** e **MAPIAllocateMore**.
    
## <a name="remarks"></a>Comentários

Normalmente, quando um aplicativo cliente ou provedor de serviços chama [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md), o sistema operacional constrói em um buffer de memória contíguo uma ou mais estruturas complexas com vários níveis de ponteiros. Quando uma função ou método MAPI cria um buffer com esse conteúdo, um cliente pode liberar posteriormente todas as estruturas contidas no buffer passando para **MAPIFreeBuffer** o ponteiro para o buffer retornado pela função MAPI que criou o buffer. Para um provedor de serviços liberar um buffer de memória usando **MAPIFreeBuffer**, ele deve passar o ponteiro para esse buffer retornado com o objeto de suporte do provedor. 
  
A chamada para **MAPIFreeBuffer** para liberar um buffer específico deve ser feita assim que um cliente ou provedor terminar de usar esse buffer. Simplesmente chamar o [método IMAPISession::Logoff](imapisession-logoff.md) no final de uma sessão MAPI não libera automaticamente buffers de memória. 
  
Um cliente ou provedor de serviços deve operar na suposição de que o ponteiro passado  _em lpBuffer_ é inválido após um retorno bem-sucedido de **MAPIFreeBuffer**. Se o ponteiro indicar um bloco de memória não alocado pelo sistema de mensagens por meio de **MAPIAllocateBuffer** ou **MAPIAllocateMore** ou um bloco de memória livre, o comportamento de **MAPIFreeBuffer** será indefinido. 
  
> [!NOTE]
> Passar um ponteiro nulo para **MAPIFreeBuffer** torna o código de limpeza do aplicativo mais simples e menor porque **MAPIFreeBuffer** pode inicializar ponteiros para NULL e, em seguida, libera-los no código de limpeza sem precisar testá-los primeiro. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

